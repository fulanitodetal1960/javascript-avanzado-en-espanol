## Async & Performance (Asíncrono y Rendimiento)

Los tres primeros títulos de esta serie se centran en la mecánica básica del lenguaje, pero el título cuarto se ramifica ligeramente para abarcar los patrones sobre la mecánica del lenguaje para gestionar la programación asincrona. La asincronía no solo es fundamental para el rendimiento de nuestras aplicaciones, sino que se está convirtiendo cada vez más en un factor crítico de la capacidad de escritura y mantenimiento.

El libro comienza aclarando primero  una gran cantidad de terminología y la confusión de conceptos sobre cosas como "asincrónico", "paralelo" y "concurrente", y explica en profundidad cómo tales cosas se aplican o no en JS.

Luego pasamos a examinar los 'callbacks'  como método principal para habilitar la asincronía. Pero es aquí donde vemos rápidamente que los 'callbacks' por sí solos son irremediablemente insuficientes para las demandas modernas de programación asincrónica. Identificamos dos deficiencias principales de codificación solo en los callbacks: pérdida de confianza en  'inversión de control (IoC)' y falta de capacidad de razonamiento lineal.

Para abordar estas dos grandes deficiencias, ES6 introduce dos nuevos mecanismos \(de hecho, patrones\): las promesas y los generadores \(promises y generators\)

Las promesas son una envoltura independiente del tiempo acerca de un "valor futuro", que le permite razonar y componer independientemente de si el valor está listo o no. Además, resuelven eficazmente los problemas de confianza de IoC dirigiendo los 'callbacks' a través de un mecanismo de promesa confiable y composable.

Los generadores introducen un nuevo modo de ejecución en las funciones JS, con lo que el generador puede pausarse en puntos de rendimiento y reanudarse asincrónicamente más tarde. La capacidad de pausa y reanudación permite que el código de búsqueda secuencial síncrono en el generador se procese de forma asincrónica entre bastidores.Al hacerlo, dirigimos las confusiones de los callbacks no lineales y no locales y, por lo tanto, hacemos que nuestro código asincrono tenga una apariencia sincronizada más razonable.

Pero es la combinación de 'promesas y generadores' lo que hace nuestro patrón de codificación asíncrono más efectivo hasta la fecha en JavaScript. De hecho, gran parte de la sofisticación futura de la asincronía que viene en ES7 y posteriores seguramente se basará en esto. Para tomar en serio la programación eficaz en un mundo asíncrono, necesitará sentirse realmente cómodo combinando 'promesas y generadores'.

Si las 'promesas y los generadores' tienen que ver con la expresión de patrones que permiten que nuestros programas se ejecuten de forma más concurrente y así lograr un mayor procesamiento en un período más corto, JS tiene muchas otras facetas para optimizar el rendimiento que vale la pena explorar.

El Capítulo 5 profundiza en temas como el paralelismo de programas con Web Workers y el paralelismo de datos con SIMD, así como técnicas de optimización de bajo nivel como ASM.js. El Capítulo 6 analiza la optimización del rendimiento desde la perspectiva de técnicas adecuadas de evaluación comparativa, que incluyen el tipos de rendimiento del que preocuparse y cual ignorar.

Escribir JavaScript de manera eficaz significa escribir código que puede romper las barreras de restricciones de ejecución dinámica en una amplia gama de navegadores y otros entornos. Se requiere una gran cantidad de planificación compleja y de esfuerzo de nuestras partes para llevar un programa de "funcionar" a "funcionar bien".

El título Async & Performance está diseñado para ofrecerte todas las herramientas y habilidades que necesitas para escribir código JavaScript razonable y eficaz.
