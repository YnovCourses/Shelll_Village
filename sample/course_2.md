#  Utilisation shell intermédiaire

Le but de cette séance est de vous faire découvrir/utiliser de nouvelle commandes shell.

## Comment va se derouler le cours

Ce cours va etre accompagné de la liste des commandes apprises dans le module que vous allez essayer et manipuler.
Le but est de produire un ou des scripts shell permettant de créer les étapes demandé.

## La verification

Votre script shell sera joué sur une machine vierges et devras donc pouvoir recréer de A à Z les étapes demandé.
La verification & correction de ces étapes seront faite via un robot qui a été fait en meme temps que le cours.

## Format du rendu

Vous allez devoir fournir un script shell sur cette organisation => https://github.com/orgs/YnovCourses/repositories.
Merci de créer un répertoire par étudiant ou groupe d'étudiants.

Le script shell `village_advance.sh` doit est le point d'entré du programme.

# Utilisation des commandes shell 

## Creation d'un village

Pour ce cours, nous allons créer un village dans notre OS afin de manipuler les commandes.
Pour ce faire, nous allons considerer que le home du user **ynov** sera la ou nous allons créer notre village

les règles sont les suivantes.

* un répertoire est un espace physique ou nous pouvons nous rendre (village, habitation, etc)
* un fichier est un élement (personne, object..) et peut avoir un contenu. Il doit avec une extension en fontion du type. Par exemple, une personnage qui s'apelle toto, sera representé par le fichier toto.personnage.
* les personanges peuvent avoir des objets dans le contenu du fichier.
* le user Ynov (nous sommes connecté avec) est un spectateur. Il a cependant des droits fort sur **/home/ynov**. Faites attention au droit et user de vos ficiher (ynov:ynov 644).
 

## Etape 0

Utiliser le fichier cmd_to_learn.md pour avoir la liste des commandes utilisables durant ce tp.

## Etape 1
Afin de rendre les acces plus correct, nous allons renforcer la securité du village. Nous allons créer des groupes et des users.

 - Creation des groupes et users Ynov_campus
 - Changement des users/groupes du village
 - Passage du folder en mode recursif avec la restriction suivante:
   - le users peut lire, executer et ecrire.
   - le groups peut lire et executer.
   - les autres ne peuvent rien faire.
 - Passage de tout les fichier avec la restriction suivante:
   - le users peut lire et ecrire.
   - le groups peut lire et ecrire.
   - les autres ne peuvent rien faire.

## Etape 2
Nous allons créer les users & groups associé au batiment des villages. Quand on va devoir ajouter un groupe ou un user.
Pour simplifier les choses, on va créer le groupe et le user à chaque fois.
Les object doivent appartenir au batiment dans lesquels ils sont.
Les fichiers .personnages doivent appartenir à leurs propre user/group.
Les maisons doivent appartenir à leurs propriétaire

   - Creation des groupes Boulangerie, Mairie, Archive
   - Creation des users Boulanger, Vendeur, Maire, Assistant

## Etape 3
Nous allons copier le village Ynov_campus pour créer ynov_alt.

   - Creation des groupes Boulangerie, Mairie, Archive en suffixant par _alt
   - Creation des users Boulanger, Vendeur, Maire, Assistant en suffixant par _alt

🔑 N'oubliez pas le registre !
