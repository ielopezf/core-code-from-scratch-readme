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
# Wednesday
* Holiday VIII - Duty Free exercise
```javascript
function dutyFree(normPrice, discount, hol){
  let discountPer= discount/100;
  let discountFinal= normPrice*discountPer;
  let result= hol/discountFinal;
  return Math.floor(result);
}
```
* Twice As Old exercise
```javascript
function twiceAsOld(dadYearsOld, sonYearsOld) {
  // your code here
  let doubleSonYears= sonYearsOld * 2;
  //validate if it's already the double of his son's age
  if(dadYearsOld==doubleSonYears ){ return 0;}
  //otherwise, calculate how much it's going to be need to be twice his son's age
  else{
     return Math.abs(doubleSonYears-dadYearsOld);
  }
}
```
* Valid Spacing exercise
```javascript
function validSpacing(s) {
  // write your code here
  //verify if it's empty
  let result= true;
   var anteriorChar= s[0];
    var actualChar='';
  if(s == ''){ result= true; }
  else if( s== ' '){ result= false;}
  else{
    //space it´s the first or last char
    if( s.startsWith(' ') || s.endsWith(' ')){ result= false;}
    else{
     
      for(let i=1; i< s.length; i++){
        actualChar= s[i];
        console.log(actualChar);
        if( actualChar== ' ' && anteriorChar ==' '){
          result= false; break; return result;}
        anteriorChar= s[i];
         console.log(anteriorChar);
      }
     
    }
  }
   return result;
}
```
* Fake Binary exercise
```javascript
function fakeBin(x){
  let pivot= '';
for( let i= 0; i < x.length ; i++){
  if(x[i]<5){ pivot+= 0 ;}
  else {pivot+= 1 ;}
}
  return pivot;
}
```
# Thursday
* Remove All Exclamation Marks From The End Of Sentence exercise
```javascript
function remove (string) {  
 // let string = " hi! hi !!"
  let pivot=string;
  let bandera=string.endsWith('!');
 
  for(let j= string.length-1; j>0; j--){
    if(bandera==true){
      pivot= string.slice(0,j);}
     bandera= pivot.endsWith('!');
   
  }
  
  
  return pivot;
}
```

* Vowel Remover exercise
```javascript
```

* Rock Paper Scissors! exercise
```javascript
```

* Persistent Bugger exercise
```javascript
```
