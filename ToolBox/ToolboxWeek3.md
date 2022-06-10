# Woche 3 - 09.03.22

## Funktionen
### Allgemein
Strings sind immutable in javascript ! 

### Lambda Boolean Logic

Falls p true ist wird q ausgewertet was auch wieder true oder false sein kann.
Dies bezieht sich auf "and". Bei or wiederrum wird nur false herausgegeben falls q und p false sind.
Da selbe Prinzip von and kann umgedreht und auf not bezogen werden.
```javascript
const and   = p => q => p ( q ) ( p ) ;
const or    = p => q => p ( p ) ( q );
const not   = p => q => q ( q ) ( p );

```

Hierbei wird eine Funktion mit dem Funktionsscope definiert. Dabei kann niemand dran rumfummeln.
Für firstname und lastname wird einfach mit einem "konst" und "second" die jeweilige variable entnommen.
Somit kann man die vor und nachnamen seperat aufrufn und unterschieden
```javascript
const Pair = x => y => f =>  f(x)(y);


const firstname = x => y => x;
const lastname  = x => y => y;

const firstname = konst;
//const lastname  = snd;

const firstname = T;
const lastname  = F;
```

### Pair, Product Type
```javascript
const Pair = x => y => f => f(x)(y);
const fst = p => p(T);
const snd = p => p(F);

//Pair kann nicht zur laufzeit geändert werden.
lt a  = Pair(1),(2);
.
.
.
foo(a)
```

### Lambda Algebraic Datatypes
Siehe Test File:lambdaTest.js, Zeile 76.
```javascript
const Left   = x => f => g => f(x);
const Right  = x => f => g => g(x);
const either = e => f => g => e(f)(g); 
//eta reduction
const either = e => f  => e(f);
const either = id;
```