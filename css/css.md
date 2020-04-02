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


## Flexbox

### Les propriétés flexbox

* flex-direction(#### flex-direction)
* flex-wrap(#flex-wrap)
* flex-flow(#flex-flow)
* justify-content(#justify-content)
* align-items(#align-items)

#### flex-direction

La propriété ```flex-direction``` définit la direction dans laquelle le conteneur veut aligner ses éléments enfants

Elle peut accepter 4 valeurs : 
* ```flex-direction: row;``` (par défaut)
* ```flex-direction: row-reverse;```
* ```flex-direction: column;```
* ```flex-direction: column-reverse;```






### Centrer Horizontalement un enfant dans son parent

**HTML**

```
<div class="parent">
	<p class="enfant">
		Je suis centré horizontalement
	</p>
</div>
```

**CSS**

```
.parent {
	width:300px;
	height:200px;
	background-color:black;
	color:white;
	display:flex;
	justify-content:center;
}
```

### Centrer Verticalement un enfant dans son parent

**HTML**

```
<div class="parent">
	<p class="enfant">
		Je suis centré verticalement
	</p>
</div>
```

**CSS** 

```
.parent {
	width:300px;
	height:200px;
	background-color:black;
	color:white;
	display:flex;
	align-items:center;
}
```

### Centrer Horizontalement et verticalement un enfant dans son parent

**HTML**

```
<div class="parent">
	<p class="enfant">
		Je suis centré horizontalement et verticalement
	</p>
</div>
```

**CSS** 

```
.parent {
	width:300px;
	height:200px;
	background-color:black;
	color:white;
	display:flex;
	align-items:center;
	justify-content:center;
}
```