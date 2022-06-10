# Woche 6 - 06.04.22

## Console Goody:
Array grösse definieren, bzw. optionale Argumente:
```javascript
Array.from("adsdad");
[0,1,2,3,4]
Array.from({length:10});
//Mapping
Array.from({length:10}).map(el => 1);
Array.from({length:10}).map( (el, idx) => idx);
Array.from({length:10}, (el, idx) => idx);
```

Open, dynamic
Der Pubkt ist der Object dereferenzierungsoperator, und muss in den value aufgelöst und dereferenziert werden !
Merke -> this definiert immer das links vom Punkt.
```javascript
    const good = {
        firstname : "Good",
        lastname  : "Boy",
        // must use "this" or type error
        getName   : function() { return this.firstname + " "  + this.lastname }
    };
```

Mixed, classified
Es wird eine Konstante angelegt damit nichts überschrieben wird.
es wird eine neue property mit prototype hinzu.
Eine Person muss von da an mit "new" angegeben werden.
Ist die "default" konstruktion in z.B. TypeScript
```javascript
Person.prototype.getName = function(){
    return this.firstname + "" + this.lastname;
};
return Person;
new Person("Good", "Boy") instanceof Person
```

Prototype macht eine Klassifikation von Objekte, gleicht Typen..
```javascript

```