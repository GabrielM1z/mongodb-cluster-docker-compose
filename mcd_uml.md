## Utilisateur

Attributs :
ID utilisateur (unique)
Nom
Prénom
Email (unique)
Photo de profil
Date d’inscription
Rôles (administrateur, organisateur, membre, etc.)

## Événement

#### Attributs :
ID événement
Nom de l’événement
Description
Date de début
Date de fin
Lieu
Photo de couverture
Statut (public, privé)
Organisateurs (relation avec Utilisateur)
Participants (relation avec Utilisateur)

#### Relations :
Un événement peut avoir plusieurs organisateurs (1..*)
Un événement peut avoir plusieurs participants (0..*)


## Groupe

#### Attributs :
ID groupe
Nom du groupe
Description
Icône
Photo de couverture
Type de groupe (public, privé, secret)
Membres (relation avec Utilisateur)
Administrateurs (relation avec Utilisateur)

#### Relations :
Un groupe peut avoir plusieurs membres (1..*)
Un groupe peut avoir plusieurs administrateurs (1..*)


## Fil de Discussion

#### Attributs :
ID fil de discussion
Messages (relation avec Message)
Type de fil (lié à un événement ou un groupe)

#### Relations :
Un fil de discussion peut contenir plusieurs messages (0..*)
Un fil de discussion est lié à un seul groupe ou un seul événement


## Message

#### Attributs :
ID message
Contenu
Date de création
Auteur (relation avec Utilisateur)

#### Relations :
Un message est créé par un utilisateur
Un message peut être commenté par plusieurs utilisateurs (0..*)


## Album Photo

#### Attributs :
ID album
Photos (relation avec Photo)

#### Relations :
Un album est lié à un seul événement
Un album peut contenir plusieurs photos (0..*)


## Photo

#### Attributs :
ID photo
Lien
Description
Auteur (relation avec Utilisateur)

#### Relations :
Une photo peut être commentée par plusieurs participants (0..*)


## Sondage

#### Attributs :
ID sondage
Questions (relation avec Question)

#### Relations :
Un sondage peut contenir plusieurs questions (1..*)
Un sondage est lié à un événement


## Question

#### Attributs :
ID question
Contenu de la question
Réponses possibles (relation avec Réponse)

#### Relations :
Une question peut avoir plusieurs réponses possibles (1..*)
Une seule réponse peut être choisie par participant


## Réponse

#### Attributs :
ID réponse
Contenu de la réponse


## Billet

#### Attributs :
ID billet
Type de billet
Nom
Prénom
Adresse complète
Date d'achat
Montant

#### Relations :
Un billet est lié à un événement
Une personne extérieure peut obtenir un billet


## Shopping List (Bonus)

#### Attributs :
ID item
Nom
Quantité
Heure d’arrivée


## Covoiturage (Bonus)

#### Attributs :
ID covoiturage
Lieu de départ
Heure de départ
Prix
Nombre de places disponibles
Temps d’écart max