
# Exercice 1. Variables d’environnement



1- <b>_1. Dans quels dossiers bash trouve-t-il les commandes tapées par l’utilisateur ?_</b>

on tappe la commande `printenv PATH` et on a ce chemin comme résultat `/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin
:/bin:/usr/games:/usr/local/games:/snap/bin`

2- <b>_1.Quelle variable d’environnement permet à la commande cd tapée sans argument de vous ramener dans
votre répertoire personnel ?_</b>

la variable d'environnement est la suivante : `$HOME`

3- <b> Explicitez le rôle des variables LANG, PWD, OLDPWD, SHELL et _.</b>

la variable d’environnement LANG détermine la langue que les logiciels utilisent pour communiquer avec l’utilisateur
la variable d'environnement PWD contient le répertoire de travail courant de l'interpréteur de commande.
la variable d'environnement OLDPWD contient le chemin absolu vers le répertoire courant précédent
la variable d'environnement SHELL indique l'interpréteur shell utilisé par défaut, ici c'est /bin/bash 
