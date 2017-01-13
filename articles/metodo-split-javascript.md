# Método String split() Javascript.

*Método Split() en Javascript. Definición - Uso - Ejemplos - Video tutorial.*

[Video tutorial](youtube.com " target="_blank)

<hr>

**El método split() divide un string y las divisiones resultantes pasan a ser los elementos de un nuevo array.**

*Sintaxis:*

`string.split(separador,límite)`

* El parámetro `separador`(opcional) indica en donde debe hacerse la división, puede ser un caracter(entre comillas) o una [expresión regular(regex)](#).

* El parámetro `límite`(opcional) indica un límite en la cantidad de divisiones en el nuevo array.

* Si no ponemos parámetros, devolverá un array con un solo elemento.

**Ejemplo:**

```
var cadena = "Analizando el funcionamiento de split";
var resultado = cadena.split(" ");

console.log(resultado);

// Resultado:
// [ "Analizando", "el", "funcionamiento", "de", "split" ] 

//------------------------------------------------
// ver cómo Gist en Github  -->> https://gist.github.com/agustinpfs/1df3f622525752d3fcd7a120477b40b8
```


En el ejemplo utilizamos solo el parámetro separador indicando que la división se realize en cada espacio.

Si lo dejaramos vacío ("") haría la división en cada caracter.

Si colocaramos una letra, por ejemplo ("i"), haría la división en cada letra i __sin incluírla__.

Con el parámetro límite. Ejemplo (" ", 2), nos devuelve un array con los 2 primeros elementos.

<!-- CÓDIGO DE LA CONSOLA PARA SER EJECUTADO DISPONIBLE EN WEB(RunKit) http://pandawebs.net/metodo-split-javascript/ 
      
var cadena = "Analizando el funcionamiento de split";
var resultado = cadena.split(" ");

console.log(resultado);

-->

<hr>
<!-- CÓDIGO DE EJEMPLO EN PÁGINA WEB(JSFiddle embebido)
(ejecutar en web)
http://pandawebs.net/metodo-split-javascript/

<!DOCTYPE html>
<html>
  <body>

    <em>Crear array usando cada palabra de este string como elemento</em>
    <button onclick="miFuncion()">Crear array</button>
    <br>
    <p><strong>Nuevo Array:</strong></p>
    <p id="demo"></p>

    <script>
    
      function miFuncion() {
        var str = "Crear array usando cada palabra de este string como elemento";
        var res = str.split(" ");
        document.getElementById("demo").innerHTML = res;
      }

    </script>

  </body>
</html> -->



<hr>

Tutoriales Javascript. [ ver índice](http://pandawebs.net/tutoriales-javascript/)

[Editar este artículo](https://github.com/Pandawebs/tutoriales-javascript/edit/master/metodo-split-javascript.md " target="_blank)

<hr>

[siguiente - **método splice()**](https://github.com/Pandawebs/Tutoriales-Javascript/blob/master/articles/metodo-splice-javascript.md) 

[anterior - **constructor javascript**](https://github.com/Pandawebs/Tutoriales-Javascript/blob/master/articles/constructor-de-objetos-javascript.md)