# Utilisation des commandes shell 

## Rendu
Le script shell `village.sh` doit est le point d'entré du programme.

## Creation d'un village

Pour ce cours, nous allons créer un village dans notre OS afin de manipuler les commandes.
Pour ce faire, nous allons considerer que le home du user **ynov** sera la ou nous allons créer notre village

les règles sont les suivantes.

* un répertoire est un espace physique ou nous pouvons nous rendre (village, habitation, etc)
* un fichier est un élement (personne, object..) et peut avoir un contenu. Il doit avec une extension en fonction du type. Par exemple, une personnage qui s'apelle toto, sera representé par le fichier toto.personnage.
* les personanges peuvent avoir des objets dans le contenu du fichier.
* le user Ynov (nous sommes connecté avec) est un spectateur. Il a cependant des droits fort sur **/home/ynov**. Faites attention au droit et user de vos ficiher (ynov:ynov 644).
 
## Etape 0

Utiliser les fichiers shell.md & cmd_to_learn.md pour avoir la liste des commandes utilisables durant ce tp.
Vous êtes libre d'utiliser tout ce que vous connaissez, les fichiers shell.md & cmd_to_learn.md sont juste la pour aider.

### Etape 1

Le village à besoin d'une Mairie pour recenser les habitants.
La mairie est un batiment comprenant 2 salles, Le bureau du maire, les archive
Deux personnes sont dans la mairie, le maire et l'assistant.
Le maire tient un registre des citoyens & des batiments.

#### Etape 1.A
* Création du village **Ynov_campus**
* Création dans le village de la mairie. Nous l'appellerons Mairie.
* Création dans la mairie des pieces suivantes:
  * Bureau
  * Archive
* Création des personnages suivants:
  * Maire dans le bureau
  * Assistant dans la mairie
* Ajouter au Maire l'objet **Clef du bureau** (ajouter un objet veut dire ajouter une ligne dans le fichier Maire.personnage)
* Ajout des objets suivant dans la salle Archive:
  * registre.objet. ce fichier est un fichier de structure de données au format yaml.
  
````YAML
---
habitants: ['Maire', 'Assistant'] # [] en yaml signifie une liste
batiments: ['Mairie', 'Maire_maison', 'Assistant_maison'] # ces deux liste sont des listes de strings
````

#### Etape 1.B

🔑 Chaque fois qu'un personnage est ajouté, vous devez lui créer une maison et l'ajouter dans le registre.

🔑 Chaque fois qu'un batiment est ajouté, vous devez l'ajouter dans la liste batiments dans le registre.

* Création de la maison du Maire. Une maison est un répertoire avec le nom du personnage + _maison. Ce qui donne Maire_maison.
* Création de la maison de l'Assistant.
* Ajouter dans la liste du registre les nouveaux habitants.
* Ajouter dans la liste du registre les nouveaux Batiments.

### Etape 2
 Vous allez supprimer tout ce que vous avez fait manuellement, et créer un script shell permettant de le faire automatiquement.

 💡 les fonctions shell vous aideront.

⚠️ Cette étape est soumise à un rendu.

### Etape 3
Dans le village, une boulangerie se crée. La boulangerie se compose d'un laboratoire communiquant avec l'etalage et la chambre froide.
Le Laboratoire et l'etalage ne peuvent pas communiquer ensemble.

* Création dans le village de la Boulangerie. Nous l'appellerons Boulangerie.
* Création dans la Boulangerie des pieces suivantes:
  * Etalage
  * Laboratoire
  * Chambre-froide
* Création des personnages suivants:
  * Boulanger dans le Laboratoire
  * Vendeur dans l'Etalage.
* Ajout des objets suivant dans la chambre froide:
  * levure.objet
  * jambon.objet
* Ajout des objets suivant dans le laboratoire:
  * pain.objet
  * pain_jambon.objet
* Création d'un lien symbolique relatif entre la chambre froide et le Laboratoire pour rendre les objets de la chambre froide disponible dans le laboratoire.
* Création d'un lien symbolique relatif pour rendre le pain et pain_jambon disponible dans l'etalage.
