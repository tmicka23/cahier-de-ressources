**[Accueil](/README.md)** | **[Liste des technologies](/cahier.md)**

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
```shell
$ cd Documents/
$ ls
Dossier
```
- `pwd`: Afficher le repertoire actuel
```shell
$ cd Documents/
$ pwd
/home/utilisateur/Document
```
- `man [commande]` : Afficher la documentation d'une commande. RTFM !!
- `mkdir` : Créer un dossier
- `rmdir` : Supprimer un dossier vide
- `mv ` : Déplacer un fichier (peut aussi servir à renommer)
```shell
$ mv /chemin/source/fichier /chemin/destination/fichier
```
- `touch`: Créer un fichier
```shell
$ touch nom_du_fichier.txt
$ touch /chemin/source/nom_du_fichier.txt
```
- `cp` : Copier un fichier
```shell
$ cp fichier_a_copier.txt /chemin/source/
```
- `cat`: Afficher le contenu d’un fichier texte en intégralité
- `wc` : Compter les lignes, les mots et les caractères
```shell
$ wc -l languages.txt
50
```
- `sort` : Classer par ordre alphabétique
```shell
$ sort languages.txt
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
