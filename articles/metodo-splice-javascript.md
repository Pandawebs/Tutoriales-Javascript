# Método Array splice() Javascript.

*Método Splice() en Javascript. Definición - Uso - Ejemplos - Video tutorial.*

[Video tutorial](youtube.com " target="_blank)

<hr>

**El método splice() agrega o quita elementos de un array.**

*Sintaxis:*

`array.splice(inicio, eliminar, nuevo,.....,nuevo)`

Parametros:

* `inicio` (requerido) Indica a partir de que elemento se iniciará el cambio(eliminar o agregar).

* `eliminar` (requerido) Indica el número de elementos a eliminar.

* `nuevo` (opcional) Son los nuevos elementos que añadiremos al array.

==*Splice no crea un nuevo array. Modifica el original*==

**Ejemplo:**

```js
var paisaje = ["montaña", "rio", "cielo", "bosque"];
paisaje.splice(2, 1, "mar", "playa");

console.log(paisaje);

// Resultado:
// [ "montaña", "rio", "mar", "playa", "bosque" ]

//------------------------------------------------
// ver cómo Gist en Github  -->> https://gist.github.com/agustinpfs/327294a521692bf46d80dff9453ebe53
```
* En el array original(linea 1):

  * `montaña` -> posisión 0

  * `río` -> posisión 1

  * `cielo` -> posisión 2

* En la linea 2 `paisaje.splice(2, 1, "mar", "playa")` indicamos: Ir a la posisión _**2**_ (cielo) y eliminar _**1**_ elemento a partir de esa posisión(incluída) que sería cielo. Luego que agrege mar y playa en esa misma posisión.

<hr>

**Despejemos dudas agregando conectores al código:**

![alt](http://pandawebs.net/assets/images/splice.png)

<hr>

Si queremos solo agregar y no borrar, el segundo parámetro será 0.
**Ejemplo:**

```js
var paisaje = ["montaña", "rio", "cielo", "bosque"];
paisaje.splice(2, 0, "mar", "playa");


console.log(paisaje);

// Resultado:
// [ "montaña", "rio", "mar", "playa", "cielo", "bosque" ] -->

//------------------------------------------------
// ver cómo Gist en Github  -->> https://gist.github.com/agustinpfs/6565f6dfef11e7e12d55c225a284cdc1
```

Si usamos valores negativos comienzamos a contar desde el final.

**Ejemplo:**

```js
var paisaje = ["montaña", "rio", "cielo", "bosque"];
paisaje.splice(-1, 0, "mar", "playa");


console.log(paisaje);

// Resultado:
// [ 'montaña', 'rio', 'cielo', 'mar', 'playa', 'bosque' ]

//------------------------------------------------
// ver cómo Gist en Github  -->> https://gist.github.com/agustinpfs/6565f6dfef11e7e12d55c225a284cdc1
```

* `bosque` -> posisión 0

* `cielo` -> posisión -1

A partir de la posisión -1(incluída) son insertados los nuevos elementos(mar y playa).

<!-- CÓDIGO DE LA CONSOLA PARA SER EJECUTADO DISPONIBLE EN WEB(RunKit) http://pandawebs.net/metodo-splice-javascript/ 
       
var paisaje = ["montaña", "rio", "cielo", "bosque"];
paisaje.splice(2, 0, "mar", "playa");

console.log(paisaje);

-->

<hr>

<!-- CÓDIGO DE EJEMPLO EN PÁGINA WEB(JSFiddle embebido)
(ejecutar en web)
http://pandawebs.net/metodo-split-javascript/

<!DOCTYPE html>
<html>
  <body>

    <p>Cambiar montaña y rio por mar y playa.</p>

    <button onclick="miFuncion()">Cambiar!</button>

    <p id="demo"></p>

    <script>
    
      var paisaje = ["montaña", "rio", "cielo", "bosque"];
      document.getElementById("demo").innerHTML = paisaje;

      function miFuncion() {
        paisaje.splice(0, 2, "mar", "playa");

        document.getElementById("demo").innerHTML = paisaje;
      }

    </script>

  </body>
</html> -->

<hr>


<br>

Tutoriales Javascript. [ ver índice](http://pandawebs.net/tutoriales-javascript/)

[Editar este artículo](https://github.com/Pandawebs/tutoriales-javascript/edit/master/metodo-splice-javascript.md " target="_blank)

<hr>

[siguiente - **método slice()**](https://github.com/Pandawebs/Tutoriales-Javascript/blob/master/articles/metodo-slice-javascript.md) 

[anterior - **método split()**](https://github.com/Pandawebs/Tutoriales-Javascript/blob/master/articles/metodo-split-javascript.md)
