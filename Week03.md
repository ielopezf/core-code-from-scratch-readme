# Monday

1. Who likes it
```javascript
    function likes(names) {
  
      //revisar que tenga al menos un like
  
      const singular= " likes this";
  
      const plural = " like this";
  
      var pivoteNombres="";
  
      //un like
    
      if( names.length==1){    
    
        pivoteNombres= names[0] + singular;  
    
        return pivoteNombres }
  
    //sin likes
  
    if (names.length==0){  return "no one likes this";  }
  
    else{
  
      //sies menor a 4 personas se imprimen los nombres
    
      if(names.length <4){
    
        pivoteNombres= names[0];
      
        for( let i= 1 ; i < names.length ; i++ ){
         
            if(i != names.length -1){
          
              pivoteNombres+= ", "+names[i] ; }
            
            else{ 
          
              pivoteNombres+= " and " + names[i] ;}
               
        }
      
        return pivoteNombres + plural;
      }
    
      //si es mayor a 4 solo se imprimen los dos primeros y nombres y el # restante de likes
      else{
      
        return  names[0] + ", "+ names[1] + " and " + (names.length -2) + " others" +plural;
   
      }
    }

  }
```
2. Bit counting
```Javascript
var countBits = function(n) {
  // Program Me
  if(n >=0){
    let pivot=n.toString(2);
    var num=0;
    for ( let char in pivot)
      {
        if( pivot[char]==1){
          num+=1;
        }
      }
    return num;
  }
};
```
3.Your order, please
```Javascript
function order(words){
  // ...
  
  var final="";
  const pivot= words.split(" ");
  const pivot2= words.split(" ");
  if(words=== "")
    {
      return "";
    }
   
  else{
    
    var frase= pivot;
    let pivotLen= pivot.length ;
   for(let i=0; i<pivotLen ; i++){
      
      let cont=1;
      var result= pivot2[i].indexOf(cont);
          
      while(result == -1){
        cont+=1;
        result= pivot2[i].indexOf(cont);
      }
      if(result!= -1)
      {frase[cont -1 ]= pivot2[i];
       //delete pivot[i];
        }
      cont=1;
   
    }
    
    
    final= frase.join(' ');
    return final;
  }
}
```


