# Aide globale 2

## Attention

- **on ne vous demande pas d'etre idempotent** vos script ne serons joué qu'une seule fois.
- pensez à clean vos os, voir meme à trash la vm et recommencer sur une vm vierge
- lisez bien les consignes, ce n'est pas parce qu'en france on ecris de gauche à droite et de bas en haut qu'il faut toujours executer les exos et les taches dans le meme sens

## builting bash

https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html#The-Set-Builtin


## processing bash

- &
  - c'est un fork classique
  - auto kill à la fermeture du terminal

```bash
for i in {1..100} ;
do
    ( ./my_script.py & )
done
```

- parallel
  - gestion du threading assez simple
````bash
parallel -j0 ./my_script.py ::: {1..100}
````

- nohup & tmux
  - gestion avancé du process
  - risque avancé de crash os en cas d'erreur

Certain process linux ont déja des options natives pour être lancé en background.