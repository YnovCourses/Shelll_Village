# Voici une toolbox bash pour vous.

## Doc linux debutant / global

https://www.tutorialspoint.com/unix/index.htm

## Les boucles en shell

https://www.cyberciti.biz/faq/bash-for-loop/
https://www.tutorialspoint.com/unix/unix-shell-loops.htm
https://www.tutorialspoint.com/unix/unix-loop-control.htm

## Les fonction en shell

https://www.tutorialspoint.com/unix/unix-shell-functions.htm

## les variables

https://www.tutorialspoint.com/unix/unix-using-variables.htm
https://www.tutorialspoint.com/unix/unix-special-variables.htm
https://www.tutorialspoint.com/unix/unix-using-arrays.htm
https://www.tutorialspoint.com/unix/unix-environment.htm

## L'échappement et les quotes

https://www.tutorialspoint.com/unix/unix-quoting-mechanisms.htm

## Redirection de shell 

https://www.tutorialspoint.com/unix/unix-io-redirections.htm

## Les conditions

https://www.tutorialspoint.com/unix/unix-decision-making.htm

## Les opérations

https://www.tutorialspoint.com/unix/unix-basic-operators.htm

## L'utilisation et l'interpretation de resultat de commandes.

https://www.tutorialspoint.com/unix/unix-pipes-filters.htm

Il est aussi possbile de récuperer le resultat d'une commande dans une variables.

`````SHELL
ls
my_ls=$(ls)
echo $my_ls


pwd
my_pwd=$(pwd)
echo $my_pwd


pwd | cut -d '/'  -f2 | wc -c
my_custom=$(pwd | cut -d '/'  -f2 | wc -c)
echo $my_custom

`````
va donner le resultat suivant.
````SHELL
[root@fedora ansible]# sh test.sh
 ansible.cfg   check_house_exo_2.yml   check_house.yml   exo_1.yml   exo_2.yml   exo_3.yml   group_vars   templates  '#test.sh#'   test.sh   test.sh~
ansible.cfg check_house_exo_2.yml check_house.yml exo_1.yml exo_2.yml exo_3.yml group_vars templates #test.sh# test.sh test.sh~
/home/ynov/Shelll_Village/ansible
/home/ynov/Shelll_Village/ansible
5
5

````

