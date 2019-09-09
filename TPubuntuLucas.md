# Prise en main de l’interpréteur de commandes

## Manuel

1- <b>_A l’aide du manuel, identifiez le rôle de la commande which_</b>

Pour identifier le rôle de la commande which a l'aide du manuel, j'ai effectué la commande suivante :
`man which` 
Celà m'a alors dis que cette commande sert a localiser une commande 

2- <b>_Quand on consulte cette page, comment peut-on rechercher, par exemple, le mot option_ ?</b>
 
Pour rechercher le mot option lorsqu'on consulte cette page il suffit de faire la commande suivante : `/option` on aura alors en surbrillance toute les fois où apparait le mot option 

3- <b>_Comment quitte-t-on le manuel ?_</b>

Pour quitter le manuel il faut appuyer sur la touche q 

4- <b>_Chaque section du manuel a une première page, qui présente le contenu de la section. Afficher la
première page de la section 6 ; de quoi parle cette section ?_</b>

Pour afficher la première page de la section 6 j'ai effectué la commande suivante : `man 6 intro`
Cette section parle des jeux et des programmes disponnible sur le système 

## Navigation dans l’arborescence des fichiers

1- <b>_allez dans le dossier /var/log_</b>

`cd /var/log` 

2- <b>_remontez dans le dossier parent (/var) en utilisant un chemin relatif_</b>

`cd ..`

3- <b>_retournez dans le dossier personnel_</b>

`cd`

4- <b>_revenez au dossier précédent (/var)_</b>

`cd -`

5- <b>_essayez d’accéder au dossier /root ; que se passe-t-il ?_</b>

Lorsque je fait `cd /root` j'ai l'erreur "Permission Denied" c'est a dire que je n'ai pas les droits

6-  <b>_essayez la commande sudo cd /root ; que se passe-t-il ? Expliquez_</b>

ça ne marche pas car en mode sudo je ne peux pas utiliser les commandes du shell (cd)

7-  <b>_à partir de votre dossier personnel, créez l’arborescence suivante :_</b>

`mkdir dossier1` <br> `mkdir dossier2` <br> `cd dossier2` `mkdir dossier2.1` `mkdir dossier 2.2` <br> `cd dossier2.2` `touch fichier2` `touch fichier3` <br> `cd /dossier1` `touch fichier1`

8-  <b>_revenez dans votre dossier personnel ; à l’aide de la commande rm, essayez de supprimer Fichier1, puis
Dossier1 ; que se passe-t-il ?_</b>

Pour supprimer le Fichier1 j'effectue la commande suivante : `rm Dossier1/Fichier1`

la commande `rm Dossier1` a affiché une erreur _cannot remove Dossier1: Is a directory_
Il faut modifier la commande `rm` pour supprimer un dossier.



9-  <b>_quelle commande permet de supprimer un dossier ?_</b>

`rmdir`

10- <b>_que se passe-t-il quand on applique cette commande à Dossier2 ?_</b>

ça n'a pas supprimer dossier2 et donc accessoirement tout ce qu'il y'avait à l'interieur 

11- <b>_comment supprimer en une seule commande Dossier2 et son contenu ?_</b>

`rm -r dossier2` 

## Commandes importantes 

1- _Quelle commande permet d’afficher l’heure ? A quoi sert la commande time ?

la commande qui permet d'afficher l'heure est la commande : `date` <br> la commande `time` sert à determiner le temps d'execution d'une commande choisie. 


2- _Dans votre dossier personnel, tapez successivement les commandes ls puis la ; que peut-on en déduire
sur les fichiers commençant par un point ?

On peut en déduire que les fichiers commençant par un point sont des fichiers cachés 

3- _Où se situe le programme ls ?_

J'ai effectué la commande `which ls` et j'ai eu l'arborescence suivante : `/usr/bin/ls` 

4- _Que fait la commande ll ? (indice : la commande alias peut vous aider)_

la commande ll affiche toutes les informations des fichiers et des dossiers 

5- _Quelle commande permet d’afficher les fichiers contenus dans le dossier /bin ?_

La commande qui permet d'afficher cela est : `ls /bin`

6- _Que fait la commande ls .. ?_

La commande ls permet d'obtenir la liste et les caractéristiques des fichiers contenus dans un répertoire.

7- _Quelle commande donne le chemin complet du dossier courant ?_

`pwd`

8- _Que fait la commande echo 'yo' > plop exécutée 2 fois ?_

Elle créee un fichier nommé plop avec écrit à l'interieur yo 

9- _ Que fait la commande echo 'yo' >> plop exécutée 2 fois ?_ 

Elle créee un fichier nommé plop avec écrit à l'interieur yo et la deuxième execution ne recrée pas le fichier mais rajoute un yo a la suite 

10- _A quoi sert la commande file ? Essayez la sur des fichiers de types différents_ 

file permet de déterminer le type d'un fichier 




