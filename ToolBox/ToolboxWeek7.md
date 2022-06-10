# Woche 7 - 13.04.22


##Goodie
```javascript
let x = 1;
{x: x}
{x: 1} = $1
{x} = {x: 1} = $2
let obj = {foo: function foo(){ return 1;}  }

obj.foo()
1 = $3

obj = { foo(){ return 1; }  }
{foo:function} = $4

obj.foo() = 1 = $3
```
##CLasses
Mit einer syntaktische verkürzung gegenüber der vorherigen Version mit dem eigenen lokalen Scope:
```javascript
class Person {
    constructor(first, last) {
        this.firstname = first;
        this.lastname = last;
    }
    getName() {
        return this.firstname + " " + this.lastname
    }
}
// new Person("Good", "Boy") instanceof Person
```

Ein extends Example, bzw spezialisierung des der Person als Studenten:
```javascript
class Student extends Person {
    constructor (first, last, grade) {
        super(first, last); // don't forget the super call
        this.grade = grade;
    }
}
const s = new Student("Top","Student", 5.5);
```

```javascript
let foo = () => 1;

foo = () => 1;
foo() = 1;
foo.x = 3;

```

Prototype chain
Student -> Person -> Object  ( alle sind prototypes )
Der prototype des objectes s wird gesetzt auf den wert der prototype property der instance of S
- Object ist der KOnstruktor von Objekten ! 
- Deshalb könen die FUnkctionen weitere Properties haben !
- Die sind vom Typ Funktion 

```javascript
Object.setPrototypeOf(result, Person.prototype);

Number.prototype.times = function (callback){
    return Array.from({length: this}, (el, idx) => callback(idx));
    //console.log(this);
}

```