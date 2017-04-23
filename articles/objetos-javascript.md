# Objetos Javascript
*¿Qué son los Objetos en Javascript? Definición - Uso - Ejemplos - Video tutorial.*

[Video tutorial](https://youtube.com)

> *"La programación orientada a objetos puede considerarse como el diseño de software a través de un conjunto de objetos que cooperan"* -MDN

- Casi todo en Javascript es un Objeto (Functions, Arrays, Maths, etc..). Por ello se lo considera un lenguage orientado a Objetos.

- Los Objetos son compartimientos de código que interactúan entre si y forman parte de un programa.

- Son variables que pueden contener varias propiedades con distintos valores y/o acciones a través de funciones([métodos](#)).

- Consiguen un código más limpio al poder invocar los valores del Objeto a través de variables.

- Las *propiedades del Objeto* se escriben como pares de *```clave : valor```* separados por comas:

- Podemos crear nuestros propios Objetos.

<hr>

**Ejemplo. Creación de un Objeto llamado "persona":**

```js
// Objeto persona:
var persona = {nombre:"Agustin", apellido:"Palmieri"};

//Podemos variar espacios y saltos de linea sin alterar el resultado:

var persona = {
    nombre : "Agustin",
    apellido : "Palmieri"
};

//Accedemos al valor de nombre:

console.log(persona.nombre); 
// ó
console.log(persona["nombre"]); 

// Nos devuelve:
// Agustin

//------------------------------------------------
// ver cómo Gist en Github  -->> https://gist.github.com/agustinpfs/0cf16fa98029aafb59e5314f61e7233c
``` 




<!-- CÓDIGO DE LA CONSOLA PARA SER EJECUTADO DISPONIBLE EN WEB(RunKit) http://pandawebs.net/objetos-javascript/ 

var persona = {  
    nombre : "Agustin",
    apellido : "Palmieri"
};
console.log(persona.nombre); 
-->



<!-- CÓDIGO DE EJEMPLO EN PÁGINA WEB(JSFiddle embebido)
(ejecutar en web)
http://pandawebs.net/objetos-javascript/

<!DOCTYPE html>
<html>
  <body>
  
    <button onclick="Mifuncion()">
      Mi nombre y apellido ¡click aquí!!
    </button>
    <p id="demo"></p>
    
    <script>
      var persona = {
        nombre: "Agustin",
        apellido: "Palmieri"
      };

      function Mifuncion() {
        document.getElementById("demo").innerHTML =
          " Mi nombre es " +
          persona.nombre + " y mi apellido " + persona.apellido;
      }

    </script>
    
  </body>
</html> -->


<hr>

**Nota:**

En este articulo hemos creado un sencillo "Objeto Literal". Esta manera de crear Objetos se la conoce como **"Inicializador de Objetos"**.

Hay 2 maneras más de crear Objetos que se profundizan en otros artículos:

* Con palabra clave/keyword **"new"**. `new Object()`. [ir al artículo](#)

* Usando un **Constructor de Objetos**. [ir al artículo](#)

<hr>

### Objetos Nativos

Son aquellos Objetos suministrados por Javascript, tales como:

- String
- Boolean
- Number
- Array
- Image
- Date
- Math, etc.

**Estos Objetos funcionan como [*Constructor de Objetos*](http://pandawebs.net/constructor-de-objetos-javascript/)**


**Ejemplo de uso en página web y servicio para ejecutar el código en** [http://pandawebs.net/objetos-javascript/](http://pandawebs.net/objetos-javascript/)

<br>
<!--            FIRMAR COMO COLABORADOR           -->

<!-- <hr>
###Colaboradores

[TU NOMBRE](TU LINK) 

-->
<br>

<!-- Inicio links índice y github -->

<span class="link-to-index-git">Tutoriales Javascript [ ver índice](https://github.com/Pandawebs/Tutoriales-Javascript/blob/master/README.md)</span>

<strong class="link-to-github">[Editar este artículo](https://github.com/Pandawebs/Tutoriales-Javascript/edit/master/clonar-un-repositorio.md " target="_blank)</strong>

<!-- Fin links índice y github -->

[Video Tutorial](#)

<hr>

[siguiente - **métodos javascript**](https://github.com/Pandawebs/Tutoriales-Javascript/blob/master/articles/metodos-javascript.md) 

[anterior - **índice**](https://github.com/Pandawebs/Tutoriales-Javascript/blob/master/README.md) 

