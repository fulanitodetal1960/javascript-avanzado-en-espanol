## This & Object Prototypes

Tal vez uno de las más difundidos y persistentes falsas afirmaciones sobre JavaScript es que la palabra clave `this` se refiere a la función en la que aparece. Grave error.

La palabra clave `this` se enlaza dinámicamente en función de cómo se ejecute la función en cuestión y resulta que hay cuatro reglas simples para comprender y determinar completamente el vínculo con `this`.

El mecanismo de prototipo de objeto está muy relacionado con la palabra clave `this`, que es una cadena de búsqueda de propiedades, similar a cómo se encuentran las 'variables de alcance léxico'. Pero envuelto en los prototipos esta el otro gran error de JS: la idea de emular \(imitar\) las clases y la herencia \(lo que se llama "prototipo"\).

Desafortunadamente, el deseo de intentar pensar en patrones de diseño de clase y herencia en JavaScript es casi lo peor que puedes intentar hacer, porque aunque la sintaxis puede inducirte a pensar que hay algo presente igual a las clases, de hecho el mecanismo de prototipo tiene básicamente el comportamiento opuesto.

Lo que está en cuestión es si es mejor ignorar el desajuste y pretender que lo que está implementando es "herencia", o si es más apropiado aprender y abrazar cómo funciona realmente el prototipo del sistema.  Lo último se llama más apropiadamente "delegación de comportamiento".

Esto es más que una preferencia sintáctica. **La delegación es un patrón de diseño totalmente diferente, y más potente, que reemplaza la necesidad de diseñar con clases y herencia**. Sin embargo, estas reeivindicaciones pasaran de largo ante casi todas las publicaciones en blogs, libros y conferencias sobre el tema durante toda la vida de JavaScript.

Las afirmaciones que hago con respecto a la delegación versus herencia no provienen de una aversión al lenguaje y su sintaxis, sino del deseo de ver la verdadera capacidad del lenguaje apropiadamente aprovechada y para eliminar la interminable confusión y frustración.

Pero lo que preparo con respecto a los prototipos y la delegación es mucho más complicado de lo que me gustaria exponer en este momento. Si estás listo para reconsiderar todo lo que crees saber sobre las "clases" y la "herencia" de JavaScript, te ofrezco la posibilidad de "tomar la pastilla roja" (Matrix 1999) y echar un vistazo a los Capítulos 4-6 del título 'this & Object Prototypes' de esta serie.
