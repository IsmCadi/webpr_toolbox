# Woche 4 - 16.03.22

```javascript
let = [1,2,3]
let x = [1,2,3]
[x, 4,5,6]
Mapping:
[... x, 4,5,6] -> [1,2,3,4,5,6]
```

Thema Partial Application
Ausnutzen für map, filter und reduce
Mindestens eingesetzt bei oop2

Map reduce 
map -> 1, 2 und 3
x => x*2
ergibt 2, 4 und 6

Durch eta reduktion kann man den rest rauskürzen !
Hier bilde ich alle zahlen im Array auf das doppelte ab
```javascript
const times = a => b => a*b;
cont twoTimes = times(2);
[1,2,3].map(x => times(2)(x));
[1,2,3].map(times(2);
[1,2,3].map(twoTimes);
```
Beim mappen eines arrays kommt auch wieder ein array raus!
Der äussere Typ bleibt bestehen aber der innere typ kann sich ändern
aus einer list von numbers wird eine liste von strings

Das mapping kann nicht dazu führen dass es weniger einträge hat!

Funktionen die einen boolean zurückgeben nenn wir prädikate

filtern der ungerade zalen 
1 2 3
 x=> x%2 ==1
1 3
in java wirds "retain all oder select all" genannt!

Reduce Einsatz
```javascript
[1,2,3].reduce(plus,0);
```
Nur falls man sich sicher ist dasss das array nicht vorher leer ist kann man die variante verwende.

falls x keine zahl ist sondern:
```javascript
["hallo", "webpr"]
x.reduce( (acc, cur) => acc + cur, "");
```
Um rauszufinden ob alle true sind ! 
```javascript
x = [true,true,true,false,true];
beim letzten wert sieht man was der startwert sein sollte hier wäre es "true"
x.reduce( (acc, cur) => acc && cur, true);
```
Wie man einen array zurückgibt "..." wäre der spread operator
```javascript
x.reduce( (acc, cur) => [...acc, cur], []);
```
