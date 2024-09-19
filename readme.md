# Context
Vous devez réaliser une data base avec les outils utilisés en cours pour concevoir votre data base en fonction des spécifications demandé par facebook pour sa Nouvelle Application.

Vous travailler pour Facebook et vous êtes en charge de la refonte de sa base de donnée pour que la société améliore la réactivité de ses services.

Dans ce contexte Facebook à des besoins très précis pour que son service soit opérationnel le jour de la mise à jours de l’application.

Rendu attendu :
- Respecter à la lettre les besoins fonctionnelles de la nouvelle DB pour faire en sorte quelle soit cohérente.
- Sécuriser les schemas d’entrée des données avec des validators lorsque c’est nécessaire.
- Définir des collections spécifiques pour la mise à disposition de certaine données par rapport au besoin du CDC.
- Réaliser un MCD avec UML de votre DB qui servira de documentation.
- Installer et configurer mongodb et réaliser les schémas et sous schéma associés à vos requêtes nosql. 
- Faite en sorte de configurer un cluster avec au minium 3 instances de shard.


## 1 - Cahier des Charges
### 1.1 - Avant l’événement 

Chaque organisateur pourra facilement créer des événements en trois étapes. 

Configuration de son événement : 
Dans cette première étape, l’utilisateur paramètre uniquement les informations essentielles à son événement : 
- Nom 
- Description 
- Date de début 
- Date de fin 
- Lieu 
- Photo de couverture 
- Choix de rendre son événement privé ou public 
- La liste des organisateurs & des membres de l’événement


### 1.2 - Les groupes 

Facebook permet de créer votre groupe secret, privé ou publique afin d’y créer des événements en invitant automatiquement l’ensemble des membres. 

En effet, dans un groupe, la création d’événements se veut simplifiée en permettant l’invitation de tous les membres en un clic. Au sein d’un groupe publique, les organisateurs d’événements pourront s’ils le souhaitent partager leurs événements sur les autres réseaux sociaux afin de les aider dans la communication des événements.

Au sein de chaque groupe, un fil de discussion sera mis à disposition des utilisateurs afin de discuter entre eux.

Paramètre d’un groupe : 
- Nom
- Description
- Icône
- Photo de couverture
- Choix du type de groupe (public, privé, secret)
- Choix d’autoriser les membres de publier dans le groupe
- Choix d’autoriser les membres à créer des événements dans le groupe 

## 2 - Spécifications fonctionnelles

### Utilisateurs
Vous devez définir les attributs d’un utilisateur.
Il ne peut pas y avoir deux utilisateurs avec le même email.

### Événements 
Un événement peut avoir une multitude de participants. 
Un événement est géré par 1 ou plusieurs organisateurs. 

### Groupes 
Un groupe possède 1 ou plusieurs membres. 
Un groupe est géré par 1 ou plusieurs administrateurs. 

### Les fils de discussions 
Un fil de discussion peut être lié à 1 groupe ou 1 événement mais pas les deux. 
Un fil de discussion contient 0 ou plusieurs messages créés par un membre ou un administrateurs/organisateurs. 
Chaque membre/participant peut commenter un message. 

### Albums photo 
Un album photo est associé à 1 événement. 
Chaque album photo contient 0 ou plusieurs photos postées par 1 participant de l’événement. 
Ces photos peuvent être commentées par 0 ou plusieurs particpant de l’événement.

### Sondages 
Un événement peut avoir 0 ou plusieurs sondages créés par un organisateur. 
Un sondage comporte 1 ou plusieurs questions. 
Pour chaque question, il existe plusieurs réponses possibles mais uniquement 1 peut être choisie. 
Chaque participant de l’événement peut répondre aux différents sondages en choisissant pour chaque question sa réponse. 

### Billetterie 
Certain événement publique possède une billetterie. 
Un organisateur peut décider de créer 1 ou plusieurs types de billets à sa convenance. 
Un type de billet contient : 
- Un nom 
- Un montant 
- Une quantité limité de billet 
- Une personne extérieure peut obtenir 1 seul billet. 

Pour chaque billet acheté, on définira : 
- Un type de billet (ceux créés par l’organisateur) 
- Les données de la personne 
- Nom 
- Prénom 
- Adresse complète 
- Date d’achat


## BONUS :

### Shopping list 
Lors d’un événement si la shopping list est activée, un utilisateur peut indiquer ce qu’il va apporter à l’événement. Pour cela il indique: 
- Un nom 
- Une quantité 
- Une heure d’arrivée à l’événement 
- Chaque chose apporté doit être unique par événement 

### Covoiturage  (Bonus)
Lors d’un événement si le covoiturage est activé, un utilisateur peut indiquer qu’il se rendra en voiture à l’événement. Pour cela il indiquera : 
- Un lieu de départ
- Une heure de départ
- Le prix proposé
- Le nombre de place disponible
- Le temps maximum d’écart (ex: sur un trajet de 2h30, 30min, ce qui donne un trajet max de 3H)


## 3- Requests :
Suite à l’élaboration de vos votre base de donnée vous devrez faire en sorte de tester vos modèles en réalisant les requêtes suivantes : ICI
