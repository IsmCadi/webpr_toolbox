# Woche 8 - 27.04.22

##Goodie
```javascript
let y = 2;
{x: x, y: y}
{x: 1, y: 2 }
console.log(x,y)
console.log("x is ",x , "and y is", y)
console.log({x,y})  ===> {x:1, y:2}
let foo = param => console.log(param.x, param.y);
foo = ({x,y}) => console.log(param.x, param.y);
foo({x:1, y:2})

const foo2 = param => console.log(param.x, param.y);
foo2({x:1, y:2})

const foo3 = ({y, y, z=3}) => console.log(param.x, param.y);

```