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
* Student's Final Grade
```javascript
function finalGrade (exam, projects) {
  let result= 0;
  if(exam > 90 || projects >10) { result= 100;}
  else if (exam >75 && projects >=5){ result= 90;}
  else if( exam >50 && projects >=2){ result= 75;}
  else{result=0;}

  return result; // final grade
}
```
