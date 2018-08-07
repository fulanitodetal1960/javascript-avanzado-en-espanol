## Scope & Closures

Quizás una de las cosas más importantes que necesitará para llegar a un entendimiento rápido es entender cómo funciona realmente 'alcance' de las variables  en JavaScript. No basta con tener ideas borrosas y anecdóticas acerca del scope.

El título Scope & Closures comienza por desacreditar la idea errónea de que JS es un "lenguaje interpretado" y que por lo tanto no compilado. Nooop.

El motor JS compila su código justo antes \(y a veces durante!\) la ejecución. Así que buscamos una comprensión más profunda de la aproximación del compilador a nuestro código para entender cómo encuentra y trata las declaraciones de variables y de las funciones. A lo largo del camino, comprenderemos la tíìca metáfora para la gestión del scope de las variables en JS, el "Hoisting" (elevación).

Esta comprensión crítica del "alcance léxico" es en lo que basamos nuestra exploración del closure en el último capítulo del libro. El closure es quizás el concepto más importante de todos en JS, pero si no ha entendido con firmeza cómo funciona el scope (alcance), es probable que el closure (cierre) permanezca fuera de su alcance.

Una aplicación importante del closure (cierre) es el 'module pattern' (patrón de módulo), tal como lo presentamos brevemente en el Capítulo 2 de este libro. El patrón de módulo es quizás el patrón de organización de código más frecuente en todo el código JavaScript; su profunda comprensión debería ser una de sus más altas prioridades.
