# Método Array reduce() Javascript.

*Método reduce() en Javascript. Definición - Uso - Ejemplos - Video tutorial.*

[Video tutorial](youtube.com " target="_blank)


<hr>

El método Array reduce(), __reduce todos los valores de un array a un único valor.__ 
La manera de llegar al único valor lo definiremos en una función que se aplica.
Dicha función se repetirá por cada valor del array.


*Sintaxis:*

`array.reduce(function(acumulador,valorEnCurso), valorInicial)`

* `acumulador` (requerido) es el `valorInicial` (en la primera llamada a la función). A partir de la segunda llamada será el acumulado.

* `valorEnCurso` (requerido) el valor del elemento en curso del array.

* `valorInicial` (opcional) es un valor inicial que se tomará como base. Si no lo ponemos, el valor inicial del acumulador será igual al primer valor del array y el `valorEnCurso` será el segundo.


**Ejemplo:**

<!-- start code snippet: -->

```js
var numeros = [6, 4, 5, 2];

function sumar(total, num) {
    return total + num;
}

var resultado = numeros.reduce(sumar)

console.log(resultado); 

// Resultado
// 17


//------------------------------------------------
// ver cómo Gist en Github  -->> https://gist.github.com/agustinpfs/9760523c52273b007b0e0f8e121f8c1c
```
<!-- end code snippet: -->

* `reduce(sumar)` _linea7_ llama a la función sumar _linea3_ hasta completar la suma.

* `num` _linea3y4_ (valor en curso) irá cambiando entre 4, 5 y 2.

* `total` _linea3y4_  (acumulador) arranca por 6 y le siguen los resultados del llamado a la función anterior, (10, 15)

    * 1º llamado: 6(total) + 4(num)
    * 2º llamado: 10(total) + 5(num)
    * 3º llamado: 15(total) + 2(num) (resultado final=17)

**Si queremos que arranque con un valor específico hará un llamado más:**

* En la linea 7 agregamos por ejemplo el 2(valor inicial):  `var resultado = numeros.reduce(sumar, 2)`.

    * 1º llamado: 2(total) + 6(num)
    * 2º llamado: 8(total) + 4(num)
    * 3º llamado: 12(total) + 5(num)
    * 4º llamado: 17(total) + 2(num) (resultado final=19)


**Podemos incorporar directamente la función sin tener que llamarla:**

<!-- start code snippet: -->

```js
var numeros = [6, 4, 5, 2];

var resultado = numeros.reduce(function(total, num) {
    return total + num;
})

console.log(resultado);

// Resultado
// 17

//------------------------------------------------
// ver cómo Gist en Github  -->> https://gist.github.com/agustinpfs/c680ba08fb881e26984d6579a8d11d2f
```
<!-- end code snippet: -->

<!-- CÓDIGO DE LA CONSOLA PARA SER EJECUTADO DISPONIBLE EN WEB(RunKit) http://pandawebs.net/metodo-reduce-javascript/ 
       
  var numeros = [6, 4, 5, 2];

  var resultado = numeros.reduce(function(total, num) {
      return total + num;
  })

  console.log(resultado);

-->

<hr>

**Ejemplo de reduce() aplicando el método _Math.round_:**

A un array con números decimales, deseamos redondearlos a números enteros para luego sumarlos.
Le agregaremos el valor inicial de 0 para que redondeé el primer elemento también.

<!-- start code snippet: -->

```js
var numeros = [6.2, 4.7, 5.5, 2.3];

function sumar(total, num) {
    return total + Math.round(num);
}

var resultado = numeros.reduce(sumar,0)

console.log(resultado); 

// Resultado
// 19


//------------------------------------------------
// ver cómo Gist en Github  -->> https://gist.github.com/agustinpfs/e2427434d2a16238360c717154ce72d0
```
<!-- end code snippet: -->

<!-- CÓDIGO DE LA CONSOLA PARA SER EJECUTADO DISPONIBLE EN WEB(RunKit) http://pandawebs.net/metodo-splice-javascript/ 
      
  var numeros = [6.2, 4.7, 5.5, 2.3];

  function sumar(total, num) {
      return total + Math.round(num);
  }

  var resultado = numeros.reduce(sumar,0)

  console.log(resultado); 

-->


<hr>

<!-- CÓDIGO DE EJEMPLO EN PÁGINA WEB(JSFiddle embebido)
(ejecutar en web)
http://pandawebs.net/metodo-reduce-javascript/

<!DOCTYPE html>
<html>
  <body>
  
    <p>Promedios</p>
    
    <ul>
      <li>2.3</li>
      <li>5.5</li>
      <li>4.7</li>
      <li>6.2</li>
    </ul>
    
    <button onclick="miFuncion()">Sumar notas como enteros</button>

    <p id="demo"></p>

    <script>
      var numeros = [6.2, 4.7, 5.5, 2.3];

      function sumar(total, num) {
        return total + Math.round(num);
      }

      function miFuncion() {

        var resultado = numeros.reduce(sumar, 0)
        document.getElementById("demo").innerHTML = resultado;
      }

    </script>

  </body>
</html> -->

<hr>


<br>

Tutoriales Javascript. [ ver índice](http://pandawebs.net/tutoriales-javascript/)

[Editar este artículo](https://github.com/Pandawebs/tutoriales-javascript/edit/master/metodo-reduce-javascript.md " target="_blank)

<hr>

[siguiente - **método map()**](https://github.com/Pandawebs/Tutoriales-Javascript/blob/master/articles/metodo-map-javascript.md)

[anterior - **método slice()**](https://github.com/Pandawebs/Tutoriales-Javascript/blob/master/articles/metodo-slice-javascript.md)
