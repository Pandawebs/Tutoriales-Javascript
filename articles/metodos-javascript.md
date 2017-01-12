# Métodos Javascript

*¿Qué son los Métodos en Javascript? Definición - Uso - Ejemplos - Video tutorial.*

[Video tutorial](https://youtube.com)

_**Métodos en javascript son acciones dentro de los objetos.
Es una función en una propiedad del objeto.**_

**Ejemplo:**

```js
// Objeto 'persona' con Método 'nombreCompleto':

var persona = {
    nombre : "Agustin",
    apellido : "Palmieri",
    nombreCompleto: function() {return this.nombre + " " + this.apellido;}
};

// Accedemos al método nombreCompleto:

console.log(persona.nombreCompleto());

// El resultado es:
// Agustin Palmieri

//------------------------------------------------
// ver cómo Gist en Github  -->> https://gist.github.com/agustinpfs/fe6b123652eb0237260e0562ba377d74
```

<!-- CÓDIGO DE LA CONSOLA PARA SER EJECUTADO DISPONIBLE EN WEB(RunKit) http://pandawebs.net/metodos-javascript/ 
     
var persona = {
    nombre : "Agustin",
    apellido : "Palmieri",
    nombreCompleto: function() {return this.nombre + " " + this.apellido;}
};

console.log(persona.nombreCompleto());
-->

**`this` hace referencia a `persona`**. Practica colocando `persona.nombre` y `persona.apellido` en lugar de `this.nombre` y `this.apellido`. Verás que obtienes el mismo resultado.

<hr>

<!-- CÓDIGO DE EJEMPLO EN PÁGINA WEB(JSFiddle embebido)
(ejecutar en web)
http://pandawebs.net/metodos-javascript/

<!DOCTYPE html>
<html>
  <body>

    <button onclick="Mifuncion()">
      Nombre completo ¡click aquí!
    </button>
    <p id="demo"></p>

    <script>
      var persona = {
        nombre: "Agustin",
        apellido: "Palmieri",
        nombreCompleto: function() {
          return this.nombre + " " + this.apellido;
        }
      };

      function Mifuncion() {
        document.getElementById("demo").innerHTML =
          " Nombre completo: " +
          persona.nombreCompleto();
      }

    </script>

  </body>
</html> -->

<hr>

### Métodos incluídos en Javascript.

Existen múltiples métodos que vienen por defecto en los objetos nativos de javascript.


Ejemplos:

* Métodos del objeto Array:
    * [split()](#)
    * [map()](#)
    * [slice()](#)

* Método del objeto String.
    * [substr()](#)
    * [slice()](#)

* Método del objeto Math.
    * [random()](#) 

[*Lista de métodos nativos*](#)

<hr>

**Ejemplo de uso en página web y servicio para ejecutar el código en** [http://pandawebs.net/metodos-javascript/](http://pandawebs.net/metodos-javascript/)

Tutoriales Javascript. [ ver índice](http://pandawebs.net/tutoriales-javascript/)

[Editar este artículo](https://github.com/Pandawebs/tutoriales-javascript/edit/master/metodos-javascript.md " target="_blank)

<hr>

[siguiente - **constructor javascript**](https://github.com/Pandawebs/Tutoriales-Javascript/blob/master/articles/constructor-de-objetos-javascript.md) 

[anterior - **objetos javascript**](https://github.com/Pandawebs/Tutoriales-Javascript/blob/master/articles/objetos-javascript.md) 
