# Prise en main de l’interpréteur de commandes

## Manuel

1- _A l’aide du manuel, identifiez le rôle de la commande which_

Pour identifier le rôle de la commande which a l'aide du manuel, j'ai effectué la commande suivante :
`man which` 
Celà m'a alors dis que cette commande sert a localiser une commande 

2- _Quand on consulte cette page, comment peut-on rechercher, par exemple, le mot option_ ?
 
Pour rechercher le mot option lorsqu'on consulte cette page il suffit de faire la commande suivante : `/option` on aura alors en surbrillance toute les fois où apparait le mot option 

3- _Comment quitte-t-on le manuel_ ?

Pour quitter le manuel il faut appuyer sur la touche q 

4- _Chaque section du manuel a une première page, qui présente le contenu de la section. Afficher la
première page de la section 6 ; de quoi parle cette section ?_

Pour afficher la première page de la section 6 j'ai effectué la commande suivante : `man 6 intro`
Cette section parle des jeux et des programmes disponnible sur le système 

## Navigation dans l’arborescence des fichiers

1- _allez dans le dossier /var/log_
`cd /var/log` 

2- _remontez dans le dossier parent (/var) en utilisant un chemin relatif

`cd ..`

3- _retournez dans le dossier personnel

`cd`

4- _revenez au dossier précédent (/var)

`cd -`

5- _essayez d’accéder au dossier /root ; que se passe-t-il ?

Lorsque je fait `cd /root` j'ai l'erreur "Permission Denied" c'est a dire que je n'ai pas les droits

6-  _essayez la commande sudo cd /root ; que se passe-t-il ? Expliquez

ça ne marche pas car en mode sudo je ne peux pas utiliser les commandes du shell (cd)

7-  _à partir de votre dossier personnel, créez l’arborescence suivante :

`mkdir dossier1` <br> `mkdir dossier2` <br> `cd dossier2` `mkdir dossier2.1` `mkdir dossier 2.2` <br> `cd dossier2.2` `touch fichier2` `touch fichier3` <br> `cd /dossier1` `touch fichier1`

8-  _revenez dans votre dossier personnel ; à l’aide de la commande rm, essayez de supprimer Fichier1, puis
Dossier1 ; que se passe-t-il ?

9-  _quelle commande permet de supprimer un dossier ?

10- 
