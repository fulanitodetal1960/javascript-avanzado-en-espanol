# 1.9 Bucles

Durante las horas punta, hay una lista de espera para los clientes que necesitan hablar con el empleado de la tienda telefónica. Mientras hayan personas en esa lista, solo se necesita seguir atendiendo al próximo cliente.

Repetir un conjunto de acciones hasta que cierta condición falla - en otras palabras, repetir sólo mientras la condición se mantiene - es un trabajo para programar con bucles; Los bucles pueden tener diferentes formas, pero todos satisfacen este comportamiento básico.

Un bucle tiene una condición de prueba, así como un bloque \(normalmente con forma de `{..}`\). A cada repeticion del bloque del bucle, se le llama iteración.

Por ejemplo, el bucle `while` y el bucle `do..while` ilustran el concepto de repetir un bloque de sentencias hasta que una condición ya no se evalúa como verdadera:

```js
while (numOfCustomers > 0) {
	console.log( "How may I help you?" );

	// help the customer...

	numOfCustomers = numOfCustomers - 1;
}

// versus:

do {
	console.log( "How may I help you?" );

	// help the customer...

	numOfCustomers = numOfCustomers - 1;
} while (numOfCustomers > 0);
```

La única diferencia práctica entre estos bucles es si el condicional se prueba antes de la primera iteración \(`while`\) o después de la primera iteración \(`do..while`\).

De cualquier forma, si la evaluacion de la condicion da falso, la siguiente iteración no se ejecutará. Esto significa que si la condición es inicialmente falsa, un bucle `while` nunca se ejecutará, pero un bucle `do..while` se ejecutará sólo la primera vez.

A veces realiza un bucles con el propósito de contar una serie de números, como desde 0 a 9 \(diez números\). Puede hacerlo estableciendo una variable de iteración de bucle como `i` con el valor `0` e incrementándola en `1` en cada iteración.

**Advertencia**: Por una variedad de razones históricas, los lenguajes de programación casi siempre cuentan las cosas comenzando por cero, es decir, comenzando con 0 en lugar de 1. Si no está familiarizado con ese modo de pensar, puede ser muy confuso al principio. Tómese su tiempo para practicar el conteo empezando por 0 para sentirse más cómodo con él.

El condicional se prueba en cada iteración, como si hubiera una declaración `if` implícita dentro del bucle.

Podemos usar la instrucción `break` de JavaScript para detener un bucle. También, podemos observar que es extremadamente fácil crear un bucle  que de otra manera no se detendria nunca sin un mecanismo de ruptura para detenerlo.

Vamos a ilustrar esto:

```js
var i = 0;

// a `while..true` loop would run forever, right?
while (true) {
	// stop the loop?
	if ((i <= 9) === false) {
		break;
	}

	console.log( i );
	i = i + 1;
}
// 0 1 2 3 4 5 6 7 8 9
```

**Advertencia**: Esta no es necesariamente una forma práctica que quisieras usar para tus bucles. Se presenta aquí sólo con fines ilustrativos.

Mientras que `while` \(o `do..while`\) puede realizar la tarea de forma csencilla, hay otra forma sintáctica llamada bucle `for` sólo para ese propósito:

```js
for (var i = 0; i <= 9; i = i + 1) {
	console.log( i );
}
// 0 1 2 3 4 5 6 7 8 9
```

Como puede ver, en ambos casos el condicional` i <= 9` es verdadero para las primeras 10 iteraciones \(`i ` con valores de 0 a 9\) en cualquier forma de bucle, pero se convierte en falso una vez que `i` tenga el valor 10.

El bucle `for` tiene tres cláusulas: la cláusula de inicialización \(`var i = 0`\), la cláusula de prueba condicional \(`i <= 9`\) y la cláusula de actualización \(`i = i + 1`\). Así que si vas a contar con su bucle de iteraciones, `for` es una forma más compacta y, a menudo, más fácil de entender y escribir.

Hay otras formas de bucle especializados que están destinados a iterar sobre valores específicos, como las propiedades de un objeto \(véase el capítulo 2\), donde la prueba condicional implícita es solo ver si todas las propiedades han sido procesadas. El concepto de "bucle hasta que una condición falla" se cumple sin importar la forma del bucle.



