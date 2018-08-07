## Comentar el código

El empleado de la tienda telefónica puede tomar notas de las características de un teléfono recién lanzado o sobre los nuevos planes que su empresa ofrece. Estas notas son sólo para el empleado - no son para que las lean los clientes. Sin embargo, estas notas ayudan al empleado a hacer mejor su trabajo documentando los comos y porqués de lo que debe decir a los clientes.

Una de las lecciones más importantes que puede aprender sobre la escritura de código es que no es sólo para la computadora. El código es tanto, si no más, para el desarrollador como para el compilador.

Su computadora sólo se preocupa por el código máquina, una serie de 0s y 1s binarios, que viene de la compilación. Hay una cantidad casi infinita de programas que podrías escribir produciendo la misma serie de 0s y 1s. Las decisiones que tome sobre cómo escribir el programa importan, no solo pra usted, sino para los demás miembros de su equipo e incluso para su futuro.

Debe esforzarse no solo en escribir programas que funcionen correctamente, sino programas que tengan sentido cuando se examinen. Puede recorrer un largo camino en este sentido eligiendo buenos nombres para sus variables (consulte "Variables") y funciones (consulte "Funciones").

Sin embargo, otra parte importante son los comentarios del código. Estos son fragmentos de texto en su programa que se insertan para explicarle cosas a un ser humano. El intérprete / compilador siempre ignorará estos comentarios.

Hay muchas opiniones sobre lo que debe ser un buen código comentado; No podemos definir reglas universales absolutas. Pero algunas observaciones y directrices son muy útiles:

* El código sin comentarios es subóptimo.
* Demasiados comentarios \(uno por línea, por ejemplo\) es probablemente un signo de código mal escrito.
* Los comentarios deben explicar 'por qué', no lo 'qué' hacen. Opcionalmente pueden explicar 'cómo' si es particularmente confuso.

En JavaScript, hay dos tipos de comentarios posibles: comentarios de una sola línea y comentarios de varias líneas.

Examine esto:

```js
// This is a single-line comment

/* But this is
       a multiline
             comment.
                      */
```

El comentario de una sola línea **//**  es apropiado si vas a poner un comentario justo encima de una sola sentencia, o incluso al final de una línea. Todo lo que pongas en la linea despues de **//** se trata como comentario \(por lo tanto es ignorado por el compilador\). No hay ninguna restricción a lo que puede aparecer dentro de un comentario de una sola línea.

Examine esto:

```js
var a = 42;		// 42 is the meaning of life
```

El comentario multilinea **/ \* .. \* /**  es apropiado si tienes que hacer varias líneas de explicación en tu comentario.

Aquí muestro un uso común de comentarios multilínea:

```js
/* The following value is used because
   it has been shown that it answers
   every question in the universe. */
var a = 42;
```

También puede aparecer en cualquier parte de una línea, incluso en el centro de una línea, porque el signo **\* /** lo termina. Por ejemplo:

```js
var a = /* arbitrary value */ 42;

console.log( a );	// 42
```

Lo único que no puede aparecer dentro de un comentario de varias líneas es un **\* /**, porque eso sería interpretado para finalizar el comentario.

Sin duda querrá comenzar su aprendizaje de programación comenzando con el hábito de comentar el código. A lo largo del resto de este capítulo, verá que uso comentarios para explicar las cosas, haga lo mismo con suss prácticas. Confíe en mí, ¡todos los que lean su código se lo agradecerán!
