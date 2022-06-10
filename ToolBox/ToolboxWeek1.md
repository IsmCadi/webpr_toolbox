# Woche 1 - 23.02.22

## Funktionen
### Allgemein
Die oberflächlichen Ähnlichkeit überdecken die Unterschiede zwischen java und javascript.
Der Strichpunkt ist ein Statement Terminartor in JavaScript uns sollte in solchen fällen gesetzt werden.
Grundsäzlich sollten Statements und Anweisung mit einem Strichpunkt beenden.
Die Fehlermeldung "undefined ist not a function" gibt’s grundsätzlich in javascript, aber nicht zur GLEICHEN Zeit in java.
Die Sprache ist für die Automatisiereng im Browser zur Laufzeit definiert!

### Statement Terminator
Beispiele hierbei sind:
```javascript
        function fun1()    { return 1; }
        document.writeln( fun1()   === 1 );
        const noReturn2 = () => { 1; };
```
### Rückgabe des Wertes
- In javascript muss das return definiert werden!
- Return ist eine direktive mit einem Return statement :
```javascript
        function one(x) {
            return x;
        }
```

### Funktionsdefinitionen
Fun1() ist ein eigenständiger ausdruck
Fun1() === 1 ist true !!
Fun11(42) === 1 würd ein java nicht compilieren aber in javascript wird kein Compilefehler erwartet da es keinen compiler gibt !!!
```javascript
        function noReturn()    { 1; }
        function fun1()    { return 1; }
```

Die Methode wird überschrieben wie eine variable bei fun2.
Die Referenz kann nur ein mal belegt werden also wird die letzte definition übernommen. Hierbai die zweite Zeile.
Die zweite Definition überschreibt grundsätzlich immer die erste definition!
```javascript
        function fun2()    { return 1; }
        function fun2(arg) { return arg; }
```

Bei "no return" wird ein false zurückgegeben ! Dabei ist der wert dort "undefined"

### Curried style

- Der Pfeil => ist eine Infix Notation
- {1} ist ein b`Block von Statements.
- Funktion nehmen und geben andere funktionen zurück. Im Beispiel wäre dies die Funktion doit2 die callme mit dem Argument zurückgibt.
- In welchem Fall macht das sin? Falls ich dynamisch Werte einfügen will
- Funktion mit Funktion und einen Wert mitgeben nennt man "curried style", werden in runden Klammern weitergegeben.
```javascript
        const doit2 = callme => arg => callme(arg) ;
```
Canvas = Leinwandelemente auf Html Basis