#  Utilisation shell avancé

Le but de cette séance est de vous faire découvrir/utiliser de nouvelles commandes shell.

## Rendu
Le script shell `check_shell.sh` doit est le point d'entré du programme.
Vous devez pour chaque tache afficher sur la meme ligne:
`le nom | sa durée d'execution` exemple  `ajouter votre nom dans le prompt linux | 0.0s` ( 0m0.229s est accepté)
Pour toutes taches s'appelant afficher, votre script doit fournir la valeur demandée.
`afficher le nombre de group avec gid impair | 100 | 0.0s`
La sortie attendue est sur stdout

## Creation d'un script au chrono.

Durant cet exercice, vous allez devoir réaliser un shell réalisant une suite d'action.
Vous serez noter sur le resultat du script ainsi que sur son temps d'execution.

Votre script va devoir

- afficher l'heure au format "00:00:00"
- afficher le nombre d'user avec un uid pair
- afficher le nombre de group avec gid impair
- afficher le nombre de fichier
- afficher le nombre de répertoire
- afficher la version du kernel
- afficher le nom du cpu
- ajouter votre nom dans le prompt linux
- afficher les variables d'environnment
- créer le fichier random_text
- ecrire dans random_text au moins 46076442 charactere
- afficher la taille du fichier en mode human_readeable
- afficher le nombre de ligne de la commande man man
- compter combien de fois le mot man est présent dans la commande man man
- cloner le repos grafana de github
- ajouter le fichier random_text dans le repo cloner
- récuperer ce fichier https://www.elastic.co/guide/en/elasticsearch/reference/8.4/release-notes-8.4.3.html
- récuperer ce fichier https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-8.4.3-darwin-x86_64.tar.gz
- Faire des 4 etapes precedentes un zip
- afficher le nom du physical volume
- afficher l'uuid du volume group
- afficher le path du lv root
- afficher le nombre de paquet perdu en ping 8.8.8.8
- afficher si le flux entre la machine est 8.8.8.8 sur le port 443 est ouvert
- faire passer un train
- afficher l'heure "00:00:00"

## bonus
- afficher en couleur
- ecrire dans un fichier nommé result.txt en plus du retour stdout


Vous allez devoir soutenir devant la classe votre script shell.