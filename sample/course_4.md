#  Utilisation shell avancé

Le but de cette séance est de vous faire découvrir/utiliser de nouvelle commandes shell.

## Réalisation d'un service linux

Le but de cet exercice est de créer un service linux (daemon), qui tourne tout le temps.
Ce dernier est surveillé par l'os lui meme. Le nom du service est ``my_trash``. Il doit être lancé au boot de l'os.

## Format du rendu

Vous allez devoir fournir un script shell sur cette organisation => https://github.com/orgs/YnovCourses/repositories.
Merci de créer un répertoire par étudiant ou groupe d'étudiants.

Le script shell `create_trash_service.sh` doit est le point d'entré du programme.


## Réalisation d'une corbeille
le but de se service est supprimer le contenu du répertoire /trash en respectant les conditions suivante

- les fichiers doivent etre vieux d'au moins 2 jours ainsi que son contenu
- les repertoire doivent être vide
- Si un fichier est supérieur à 200Mo, il doit etre supprimé directement
- Si le fichier vient de /tmp, il est supprimé directement
- Si le fichier vient de root:root, il faut une commande spécial pour le supprimer

## Actionnement
La commande rm doit etre aliassé pour mettre le tout dans la corbeille
La commande my_trash doit etre crée et permet de lancer la corbeille
Le shell du service doit etre une boucle infinie qui verifie la corbeille toutes les heures.
La commande my_trash et l'allias doivent etre chargé pour le user à la connexion
Vous ne devez pas gerer le fait de supprimer plusieurs fichier en meme temps avec la commande rm.

## Bonus
- service de type fork
- log dans /var/log/my_trash
- filesystem dedié pour les logs
- La commande my_trash et l'allias sont chargé pour tout user, root compris
