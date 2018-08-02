# 2.9 Non-JavaScript

Hasta ahora, las únicas cosas que hemos cubierto están en el propio lenguaje JS. La realidad es que la mayor parte de
 de JS está escrito para funcionar e interactuar con entornos como los navegadores. Una buena parte de las cosas que usted escribe en su código, estrictamente hablando, no están directamente controladas por JavaScript. Eso probablemente suena un poco extraño.

El no-JavaScript de JavaScript más común que encontrara es la `API DOM`. Por ejemplo:

```js
var el = document.getElementById( "foo" );
```

La variable `document` existe como variable global cuando el código se ejecuta en un explorador. No es proporcionada por el motor JS, ni es particularmente controlado por la especificación de JavaScript. Toma la forma de algo que se parece mucho a un objeto JS normal, pero no es exactamente eso. Es un objeto especial, a menudo llamado "host object".

Por otra parte, el método `getElementById(..)` en el documento se parece a una función JS normal, pero es sólo una interfaz expuesta a un método incorporado proporcionado por el DOM de su navegador. En algunos navegadores \(de nueva generación\), esta capa también puede estar en JS, pero tradicionalmente el DOM y su comportamiento se implementa en algo más parecido a C / C ++.

Otro ejemplo lo vemos en las entrada/salida \(Input / Optput - I/O\).

alert(..) el favorito de todos muestra un cuadro de mensaje en la ventana del navegador del usuario. alerta (..) es proporcionado a su programa JS por el navegador, no por el motor JS en sí. La llamada que realiza envía el mensaje a las parte interna del navegador que es el que muestra el cuadro de mensaje.

Lo mismo ocurre con `console.log(..)`; Su navegador proporciona estos mecanismos y los vincula a las herramientas de desarrollo.

Este libro, y toda esta serie, se centra en el lenguaje JavaScript. Es por eso que no ve ninguna cobertura sustancial de estos mecanismos non-JavaScript de JavaScript . Sin embargo, debes ser consciente de ellos, ya que estarán en todos los programas de JS que escribas.

