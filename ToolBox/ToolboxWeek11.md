# Woche 10 - 25.05.22

##How to work with map and filter
```javascript
[0,1,2,3,4].map( it => it * 2);
//mehrere parameter ausnutzen
[0,1,2,3,4].map( (it , index ) => it + index);

// aktuelles element und den index kann damit in einem mapping verwendet werden
const other = ["null", "eins", "zwei"];
[0,1,2].map( (it , index ) => other[index] + ":" + it.toString() );
//filter ungrad
[0,1,2].filter(it % 2 === 1 );
//filter grad
[0,1,2].filter(it % 2 === 0 );
//mit element und index filtern
[0,1,2].filter((it, index) => it % 2 === 1 );
//filter and reduce summe über ungrad zahligen indizes = 1
[0,1,2].filter((it, index) => it % 2 === 1 ).reduce((acc, cur) => acc + cur, 0);

//summe der ungrade zahlne aufzählen  =quadratzahlen

//is false
[0,1,2,3,4,5,6,7,8,9,10,11,12].every(it => it < 12);
```