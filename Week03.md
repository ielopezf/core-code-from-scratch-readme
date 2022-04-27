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