# Tuesday
* Simple Pig Latin
```javascript
function pigIt(str){
  //Code here

  var arrayWords= str.split(" ");
  let word= "";
  let newWord= new Array();
  let first='';
  for(let i=0;i<arrayWords.length; i++){
    var char= ['.', ',','!','?'];
    
    word = arrayWords[i];
    if(char.includes( word)){continue;}
    newWord= word.split('');
    first= word.charAt(0);
    newWord.shift();
    newWord[word.length-1]= first;
    word= newWord.join('');
    arrayWords[i]= word.concat("ay");
  }
  let newArray= arrayWords.join( " ");
  return newArray; 
  
  
}
```
* Counting Duplicates
```javascript
function duplicateCount(text){
  /*We'r egoing to return a number thah indicates the quantity of 
  characters that were repeated inside the string*/
  let orderingPivot= text.toUpperCase().split('').sort();

  let result=0;

  let saveRepeatedChar= new Array();
  let word=0;

  for(let i= 0; i<orderingPivot.length ; i++){
    let count=1;
    
    if(orderingPivot[i]==orderingPivot[i+1] ){ 
     word+=1;
    }
    
    else{ 
      word+=1; 
      saveRepeatedChar.push(word); // we're adding the number of occurrences
      word= 0;
        }

  }
  
  for( let j=0; j<saveRepeatedChar.length; j++ ){
    if(saveRepeatedChar[j]> 1){result++;} //if the number of ocurrecnes is at least 2 we're adding to result
  }
  
  return result;//...
}
```
* Decode The Morse Code 
```javascript
decodeMorse = function(morseCode){
  //your code here
  //remove spaces from start and end
  morseCode= morseCode.trim();
  //save each set word
  let morseCodeWords= morseCode.split("   ");
  //create pivots
  let codeWords= new Array();
  let decodeAnswer= new Array();
  for(let i=0; i<morseCodeWords.length; i++){
    //we're inside a for that let us check each word
    let actualWord= morseCodeWords[i].split(" ");
    let decodeWord= "";

    for(let j= 0; j< actualWord.length; j++){
      decodeWord+= MORSE_CODE[actualWord[j]];
    }
    decodeAnswer[i]= decodeWord;
  }
  
  
  return decodeAnswer.join(" ");
}
```
# Wednesday
* Valid Parentheses
```javascript
```
* Convert String To Camel Case
```javascript
```
* Unique In Order
```javascript
var uniqueInOrder=function(iterable){

  let arrayChar= new Array();
  
  if(iterable.length ==0 ){ arrayChar=[];}
  else{
    arrayChar.push(iterable[0]);
    for(let i= 0; i<iterable.length-1 ; i++){
    
    if(iterable[i]!=iterable[i+1]){ 
    
    arrayChar.push(iterable[i+1]);
    }
    
  }}
  
  
  return arrayChar;//...
}

```
# Thursday
* Fold an array
```javascript
function reverseArray( array){
  const reversedArray=[];
  for( let i= array.length-1 ; i >=0; i--){
    reversedArray.push(array[i]);
  }
  return reversedArray;
}

function sum( a1, a2){
const sumArr=[];
   for(let i=0; i<a1.length; i++){
         //delete result[i];
         let res=a1[i] + a2[i];
      sumArr.push(res);
      }
  return sumArr;
}

function setResult(piv,short){
  let b2= new Array();
  let b3= new Array();
  b2= reverseArray(piv);
  b3= sum(b2, short);
  return b3
}

function foldArray(array, runs)
{
  let newArray= array;
  let result= new Array();
  let lengthArray= 0;//newArray.length;
  let middleIndex= 0;//Math.floor(newArray.length/2);
  let firstHalf= new Array();
  let secondHalf= new Array();
  array=0;
  

  while(runs){
   
    lengthArray=newArray.length;
    middleIndex= 0;
    secondHalf=0;
    result=0;
        
    if(lengthArray%2 != 0 && lengthArray!=1){
      middleIndex= Math.floor(lengthArray/2);
      secondHalf=newArray.slice(middleIndex+1);
      
      let middle= newArray[middleIndex];
     // firstHalf= newArray.splice(0, middleIndex );
      firstHalf= newArray.slice(0, middleIndex );
      result= setResult(secondHalf,firstHalf);
      
      result.push(middle);
      newArray= 0;
      newArray= result;
      console.log("newArray: "+newArray);
      newArray= 0;
    newArray= result;
    }
    else if( lengthArray==1){
      result= newArray;
      newArray= 0;
    newArray= result;
      break;
    }
    else{
      middleIndex= Math.floor(lengthArray/2);
      secondHalf=newArray.slice(middleIndex);
      firstHalf= newArray.slice(0, middleIndex );
      result= setResult(secondHalf,firstHalf);
      newArray= 0;
    newArray= result;
    }
    
    runs--;
  }
  
 let newResult= result;
 result=0;
 array=0;
 
  return newResult;
 
  
}

```
* Encrypt This!
```javascript
var encryptThis = function(text) {
  // Implement me! :)
  
  var arrayWords= text.split(' ');
  var firstLetter= '';
  var lastLetter='';
  var secondLetter='';
  
  var result='';
  for(let i=0; i< arrayWords.length; i++){
   
    let actualWord=arrayWords[i];
    let wordArray=actualWord.split('');
    
    firstLetter= actualWord.charCodeAt(0);
    wordArray[0]=firstLetter;
   
    if( actualWord.length>2){
      secondLetter= actualWord.charAt(1);
      lastLetter=actualWord.charAt(actualWord.length -1 );
      wordArray[wordArray.length-1]=secondLetter;
      wordArray[1]=lastLetter;
    }
    
   
    arrayWords[i]= wordArray.join('');
    
  }
  result= arrayWords.join(" ");
  return result;
}
```
