# Método slice() Javascript.

*Método slice() en Javascript. Definición - Uso - Ejemplos - Video tutorial.*

[Video tutorial](youtube.com " target="_blank)

<hr>

Este método existe tanto para el Objeto Array como para el [Objeto String](#).

### Método Array slice().

*Sintaxis:*

`array.slice(inicio,final)`

**Copia una cantidad de elementos de un array en un nuevo array(no modifica el original).**

La copia se indica entre 2 argumentos(inicio y final).

**Ejemplo:**
Vamos a crear un nuevo array copiando solo las frutas cítricas del siguiente array:

<!-- start code snippet: -->

```js
var frutas = ["Banana", "Naranja", "Limón", "Manzana", "Mango"];
var citricos = frutas.slice(1, 3);

console.log(citricos);

// Resultado:
// ["Naranja", "Limón"]

//------------------------------------------------
// ver cómo Gist en Github  -->> https://gist.github.com/agustinpfs/d144690cb07b05fe576a9ea9b3b5ab89
```
<!-- end code snippet: -->

**Explicación:**

* La primera posisión del array es el 0*(Banana)*.

* Las cítricas son la naranja y el limón, necesitamos copiar en un nuevo array el elemento 1*(`Naranja`)* y el elemento 2*(`Limón`)*.

* Tengamos en cuenta que las posisiones que indiquemos incluye la del inicio y no incluye la del final.

* Es decir: `frutas.slice(1, 3)` copia desde la posisión 1*(`Naranja`)* que se incluye, hasta la posisión 3*(`Manzana`)* que no se incluye.

* Resultado:  `["Naranja", "Limón"]`.
<hr>

Si ponemos un sólo número como argumento será tomado como el primer argumento(inicio) y copiará hasta el final del array.

`fruits.slice(3)`

_Resultado_:

`["Manzana", "Mango"]`

<hr>

### Argumentos negativos.

* Si son números negativos el inicio comenzará en el final.

*Sintaxis negativos*:
*```array.slice(final, inicio)```*

Ejemplo:

`var frutas = ["Banana", "Naranja", "Limón", "Manzana", "Mango"];`

* Mango será la posisión 0, Manzana -1, etc...

* Por ejemplo `fruits.slice(-3, -1)` creará el siguiente array:

`["Limón", "Manzana"]`


Si ponemos un sólo número negativo como argumento lo tomará como el argumento final, siendo 0 el valor por defecto inicial.


`fruits.slice(-3)` creará un nuevo array con los elementos desde la posisión 0(Mango) a la -3(Naranja - no incluído):

`["Limón", "Manzana", "Mango"]`


**Inicial positivo. Final negativo:**


`fruits.slice(1, -3)` creará el array:


`["Naranja"]`

<!-- CÓDIGO DE LA CONSOLA PARA SER EJECUTADO DISPONIBLE EN WEB(RunKit) http://pandawebs.net/metodo-splice-javascript/ 
   
var frutas = ["Banana", "Naranja", "Limón", "Manzana", "Mango"];
var citricos = frutas.slice(1, 3);

console.log(citricos);

-->

<hr>

<!-- CÓDIGO DE EJEMPLO EN PÁGINA WEB(JSFiddle embebido)
(ejecutar en web)
http://pandawebs.net/metodo-slice-javascript/

<!DOCTYPE html>
<html>
  <body>
    <ul>
      <li>Banana</li>
      <li>Naranja</li>
      <li>Limón</li>
      <li>Manzana</li>
      <li>Mango</li>
    </ul>

    <button onclick="miFuncion()">Frutas cítricas de la lista</button>

    <p id="demo"></p>

    <script>
      function miFuncion() {
        var frutas = ["Banana", "Naranja", "Limón", "Manzana", "Mango"];
        var citricos = frutas.slice(1, 3);

        document.getElementById("demo").innerHTML = citricos;
      }

    </script>

  </body>
</html> -->

<hr>

### Método String slice().

Funciona igual que [Array slice()](#) pero con strings.

*Ejemplo:*

```js
var str = "Hola mundo!";
var resultado = str.slice(0, 4);

console.log(resultado);

// Resultado:
// Hola

//------------------------------------------------
// ver cómo Gist en Github  -->> https://gist.github.com/agustinpfs/2c959f98762b0985a17bb0cdf0d504d7
```
<!-- CÓDIGO DE LA CONSOLA PARA SER EJECUTADO DISPONIBLE EN WEB(RunKit) http://pandawebs.net/metodo-splice-javascript/ 
      
  var str = "Hola mundo!";
  var resultado = str.slice(0, 4);

  console.log(resultado);
-->

<hr>

<!-- CÓDIGO DE EJEMPLO EN PÁGINA WEB(JSFiddle embebido)
(ejecutar en web)
http://pandawebs.net/metodo-split-javascript/

<!DOCTYPE html>
<html>
  <body>
    <p>Hola mundo, un abrazo para todos</p>
    <button onclick="miFuncion()">Imprimir los 15 primeros caracteres</button>

    <p id="demo"></p>

    <script>
      function miFuncion() {
        var str = "Hola mundo, un abrazo para todos";
        var citricos = str.slice(0, 15) + "...";

        document.getElementById("demo").innerHTML = citricos;
      }

    </script>

  </body>
</html> -->

<hr>


<br>

Tutoriales Javascript. [ ver índice](http://pandawebs.net/tutoriales-javascript/)

[Editar este artículo](https://github.com/Pandawebs/tutoriales-javascript/edit/master/metodo-slice-javascript.md " target="_blank)

<hr>

[siguiente - **método reduce()**](https://github.com/Pandawebs/Tutoriales-Javascript/blob/master/articles/metodo-reduce-javascript.md) 

[anterior - **método splice()**](https://github.com/Pandawebs/Tutoriales-Javascript/blob/master/articles/metodo-splice-javascript.md)
