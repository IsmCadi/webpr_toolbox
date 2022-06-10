# Woche 2 - 02.03.22

## Funktionen
### Allgemein
Kleiner Console exkurs.
```javascript
console.log("Hi, WebPr");
VM254:1 Hi, WebPr
undefined
consr x = 1
VM282:1 Uncaught SyntaxError: Unexpected identifier
const x = 1
undefined
49f4ae1f-2a73-47c0-91d3-565097f0a5cd:1          Failed to load resource: the server responded with a status of 504 ()
console.log("x", x, 1, "asdsaf")
VM529:1 x 1 1 asdsaf
undefined
console.warn("x", x, 1, "asdsaf")
VM598:1 x 1 1 asdsaf
(anonymous) @ VM598:1
undefined
console.error("x", x, 1, "asdsaf")
VM651:1 x 1 1 asdsaf
(anonymous) @ VM651:1
undefined
console.log([1,2,3])
VM779:1 (3) [1, 2, 3]
undefined
console.dir([1,2,3])
VM812:1 Array(3)
console.dir([ {a:1,y:2}
undefined

```
Meine Lösung zu der Programmieraufgabe wobei mit der Funktion "id"
der Wert x ohne Veränderung zurückgegeben wird.
```javascript
function id(x){
    return x;
}
constx_=Math.random();
document.writeln(id(x_)===x_)

```
Meine Lösung zur zweiten Programmieraufgabe mit currying, wobei zwei Variablen
übergeben und in der Funktion addiert werden.
```javascript
const plus = x => y => x+y;

const x_=Math.random();
const y_=Math.random();
const plus3=plus(3);
document.writeln(plus(x_)(y_)===x_+y_&&plus3(y_)===y_+3);

```

### Zur Snake Lösung
Die Schlange erzeugt den Kopf neu und löscht das letzte Glied.
Damit ist die Aufgabe leichter zu Programmieren.

###Scopes
Es gibt inherent nur zwei Arten von Scope. ( Es gibt immer einen globalen Scope)
Im Web wäre jenes das Window sobald wir wa Global definieren. 
- Utner der ID wird ein Eintrag im Window gemacht.
- Falls Scopenicht angegeben wird wird "this...." angenommen und dies wären dann (window....)
- Funktion gibt uns eine weitere Variante eines Scopes. Den Funktionsscope.
- Sie sind immer lokal zur umgebenden Funktion, egal wo definiert.
```javascript

```

###Variables
Die zwei legitimen möglichkeiten um eine Variable anzulegen wären:
- ~~- x = ...       mutable, global scope~~
- ~~var x = ..    mutable, "hoisted" scope~~
- let x = ...   mutable, local scope
- const x = ... immutable*, local scope

```javascript

```

###IIFE
Funktion wird definiert und auch gleich wieder aufgerufen.
Referenz nicht gleich Aufruf einer Funktion.
- Umwandung in einen Ausdruck mit "()"
- () immediatel inkvoked function expression nennt man die klammer direkt nach einer Funktion.
```javascript
function foo() {...}; foo()
(function foo() {..})()

```

Man kann schlussendlich sogar den namen der Funktion weglassen.
```javascript
(function (){...})()
```
Dies kann weiter ausgebaut werden und entspricht dem IIFE !
```javascript
( () => {...}) ()
```

###Lambda
Alpha Translation notation im lamba statt x => x, x.x
```javascript
const id = x => x //Ausdruck namens id
const id = y => y

x(1) -> x.1

```
Beta Reduktion heisst soviel wie Reduktionsaufruf.

```javascript

```

- Eta Reduktion standartoperation eines linearen operators!
- Bzw. kürzen der curry zuweisung.
- Üblich ist die Reduktion es ist aber auch eine Expansion möglich!
- Alle Umformungen sind sieteneffeckt frei und hängen an nichts ab und sind zeitunabhängig.