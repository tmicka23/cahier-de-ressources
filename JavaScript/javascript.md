**[Accueil](/README.md)** | **[Liste des technologies](/cahier.md)**

# ES6 +
Rappel des spécificités de ES6+ pour JavaScript.

### Les Classes
La création de classe permet de simplement créer de nouvelles instances (= nouvel Objet) à partir de cette classe et grâce à son constructor. On peut créer aussi une nouvelle classe à partir de cette classe, qui contient tous les attributs et méthodes de la classe parente. On peut lui définir de nouvelles méthodes ou nouveaux attributs ou surcharger des méthodes existantes.

Création d'une classe
```
class Person {
   constructor(name) {
       this.name = name;
   }
   sayHello() {
       console.log(`Hello, my name is ${this.name}`)
   }
}
```

Création d'nue nouvelle instance à partir de la classe Person avec appel de la méthode définie dans Person
```
const pedro = new Person("Pedro");
pedro.sayHello();
```

Création d'une classe qui hérite de Person, et surcharge ses méthodes
```
class Students extends Person {
  constructor (name, school) {
    // Calls the Person constructor
    super(name);
    this.school = school;
  }

  //surcharge la méthode de Person
  sayHello() {
    console.log(`Hello, my name is ${this.name} and I am a student !`);
  }

  displaySchool() {
    console.log(`My school is ${this.school}`);
  }

}
```

### Les fonction flechées
Elles permettent d'alléger l'écriture des fonctions.

Déclaration classique
```
function nameFunction (params) {
  // votre code ici
  return (optionnel, interrompt l'execution de la fonction)
}
```

Ecritures des fonctions flechées
```
// écriture basique
(param1, param2) => { /* bloc */ }

// Parenthèses non nécessaires si un seul argument
param1 => { /* bloc */ }

// Si aucun paramètres, parenthèses vides
() => { /* bloc */ }

// “return” implicite si une seule ligne d’instruction
(a, b) => a + b;
// équivalent à
(a, b) => { return a + b }

// retourner un objet avec un return implicite :
() => ({prop1: "value1", prop2: "value2"})
```

### Syntaxe de décomposition
La syntaxe de décomposition permet d’affecter des propriétés d’un tableau ou d’un objet à des variables en utilisant une syntaxe semblable aux littéraux de tableaux ou aux littéraux objets.

Par exemple, sans l'affectation par décompostion, accéder aux élément d'un tableau se ferait de la manière suivante:
```
var premier = unTableau[0];
var deuxième = unTableau[1];
var troisième = unTableau[2];
```
Avec la syntaxe de décomposition cela se fait de la manière suivante:
```
var [premier, deuxième, troisième] = unTableau;
```

### Spread Operator
