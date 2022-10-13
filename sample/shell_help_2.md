# Aide globale

## git

``git`` est un gestionnaire de code, vous devez connaître ces commandes basiques

````Shell
git status  # Permet de voir l'etat de son git local

git add # Permet d'ajouter des fichiers

git rm # Permet d'enlever des fichiers

git commit  # Permet de créer le commit

git fetch # Permet de sync le remote

git pull # Permet de récuperer les sources

git merge # Permet de faire converger deux historiques

git diff # Permet d'afficher le delta

git rebase # Permet de remettre ces commits au dessus de l'historiue

git remote # Permet de gerer les remotes
````

## Bot ansible
Pour installer ansible ```pip install ansible```

Vous devez modifier une variable dans ``ansible/group_vars/all/all.yml`` pour que cela soit correct. Le script est basé pour etre lancé dans /home/ynov/**votre_repo_git**.

Dans le fichier yaml, de mon example, le nom de mon repo git est **example**, donc il va falloir le modifier avec le nom de votre repo.
````YAML
village_path: /home/ynov/example
````

Pour lancer le playbook ``ansible-playbook exo_1.yml --diff -vv`` le ``--diff`` permet d'afficher les différences, et le ``-vv`` permet d'augmenter la verbosité.


## Aide generique

Il existe toujours 2 moyens sur un os pour avoir de l'aide sur une commande

``man pwd`` qui donnera une aide complete et globale. Elle est pratiquement toujours disponible

``pwd --help`` qui donnera une aide partielle sur la commande pwd. Il est possible d'avoir besoin sur certaine commande de passer un argument pour ensuite avoir l'aide. Je n'ai pas d'exemple en tete, mais ça donnerait ceci.

``chia status --help``. Ces deux méthodes ne sont pas forcément disponibles.

## Temps

Je vais vous parler ici de deux commande permettant de gerer le temps sous linux.

``date`` & ``time``

## Ecire du texte

Vous connaissez tous echo, qui permet d'écrire quelque part, mais ce n'est pas la seule commande.

``write`` permet de brodcast des messages d'un user à l'autre sur des tty
``printf`` est le meme binaire que la libc, et permet une extension en varags illimité
``> >> |`` sont des opérateurs shell, ils vont vous permettre de rediriger le flux de donnée d'une commande vers une autre ou de la faire sortir.
Il en existe bien d'autre...

`````shell
ls

ls > test
pwd > test

ls >> test

cat test

cat test | grep ynov
`````

## Gestion des process

### Visualiser les process
``Htop`` est un utilitaire avancé de ``top``. Les deux permettent la meme chose, mais un à une interface graphique et pas l'autre.

Ces deux utilitaires vont vous permettre de visualiser vos process en plus des perfs de votre os.

Vous pouvez aussi bien le faire avec ``ps``, la commande dedié au processus.

### Kill un process

Il existe un outillage pour le faire, c'est la serie des kills, ``kill``, ``pkill``, ``kilall``...
Tous permettent de kill des process mais pas de la meme maniere (par pid, nom, groupe etc).

Htop permet aussi de kill un process.


### Background de process

Toutes commandes linux peut etre mise en background avec l'opérateur ``&``
``Shell
ls -R &
``

C'est aussi possible de le faire avec ``nohup`` ou ``tmux``

Une fois les process en place, vous pouvez toujours les switcher en background ou foreground avec ``bg`` ou ``fg``

Attention cependant lors des process, un process mal fait va devenir un zombie et ralentir votre system.



## Le service linux

Sur les distro récente, systemd gère les daemons.

On peut voir la liste des services avec ````systemctl````

Pour voir l'etat d'un process ````systemctl status sshd````, pour le stop, start, restart ``systemctl stop|start|restart sshd``

Par default, les logs d'un service est dans /var/log/message (sur centos) /var/log/syslog sur debian (je crois). Mais un service peut logger ou bon lui semble en fonction de sa configuration et de son exec


## Creer une library shell

Cela permet de créer une librairie avec des fonctions et de les appellers dans votre code.

````SHELL

#!/bin/bash

UselessFunction() {
    pwd
}

UselessFunctionWithParameter() {
    echo "$1"
}
````

Voici votre lib, sauvegarder la en my_lib.sh et ensuite un fichier shell

````Shell
#!/bin/bash

.  /home/ynov/my_lib.sh # . = source

UselessFunction

UselessFunctionWithParameter "Random_text"

````