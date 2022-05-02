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
      console.log(pivot);
      
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
  console.log(str);
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
    console.log(" word: "+word);
    arrayWords[i]= word.concat("ay");
  }
  let newArray= arrayWords.join( " ");
  return newArray; 
  
  
}
```
* Counting Duplicates
```javascript
```
* Decode The Morse Code 
```javascript
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

function foldArray(array0, runs)
{
  console.log("\t START");
  var result= [];//new Array();
  //result=[];
  const array= array0;
  
  console.log("first array: "+array);
  const tama1= array.length;
  const tama2= Math.floor(tama1/2);
  let middle= array[tama2];
  let pivot= array.slice(tama2);
  let shortenedArray= array.splice(0, tama2);
   if(tama1==1){return array;}
  //repeat each run
   
  else{
    const newRun=runs;
    console.log( "\n runssss: "+newRun);
    for(let n=runs; n>0 ; n--){
      console.log("RUN:    "+n);
      
      console.log( "middle:"+ middle +" pivot:"+pivot+" short:"+shortenedArray);
      
      console.log("actual array: "+ array);
      //verify if it's even
      if(tama1%2 ==0){
       
       result= setResult(pivot,shortenedArray);
       console.log(result);
       
     }
    //otherwise it's odd
      else {
      //we reassigned to pivot a new array without the past first value
      pivot= pivot.slice(1);
      //we send pivot to a function that reverses the array
       console.log("newpivot without 1: "+pivot);
    
    
      result= setResult(pivot,shortenedArray);
      //result= sum(shortenedArray, secondHalf);
      result.push(middle);
     //result= sumArrays(pivot, shortenedArray);
      console.log("result run "+n +"\t "+result);
        }
     }
    return result;
    }
  
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
    console.log("\t START FOR");
   console.log("word: "+arrayWords[i]);
    console.log(arrayWords[i].length);
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
    
    console.log( "first: "+firstLetter+"second: "+secondLetter+"third: "+lastLetter);
    
    
    
    arrayWords[i]= wordArray.join('');
    console.log("new word:\t"+arrayWords[i]);
  }
  result= arrayWords.join(" ");
  return result;
}
```
