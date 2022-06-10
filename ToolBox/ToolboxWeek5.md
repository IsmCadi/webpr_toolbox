# Woche 5 - 30.03.22

## Console Goody:
Statement Terminator , semicolon ist NICHT optional !!!
In 1/3 aller Fehlerfälle fehlt das Semicolon ! Dabei muss es zudem kommen.
'' werden als "" ausgegeben, jedoch einzelne werden wie in einem normalen Satz behandelt.

\ sind oft in Regular expression... -> '\banana\s \'
Slashy syntax / \banana\s \\ /  für Regular Expression

## New Concepts
-> Code der unsere Website ändert:
Damit wurde der Schutzmeachnismus des Browsers unterlaufen ! 
PBA _> Progressive Webapp

## Refactor from:
```javascript
    <script src="function/function.js"></script>
    <script src="function/functionTest.js"></script>

    <script src="lambda/lambda.js"></script>
    <script src="lambda/lambdaTest.js"></script>

    <script src="snake/snake.js"></script>
    <script src="snake/snakeTest.js"></script>
```
## Refactor to:
```javascript
<script>
    [
    "function",
    "lambda",
    "snake"
    ].forEach( name => {
    document.writeln(`<script src="${name}/${name}.js"><`+'/script>');
    document.writeln(`<script src="${name}/${name}Test.js"><`+'/script>');
});
</script>
```

## Scripting
Eval litereal drin gestahn hätte =>  wenn code seiteneffeckt erzeugen soll un das ok ist.
Ist weniger sicher.

Function macht eine neue Funktion
Bei Function versucht man keine Seiteneffeckte zu erzeugen !
 