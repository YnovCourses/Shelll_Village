# Aide globale

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
