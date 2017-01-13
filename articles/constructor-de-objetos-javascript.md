# Constructor de objetos

**Es una función que nos servirá para crear muchos objetos a partir de una misma estructura.**

[Video tutorial](youtube.com " target="_blank)

<hr>

**Ejemplo:** 
Creamos 2 objetos llamados "miHermana" y "miHermano" utilizando un constructor llamado "persona".

```
// Constructor "persona":

function persona(nom, edad) {
    this.nombre = nom;
    this.edad = edad;   
};

var miHermana = new persona("María", 30);
var miHermano = new persona("Leonardo", 47);

// Ejecutamos:

console.log(miHermano.nombre)

// Nos devuelve:
// Leonardo

// Ejecutamos:

console.log(miHermana.edad)

// Nos devuelve:
// 30

//------------------------------------------------
// ver cómo Gist en Github  -->> https://gist.github.com/agustinpfs/232b6b12807426925d22912c4e972d46.js
```

<br>

**Despejemos dudas agregando conectores de colores al código:**


![alt](http://pandawebs.net/assets/images/constructor-de-objetos.png)


**Explicación:**

**Este constructor es una función que crea *objetos de tipo "persona."**  

* Tengamos en cuenta que los argumentos `(nom, edad)` en la linea 1 le podemos
 poner cualquier nombre. Lo relevante será el orden ya que corresponderán al mismo orden (posisión) que tienen los nuevos valores de las propiedades en las lineas 5 y 6 (conectores rojos y verdes).

 *nom(posisión 1) = María y Leonardo.*

 *edad(posisión 2) = 30 y 47.*

* Los argumentos deberán ser iguales a los valores de las propiedades (conectores azules). 

* Los nombres de los argumentos son independientes del nombre que le pongamos a las propiedades.  
Pueden ser iguales en el caso de la edad en la linea 3 `this.edad = edad;`. O distintos en el caso del nombre en la linea 2 `this.nombre = nom;`.

* En las lineas 5 y 6 llamamos a construír 2 objetos de tipo `persona`*(nombre de la función constructora)*.
Un objeto llamado `"miHermana"` y otro llamado `"miHermano"`.

* *`new`* y *`this`* son palabras reservadas(Keywords) necesarias para el uso del constructor.
    * *`new`*  nuevo objeto.
    * *`this`* sera reemplazado por el nombre del nuevo objeto `"miHermana"` - `"miHermano"` cuando necesitemos acceder a sus respectivos valores (conectores naranjas y conectores celestes).

* Las conectores marrones indican el nombre de la propiedad con la cual llamaremos cuando deseemos obtener valores de nuestro objeto. `nombre` `edad`.

<!-- CÓDIGO DE LA CONSOLA PARA SER EJECUTADO DISPONIBLE EN WEB(RunKit) http://pandawebs.net/metodos-javascript/ 
      
function persona(nom, edad) {
    this.nombre = nom;
    this.edad = edad;   
};

var miHermana = new persona("María", 30);
var miHermano = new persona("Leonardo", 47);

console.log(miHermano.nombre)
-->

<hr>

<!-- CÓDIGO DE EJEMPLO EN PÁGINA WEB(JSFiddle embebido)
(ejecutar en web)
http://pandawebs.net/metodos-javascript/

<!DOCTYPE html>
<html>
  <body>

    <button onclick="Mifuncion()">La edad de mis hermanos!</button>

    <p id="demo"></p>

    <script>
      function persona(nom, ed) {
        this.nombre = nom;
        this.edad = ed;
      }

      var miHermano = new persona("Leonardo", 47);
      var miHermana = new persona("María", 30);

      function Mifuncion() {

        return document.getElementById("demo").innerHTML =
          "Mi hermano tiene " + miHermano.edad + "años . Mi hermana tiene " + miHermana.edad + " años";
      }

    </script>

  </body>
</html> -->

<hr>

**Ejemplo:** Podemos crear un [método](http://pandawebs.net/metodos-javascript/) para poder cambiar valores de propiedades del objeto constructor.

```
// Constructor 'alumno' con método 'cambiarNombre':

function alumno(nombre, apellido, año, aula, materia) {
    this.nombre = nombre;
    this.apellido = apellido;
    this.aula = aula;
    this.materia = materia;
    this.cambiarNombre = function (nom, apell) {
        this.nombre = nom;
        this.apellido = apell;
    };
}

var mejorPromedio = new alumno("Agustin", "Palmieri", "segundo", 5, "javascript");

mejorPromedio.cambiarNombre("José","Gomez");

console.log("El mejor promedio es de " + mejorPromedio.nombre + " " + mejorPromedio.apellido);

// Resultado:
// El mejor promedio es de José Gomez

//------------------------------------------------
// ver cómo Gist en Github  -->> https://gist.github.com/agustinpfs/7db2a08e573bef19e7ac31dce18cc90a#file-test-js
```

**Nota:**
La función de la propiedad `cambiarNombre`_(linea 6)_ asigna el valor de los argumentos `(nom, apell)` a las propiedades nombre y apellido.

<!-- CÓDIGO DE LA CONSOLA PARA SER EJECUTADO DISPONIBLE EN WEB(RunKit) http://pandawebs.net/metodos-javascript/ 
     
function alumno(nombre, apellido, año, aula, materia) {
    this.nombre = nombre;
    this.apellido = apellido;
    this.aula = aula;
    this.materia = materia;
    this.cambiarNombre = function (nom, apell) {
        this.nombre = nom;
        this.apellido = apell;
    };
}

var mejorPromedio = new alumno("Agustin", "Palmieri", "segundo", 5, "javascript");

mejorPromedio.cambiarNombre("José","Gomez");

console.log("El mejor promedio es de " + mejorPromedio.nombre + " " + mejorPromedio.apellido);
-->

<hr>

Tutoriales Javascript. [ ver índice](http://pandawebs.net/tutoriales-javascript/)

[Editar este artículo](https://github.com/Pandawebs/tutoriales-javascript/edit/master/constructor-de-objetos-javascript.md " target="_blank)

<hr>

<div class="post-content_next">
  <a href="http://pandawebs.net/metodos-javascript/">
    <div class="post-content_next-left">
      <p>anterior</p>
      <span>métodos javascript</span>
  </div>
  <a href="http://pandawebs.net/metodo-split-javascript/">
    <div class="post-content_next-right">
      <p>siguiente</p>
      <span>método split()</span>
    </div>
  </a>
</div>
[siguiente - **método split()**](https://github.com/Pandawebs/Tutoriales-Javascript/blob/master/articles/metodo-split-javascript.md) 

[anterior - **métodos javascript**](https://github.com/Pandawebs/Tutoriales-Javascript/blob/master/articles/metodos-javascript.md) 