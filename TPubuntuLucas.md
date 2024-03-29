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

`rm -rf dossier2` 

## Commandes importantes 

1- <b>_Quelle commande permet d’afficher l’heure ? A quoi sert la commande time ?_</b>

la commande qui permet d'afficher l'heure est la commande : `date` <br> la commande `time` sert à determiner le temps d'execution d'une commande choisie. 


2- <b>_Dans votre dossier personnel, tapez successivement les commandes ls puis la ; que peut-on en déduire
sur les fichiers commençant par un point ?_</b>

On peut en déduire que les fichiers commençant par un point sont des fichiers cachés 

3- <b>_Où se situe le programme ls ?_</b>

J'ai effectué la commande `which ls` et j'ai eu l'arborescence suivante : `/usr/bin/ls` 

4- <b>_Que fait la commande ll ? (indice : la commande alias peut vous aider)_</b>

la commande ll affiche toutes les informations des fichiers et des dossiers 

5- <b>_Quelle commande permet d’afficher les fichiers contenus dans le dossier /bin ?_</b>

La commande qui permet d'afficher cela est : `ls /bin`

6- <b>_Que fait la commande ls .. ?_</b>

La commande ls permet d'obtenir la liste et les caractéristiques des fichiers contenus dans un répertoire.

7- <b>_Quelle commande donne le chemin complet du dossier courant ?_</b>

`pwd`

8- <b>_Que fait la commande echo 'yo' > plop exécutée 2 fois ?_</b>

Elle créee un fichier nommé plop avec écrit à l'interieur yo et re efface et le refait 

9- <b>_ Que fait la commande echo 'yo' >> plop exécutée 2 fois ?_</b> 

Elle créee un fichier nommé plop avec écrit à l'interieur yo et la deuxième execution ne recrée pas le fichier mais rajoute un yo a la suite 

10- <b>_A quoi sert la commande file ? Essayez la sur des fichiers de types différents_ </b>

file permet de déterminer le type d'un fichier 

11- <b>_Créez un fichier toto qui contient la chaîne Hello Toto ! ; créer ensuite un lien titi vers ce fichier
avec la commande ln toto titi. Modifiez à présent le contenu de toto et affichez le contenu de titi :
qu’observe-t-on ? Supprimez le fichier toto ; quelle conséquence cela a-t-il sur titi ?_</b>

Lorsqu'on a modifié le contenu de toto cela a modifier le contenue de titi cependant lorsqu'on supprime le fichier toto le fichier titi 
reste présent

correction prof : La modification affecte les deux fichiers (ils sont liés) ; après suppression de toto, titi
permet encore d’accéder au fichier car c’est un lien physique

12- <b>_Créez à présent un lien symbolique tutu sur titi avec la commande ln -s titi tutu. Modifiez le
contenu de titi ; quelle conséquence pour tutu ? Et inversement ? Supprimez le fichier titi ; quelle
conséquence cela a-t-il sur tutu ?_</b>

La supression de l'un entraine la supression de l'autre 

correction prof : La modification affecte les deux fichiers (ils sont liés) ; après suppression de titi, tutu ne
permet plus d’accéder au fichier car c’est un lien symbolique

13- <b>_Affichez à l’écran le fichier /var/log/syslog. Quels raccourcis clavier permettent d’interrompre et
reprendre le défilement à l’écran ?_</b>

La touche arrêt défil permet d'interrompre et reprendre le défilement a l'écran 

correction prof : cat /var/log/syslog ; CTRL + S ; CTRL + Q


14- <b>_Affichez les 5 premières lignes du fichier /var/log/syslog, puis les 15 dernières, puis seulement les
lignes 10 à 20._</b>

j'utilise la commande `head -5 /var/log/syslog` pour les 5 première lignes du fichier 
la commande `tail -15 /var/log/syslog` pour les 15 dernières lignes et `head -n 10 25 /var/log/syslog` pour les lignes 10 à 20

correction prof : head -5 /var/log/syslog ; tail -15 /var/log/syslog ; head -20 /var/log/syslog | tail -11


15- <b>_Que fait la commande dmesg | less ?_</b>

Elle affiche en une seule page les informations du noyau 

correction prof : Affiche page par page les messages émis par le noyau


16- <b>_Affichez à l’écran le fichier /etc/passwd ; que contient-il ? Quelle commande permet d’afficher la page
de manuel de ce fichier ?_</b>

j'ai fait `cat /etc/passwd/`,  il contient différentes informations sur les comptes utilisateurs. 

correction prof : contient les mots de passe et autres informations sur les utilisateurs

La commande qui permet d'afficher la page de manuel est `man 5 passwd` 

17- <b>_Affichez seulement la première colonne triée par ordre alphabétique inverse_</b>


`sort -r: +1 /etc/passwd` 

correction prof cut -d: -f1 /etc/passwd | sort -r



18- <b>_Quelle commande nous donne le nombre d’utilisateurs ?_</b>

`who` correction prof : `wc -l /etc/passwd` (compte le nombre de lignes du fichier /etc/passwd et donc le nombre
d’utilisateurs

19- <b>_Combien de pages de manuel comportent le mot-clé conversion dans leur description ?_</b>

j'ai fait `man -k conversion  | wc -l ` je vois qu'il y'a 4 résultats

20- <b>_A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine_</b>

`find -name "passwd"` 

21-<b> _Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier
~/list_passwd_files.txt et que les erreurs soient redirigées vers le fichier spécial /dev/null_</b>

`find / -name passwd 1> ~/list_passwd_files.txt 2> /dev/null`


22- <b>_Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini l’alias ll vu
précédemment_</b>

`grep -r "alias ll" .`


23- <b>_Utilisez la commande locate pour trouver le fichier history.log._</b>

`locate history.log` il se situe donc dans /var/log/apt

24- <b>_Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il ? Pourquoi ?_</b>

Non il n'apparait pas car la commande locate recherche dans une base de données et non pas sur notre disque dur, le fichier n'est donc pas repertorié dans la base de données (Elle est mise a jour une fois par jour) 








