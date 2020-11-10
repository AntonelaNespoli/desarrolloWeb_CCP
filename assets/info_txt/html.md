# HTML(HyperText Markup Language)

HTML significa *“Lenguaje de Marcado de Hipertexto”* por sus siglas en ingles, es un lenguaje que pertenece a la familia de los “lenguajes de marcado”. Es utilizado para la elaboración de páginas web y forma parte del universo del **FRONTEND**.

El estándar HTML lo define la *W3C (World Wide Web Consortium)* y actualmente se encuentra en su versión *HTML5*.

Cabe destacar que HTML no es un lenguaje de programación ya que no cuenta con funciones aritméticas, variables o estructuras de control propias de esos lenguajes, por lo cual HTML *genera únicamente páginas web estáticas*, sin embargo, se puede usar en conjunto con diversos lenguajes de programación para la creación de *páginas web dinámicas*.

## ¿Para que sirve HTML?

Básicamente nos permite definir la estructura básica de una página y organizar la forma en que se mostrará su contenido, además de podemos incluir enlaces (links) hacia otras páginas o documentos.Para esto utilizamos **etiquetas**, con las que podemos agregar texto, imágenes, links, entre otras cosas.

## ¿Que son las etiquetas HTML?

Las etiquetas HTML son fragmentos de texto rodeados por corchetes angulares < >, que se utilizan para escribir código HTML, existen etiquetas de apertura: **\<etiqueta>**, y etiquetas de cierre: **\</etiqueta>**. Existe una gran variedad de etiquetas para distintos usos.

## ¿Que es un documento HTML?

Para desarrollar una página web en HTML necesitamos crear un documento HTML, que no es otra cosa que un archivo con la extensión **.html**. En el escribiremos todo el texto y las etiquetas necesarias para la creación de una página, al texto escrito en el documento se le llama **código HTML**. Un documento HTML se puede generar con cualquier editor de textos simple como el bloc de notas de Windows o con editores más modernos y completos como Visual Studio Code, Atom, etc.

## Empecemos a escribir código!

Una página de HTML es un documento que está formado por partes como un encabezado, cuerpo y a veces un pie de página,como una carta. Por ejemplo:

    <!DOCTYPE html>
    <html>
        <head>
            <title>Chicas Programadoras</title>
        </head>
        <body>
            <h1>Hola Mundo</h1>
            <p>Hoy aprendemos HTML!</p>
        </body>
    <html>

Las etiquetas que acabamos de ver le dicen a los navegadores web como *renderizar*, es decir mostrar, el contenido que tiene el documento. Analicemos un poco esto:

* **\<!DOCTYPE html>**: *Todos los documentos HTML deben comenzar con esta declaración*. No es una etiqueta HTML, sino que es "información" para que el navegador sepa que tipo de documento esta *leyendo*, en este caso es HTML5 ya que al no colocar la versión por defecto es la ultima estable.
* **\<html> y \</html>**: Son las etiquetas que marcan el inicio y el fin del *documento HTML*.
    * **\<head> y \</head>**: Son las etiquetas que definen el *encabezado*. Entre ellas colocamos toda la información que necesita el navegador sobre nuestra página web, como el título, el autor, etc. Estos datos no se muestran en la web.
        * **\<title>**: Es el título de nuestra web y parece en la pestaña del navegador.
    * **\<body> y \</body>>**: Definen el cuerpo de la pagina, es lo que se muestra en el navegador.
        * **\<h1>**: Es un titulo y el número define el nivel de importancia, hay 6 niveles.
        * **\<p>**: Define un párrafo.

>**Good Practice!** Notaremos que si quitamos una etiqueta o varias, el texto igualmente se mostrará en pantalla. ***De todas formas, siempre hay que cerrar las etiquetas y en el orden inverso al que fueron abiertas!***

Otra cosa importante que debemos notar es que las etiquetas están siempre dentro de otra de nivel más alto.

Una de las características de este lenguaje es que sus etiquetas se van anidando de *forma tal que se mantiene una estructura*. Por ejemplo:

    <body>                              --> es padre de las etiquetas <h1> y <p> 
        <h1>Hola Mundo</h1>             --> <h1> y <p> están al mismo nivel por ende son hermanas. 
        <p>Hoy aprendemos HTML!</p>         Y pueden a su vez cada una tener sus propias etiquetas hijas.
    </body>                                 

>**Good Practice!** Es recomendable dejar "sangrías" cuando escribimos una etiqueta, nos sirve para mantener el código ordenado y mantener una estructura. 

### Etiquetas de HTML: *Títulos y párrafos*

Hay muchas etiquetas! Lo importante por ahora es que aprendamos las más frecuentes.

Hay 6 niveles para la etiqueta de titulo y lo definimos del 1 al 6, siendo 1 el más importante:
* # Hola  -->  **\<h1>** Hola **\</h1>** 
* ## Hola  -->  **\<h2>** Hola **\</h2>**
* ### Hola  -->  **\<h3>** Hola **\</h3>**
* #### Hola  -->  **\<h4>** Hola **\</h4>**
* ##### Hola  -->  **\<h5>** Hola **\</h5>**
* ###### Hola  -->  **\<h6>** Hola **\</h6>**

Las etiquetas que tienen una barra (/) son de Cierre, es decir que hasta allí es el alcance de la misma.

Si quisiéramos agregar un párrafo además del título podríamos tener algo así:

    <h1>Hola</h1>
    <p>Bienvenidas a chicas programadoras, esto es un club donde aprenderemos a programar!</p>

Si abrimos el archivo en el navegador, debería verse algo así:

># Hola
Bienvenidas a chicas programadoras, esto es un club donde aprenderemos a programar!

### Etiquetas de HTML: *Listas*

Hay dos tipos de listas:

#### Ordenadas:
Son las que enumeran los diferentes puntos de la lista de forma ordenada y se ven así:

>1. Poner agua a hervir
2. Agregar arroz
3. Esperar 15 minutos

Para generar una lista ordenada, el código es el siguiente:

    <ol>                                --> ol = Ordered list
        <li>Poner agua a hervir</li>    --> li = List item
        <li>Agregar arroz</li>
        <li>Esperar 15 minutos</li>
    </ol>

#### No ordenadas:
Son las que utilizan iconos para enumerar cada item de la lista. Por ejemplo:

>* Manteca
>* Yerba
>* Aceite

Y el código nos quedaría así:

    <ul>                    --> ul = Unordered list
        <li>Manteca</li>
        <li>Yerba</li>
        <li>Aceite</li>
    </ul>

### Etiquetas de HTML: *Links*

Los links son palabras u oraciones que al hacer click conducen a otra página web. 

Los reconocemos porque en general están subrayados o destacados de alguna forma, como por ejemplo, de un color diferente.

El etiqueta para crear un link en HTML es: \<a href="url">texto del link</a>

* *href*: es la referencia, y ahí colocamos la url de la web que queremos enlazar.
* El texto que colocamos entre ambos tags, es el que sera visible en la web.
Por ejemplo, si tenemos este link en nuestro código:


    <a href="http://www.chicasprogramadoras.club">Chicas Programadoras</a>

lo veremos así, en nuestra web:

>[Chicas Programadoras](http://www.chicasprogramadoras.club)

### Atributos de una etiqueta

