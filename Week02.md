# Thursday

* Multiply exercise

function multiply(a, b){
  var resultado = a * b;
  return resultado;
}

* ASCII Exercise

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

* Char From ASCII Value

function getChar(c){
  
return String.fromCharCode(c);
}


