

# UNIX / LINUX

## C'est quoi ?

Linux est un système d'exploitation (Operating System : OS) qui a la particularité d'être **libre**, c'est-à-dire que son code source est **ouvert** : tout le monde peut le consulter. L’environnement UNIX constitue un élément important du développement d’internet.

## Commandes de base

- `cd` : Changer de répertoire
```shell
$ cd ..
$ cd Documents/Dossier/
```
- `ls` : Lister les fichiers dans un répertoire
- `ls -l` : Afficher les détails des fichiers
- `ls -a` : Afficher les fichiers cachés / qui commencent par un point
- `ls -l` : Afficher les fichiers avec les détails
```shell
$ cd Documents/
$ ls
Dossier
```
- `pwd`: Afficher le repertoire actuel (print working directory)
```shell
$ cd Documents/
$ pwd
/home/utilisateur/Document
```
- `man [commande]` : Afficher la documentation d'une commande. RTFM !!
- `mkdir` : Créer un dossier
-`mkdir -p`: Créer un dossier et sous-dossier
```shell
$ mkdir -p quetes/legumes-fruits/fruits
```
- `rm` : Supprimer un fichier
- `rmdir` : Supprimer un dossier vide
- `rmdir -r`: Supprimer un dossier récursivement (avec tous les dossiers et fichiers qu'il contient
- `mv ` : Déplacer un fichier (peut aussi servir à renommer)
```shell
$ mv /chemin/source/fichier /chemin/destination/fichier
$ mv fichier1 fichier2
$ mv fichier1 truc
```
- `touch`: Créer un fichier
```shell
$ touch nom_du_fichier.txt
$ touch /chemin/source/nom_du_fichier.txt
```
- `cp` : Copier un/des fichier(s)
```shell
$ cp fichier_a_copier.txt /chemin/source/
$ cp fichier_source1    fichier_source2    fichier_destination
```
- `cp -R`  : Copier un/des dossier(s)
```shell
$ cp dossier_source1    dossier_source2    dossier_destination
```

- `>`: stocker le résultat d'une commande dans un fichier spécifié par la suite
```shell
$ echo "Je suis moisi" > vieuxtacos.txt
```
- `>>`: stocker le résultat d'une commande mais en ajoutant du contenu

- `cat`: Afficher le contenu d’un fichier texte en intégralité
- `wc` : Compter les lignes, les mots et les caractères
```shell
$ wc -l languages.txt
50

$ wc languages.text
```
- `sort` : Classer par ordre alphabétique
```shell
$ sort languages.txt
$ cat Swedish.csv Danish.csv Norwegian.csv | sort -u
```
- `grep` : Rechercher une chaine de caractère dans un fichier (attention aux majuscules !!)
```shell
$ grep "France,2019,PHP" fichier.csv
```
- `history` : Afficher l'historique du terminal
- `clear` : Effacer le contenu du terminal
- `head` : Afficher les premières lignes d'un fichier
- `tail` : Afficher les dernières lignes d'un fichier
- `find` : Rechercher un fichier ou répertoire
```shell
 $ find /chemin/ -type [f|d] -iname "pattern" où f=file et d=répertoire, pattern = le schéma de recherche => par exemple : *data* pour tous les fichiers contenant la suite de caractère data.
 ```
 
## La commande sudo
Exécuter une ligne de commande en mode super utilisateur
```shell
$ sudo <commande> : Exécuter la commande suivante en tant qu'admin.
```

## Trier / Filtrer / Rediriger
- `|` : Pipe, redirige la sortie d'une commande, afin de l'utiliser comme entrée
- `<` : Modifier l'entrée
- `>` : Modifier la sortie
```shell
 $ ls ~ > home-contents.txt
le résultat de ls ~ a été écrit dans le fichier home-contents.txt
 ```
- `>>` : Ajoute la sortie à la suite de l'existant dans un fichier
- `dev/null` : "périphérique nul" (pseudo-périphérique qui ne garde pas les données)
```shell
 $ ls / > /dev/null
 $ > /dev/null
 ```

## Exemples pratiques
## Exemple 1:
Fichier Prenoms.csv avec utilisateur;genre;nationalité:

    aaliyah;f;english (modern);0
    aapeli;m;finnish;0
    aapo;m;finnish;0
    aaren;m,f;english;0
    aarne;m;finnish;0
    
 Compter le nombre de prénoms féminins et finlandais, voici ce qu'on écrira :
```shell
 $ grep "f;french" <  Prenoms.csv |  wc -l
 ```
Prenoms.csv est redirigé vers grep (<) où l’on ne va garder que le genre féminin et la nationalité french("f;french") . Tout cela est ensuite redirigé comme entrée ( | ) vers wc – l qui va en sortie nous donner le décompte.

## Exemple 2:
```shell
 $ grep swedish Prenoms.csv > Swedish.csv
 Filtre Prenoms.csv avec le critère swedish et renvoie ça vers un fichier Swedish.csv
 ```
 
## Exemple 3:
Créer un fichier php_france_2019.csv contenant uniquement le nombre de wilders ayant fait du PHP, sur un campus en France, en 2019, à partir d’un fichier wilders.csv
```shell
 $  grep "France,2019,PHP"< wilders.csv | w -l  >  php_france_2019.csv
 ```

## Exemple 4:

Créer un fichier javascript_biarritz_toulouse.csv contenant uniquement les wilders ayant fait du JavaScript, sur les campus de Toulouse et Biarritz. 
Indice : tu peux avoir besoin de créer des fichiers "intermédiaires", et de les concaténer.

```shell
 $  	grep Toulouse wilders.csv > toulouse.csv  
 $	grep JavaScript toulouse.csv > javascript_biarritz_toulouse.csv
 $	grep Biarritz wilders.csv > biarritz.csv
 $	grep JavaScript biarritz.csv >> javascript_biarritz_toulouse.csv
 ```


