## Valores y Tipos

Si le preguntas a un empleado en una tienda de teléfono cuánto cuesta un teléfono determinado, y le dicen "noventa y nueve con noventa y nueve" \(es decir, $ 99.99\), te están dando una cifra numérica real que representa lo que vas a necesitar pagar \(más impuestos\) para comprarlo. Si usted quiere comprar dos de esos teléfonos, puede hacer un calculo mental fácilmente para duplicar ese valor y obtener $ 199.98 de costo base.

Si ese mismo empleado coge otro teléfono similar, pero dice que es "gratis", no le están dando un número, sino otro tipo de representación de su costo esperado \($ 0.00\) - la palabra "gratis".

Cuando más tarde pregunte si el teléfono incluye un cargador, la respuesta sólo podría haber sido "sí" o "no".

De manera similar, cuando expresa valores en un programa, elige diferentes representaciones para esos valores en función de lo que planea hacer con ellos.

Estas representaciones diferentes de valores se denominan **'tipos'** en la terminología de programación. JavaScript tiene tipos incorporados para cada uno de estos valores primitivos:

* Cuando necesitas hacer calculos numericos, quieres `números`.
* Cuando necesite imprimir un valor en la pantalla, necesita una `cadena de caracteres` \(uno o más caracteres, palabras, oraciones\).
* Cuando necesite tomar una decisión en su programa, necesita un `booleano` \(verdadero o falso\).

Los valores que se incluyen directamente en el código fuente se llaman literales. Las `cadenas` literales están rodeados por comillas dobles **"..."** o comillas simples **'...'** - la única diferencia es la preferencia estilística. Los literales `número` y `booleanos` se presentan tal cual \(es decir, **42**, **true**, etc.\).

Examine esto:

```js
"I am a string";
'I am also a string';

42;

true;
false;
```

Además de los tipos string / number / boolean, es común que los lenguajes de programación proporcionen arrays, objetos, funciones y más. Cubriremos mucho más sobre valores y tipos a lo largo de este capítulo y el siguiente.

### Conversión entre tipos

Si tienes un número pero necesitas imprimirlo en la pantalla, necesitas convertir el valor en una cadena, y en JavaScript esta conversión se llama "coerción". Del mismo modo, si alguien introduce una serie de caracteres numéricos en un formulario en una página de comercio electrónico, la introduce como una cadena, pero si necesita utilizar ese valor para realizar operaciones matemáticas, debe convertirla (Coercion) en un número.

JavaScript proporciona varias facilidades diferentes para forzar la coerción entre tipos. Por ejemplo:

```js
var a = "42";
var b = Number( a );

console.log( a );	// "42"
console.log( b );	// 42
```

El uso de la funcion `Number \(..\)` \(una función incorporada\) fuerza una coerción explícita de cualquier otro tipo al tipo de número. Eso debería ser muy sencillo.

Pero tenemos un conflicto cuando intentamos comparar dos valores que no son del mismo tipo, lo que requeriría una coerción implícita.

Al comparar la cadena "99.99" con el número 99.99, mucha gente estaría de acuerdo en que son equivalentes. Pero no son exactamente iguales, ¿verdad? Es el mismo valor en dos representaciones diferentes, dos tipos diferentes. Se podría decir que son "vagamente iguales", ¿no?

Para ayudarte en estas situaciones comunes, JavaScript a veces se activa y convertira implícitamente los valores en tipos coincidentes.

Así que si usas el operador comun de igualdad **'=='** para hacer la comparación "99.99" == 99.99, JavaScript convertirá el lado izquierdo "99.99" en su número equivalente 99.99. La comparación asi se convierte en 99.99 == 99.99, que es por supuesto verdad.

Si bien está diseñado para ayudarlo, la coerción implícita puede crear confusión si no se ha tomado su tiempo para aprender las reglas que rigen su comportamiento. La mayoría de los desarrolladores de JS nunca lo tienen, por lo que la sensación común es que la coerción implícita es confusa y daña los programas con errores inesperados, por lo que debe evitarse. Incluso a veces se llama un defecto en el diseño del lenguaje.

Sin embargo, la coerción implícita es un mecanismo que se puede aprender, y además debe ser aprendido por cualquiera que desee tomarse en serio la programación en JavaScript. ¡No sólo no confunde una vez que se aprenden las reglas, sino que se pueden hacer mejores programas! El esfuerzo vale la pena.

**Nota**: Para obtener más información sobre la coerción, consulte el Capítulo 2 de este título y el Capítulo 4 del título de Tipos y Gramática de esta serie.

