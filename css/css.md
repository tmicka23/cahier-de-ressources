**[Accueil](../README.md)** | **[Liste des technologies](../cahier.md)**

# Liste des ressources sur CSS 

### [Documentation Officielle](https://developer.mozilla.org/fr/docs/Web/CSS)

## Cours sur CSS

* [Grafikart](https://www.grafikart.fr/formations/css)
* [CodeCademy](https://www.codecademy.com/learn/learn-css)
* OpenClassroom
    * [niveau débutant](https://openclassrooms.com/fr/courses/1603881-apprenez-a-creer-votre-site-web-avec-html5-et-css3)
    * [niveau intermédiaire](https://openclassrooms.com/fr/courses/5919246-creez-des-animations-css-modernes)
    * [niveau avancé](https://openclassrooms.com/fr/courses/2745636-utilisez-les-effets-avances-de-css-sur-votre-site)
* Flexbox Froggy 
	* [S'entrainer sur Flexbox](https://flexboxfroggy.com/#fr)


## Autour de CSS

* **Les Frameworks**
    * [Bootstrap](frameworks/bootstrap.md)
    * [Foundation](frameworks/foundation.md)
    * [Materialize](frameworks/materialize.md)
    * [Bulma](frameworks/bulma.md)
    * [Buddy](https://buddycss.com)
* **Les préprocesseurs**
    * [Sass](preprocesseurs/sass.md)
    * [Less](preprocesseurs/less.md)
    * [Compass](preprocesseurs/compass.md)
    * [Stylus](preprocesseurs/stylus.md)
* **Outils**
	* Check my CSS(http://csslint.net/)

# Cheat Sheet

## Appeler un fichier CSS

3 façons de faire : 

* Inline (à proscrire)

Il est possible de rédiger du CSS directement dans un fichier HTML à l'aide de l'attribut style, placé dans une balise HTML.

Exemple :

```<div style="color:blue;font-size:28px;">Lorem Ipsum</div>```

* Entre des balises ```<style>``` (à proscrire)

Placée dans le ```<head>```, la balise ```<style>``` permet également d'intégrer du CSS dans un fichier HTML

* Dans un fichier CSS externe

Il est fortement conseillé de rédiger son CSS dans un fichier séparé. Une fois fait, il devra être appelé dans le head du document html afin de l'appliquer à la page.

Pour ce faire, utiliser la balise ```<link>``` de la manière suivante : 

```
<link rel="stylesheet" type="text/css" href="style.css">
```

Bien penser à spécifier correctement le chemin vers le fichier CSS. S'il est dans le même dossier que le fichier HTML, il s'uffit d'écrire son nom. S'il se trouve dans un dossier enfant, spécifier comme suit : 

```
<link rel="stylesheet" type="text/css" href="/mon-dossier/style.css">
```

## Les sélecteurs CSS

Il existe en CSS trois moyens de définir un style à un élément : 
* Les balises
* Les classes
* Les ID

### Les balises

Il est possible d'assigner un style à des balises en spécifiant simplement leur nom : 

```
h1 {
	color:blue;
}
```

Dans cet exemple, toutes les balises ```<h1>``` seront de couleur bleue.

### Les classes

Il est possible d'assigner un style à des éléments en fonction de leur classe précisée dans l'attribut ```class="ma-classe"``` en ajoutant un **point** avant le nom de la classe : 

```
.ma-classe {
	background-color:green;
}
```

Dans cet exemple, tous les éléments ayant la classe **ma-classe** auront un background de couleur verte.

### Les ID

Il est enfin possible d'appliquer un style à des éléments en fonction de leur identifiant précisé dans l'attribut ```id="mon-id"``` en ajoutant un **dièse** avant le nom de l'identifiant : 

```
#mon-id {
	text-decoration:underline;
}
```

Dans cet exemple, l'élement ayant pour identifiant **mon-id** aura son texte souligné.



## Flexbox

### Les propriétés flexbox

* [flex-direction](####-Flex-direction)
* [flex-wrap](####-Flex-wrap)
* [flex-flow](####-Flex-flow)
* [justify-content](####-Justify-content)
* [align-items](####-Align-items)

#### Flex-direction

##### Définition

La propriété ```flex-direction``` définit la direction dans laquelle le conteneur veut aligner ses éléments enfants

Elle peut accepter 4 valeurs : 
* ```flex-direction: row;``` (par défaut) : les enfants s'aligneront en lignes
* ```flex-direction: row-reverse;``` : les enfants s'aligneront en lignes inversées
* ```flex-direction: column;``` : les enfants s'aligneront en colonnes
* ```flex-direction: column-reverse;``` : les enfants s'aligneront en colonnes inversées

[voir sur codepen](https://codepen.io/GCR/pen/poJBwrd?editors=1100)

#### Flex-wrap

##### Définition

La propriété ```flex-wrap``` définit si le parent alignera ses enfants sur une ou plusieurs lignes.

Elle peut accepter 3 valeurs : 
* ```flex-wrap: nowrap;``` (par défaut) : les enfants s'aligneront sur une seule ligne et peuvent donc déborder du parent
* ```flex-direction: wrap;``` : les enfants s'aligneront sur plusieurs lignes, de gauche à droite avec saut de ligne en cas de débordement 
* ```flex-direction: wrap-reverse;``` : les enfants s'ligneront sur plusieurs lignes de droite à gauche avec saut de ligne en cas de débordement

[voir sur codepen](https://codepen.io/GCR/pen/QWbPgJa)

#### Justify-content

##### Définition

La propriété ```justify-content``` définit l'alignement des enfants le long de l'axe principal.

Elle peut accepter 5 valeurs : 
* ```justify-content: flex-start;``` (par défaut) : les enfants sont regroupés en début de ligne
* ```justify-content: flex-end;``` : les enfants sont regroupés en fin de ligne
* ```justify-content: center;``` : les enfants sont centrés le long de la ligne
* ```justify-content: space-between;``` : les enfants sont répartis sur la ligne. Le premier enfant est donc collé contre le début de son parent et le dernier enfant contre la fin de son parent.
* ```justify-content: space-around;``` : les enfants sont repartis sur la ligne avec les mêmes marges autour de chacun

[voir sur codepen](https://codepen.io/GCR/pen/poJBwQV)

#### Align-items

##### Définition

La propriété ```align-items``` définit l'alignement des enfants le long de l'axe secondaire. 
Si ```flex-direction:row``` est utilisée, ```align-items``` alignera les enfants verticalement.
Si ```flex-direction:column``` est utilisée, ```align-items``` alignera les enfants horizontalement. 

Elle peut accepter 5 valeurs : 
* ```align-items: flex-start;``` : les enfants sont regroupés au début de l'axe secondaire
* ```align-items: flex-end;``` : les enfants sont regroupés à la fin de l'axe secondaire
* ```align-items: center;``` : les enfants sont centrés sur l'axe secondaire
* ```align-items: baseline;``` : les enfants sont répartis sur l'axe secondaire. Le premier enfant est donc collé contre le début de son parent et le dernier enfant contre la fin de son parent.
* ```align-items: stretch;``` (par défaut) : les enfants sont étirés jusqu'à remplir le parent (sauf si les dimensions de l'axe correspondant des enfants sont précisées)

[voir sur codepen](https://codepen.io/GCR/pen/NWqmvPy)
