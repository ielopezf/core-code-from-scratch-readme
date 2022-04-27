# Thursday

* Multiply exercise
```javascript
function multiply(a, b){
  var resultado = a * b;
  return resultado;
}
```

* ASCII Exercise
```javascript
function uniTotal (cadena) {
// total up dem unicodes!
  let letrasTotal= cadena.length;
  let suma=0;
  for(let conta=0; conta<letrasTotal;conta++){
    let caracter=cadena.charCodeAt(conta);
    suma= caracter+ suma;
  }//fin del for contador
  return suma;
}
```
* Char From ASCII Value
```javascript
function getChar(c){
  
return String.fromCharCode(c);
}
```
* Binary adittion
```javascript
 function addBinary(a,b) {
var sum = a+b;
  var bina= sum.toString(2);
  console.log(bina);
  return bina;
}
```
