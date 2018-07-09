# 1.10 Funciones

El empleado de la tienda de teléfonos probablemente no lleva consigo una calculadora para calcular los impuestos y la cantidad final de la compra. Esa es una tarea que necesita definir una vez y reutilizarla una y otra vez. Lo más probable es, que la compañía tenga una caja registradora \(computadora, tableta, etc.\) con esas "funciones" incorporadas.

Del mismo modo, su programa casi seguramente querrá dividir las tareas del código en piezas reutilizables, en lugar de repetirse repetidamente de forma repetida \(juego de palabras!\). La forma de hacerlo es definir una función.

Una función es generalmente una sección con el nombre del código que puede ser "llamada" por ese nombre, y el código dentro de ella se ejecutará cada vez que se llama. Examine esto:

```js
function printAmount() {
	console.log( amount.toFixed( 2 ) );
}

var amount = 99.99;

printAmount(); // "99.99"

amount = amount * 2;

printAmount(); // "199.98"
```

Opcionalmente, las funciones pueden tomar argumentos \(también conocidos como parámetros\), valores que se le "pasan". Además, también pueden devolver un valor.

```js
function printAmount(amt) {
	console.log( amt.toFixed( 2 ) );
}

function formatAmount() {
	return "$" + amount.toFixed( 2 );
}

var amount = 99.99;

printAmount( amount * 2 );		// "199.98"

amount = formatAmount();
console.log( amount );			// "$99.99"
```

La función `printAmount(..)` toma un parámetro que llamamos `amt`. La función `formatAmount()` devuelve un valor. Por supuesto, también puedes combinar esas dos técnicas en la misma función.

Las funciones se usan co frecuencia con el codigo que piensa 'llamar' repetidamente, pero también pueden ser útiles para organizar fragmentos de código relacionados en colecciones con nombre, incluso si sólo piensa llamarlas una vez.

Examine esto:

```js
const TAX_RATE = 0.08;

function calculateFinalPurchaseAmount(amt) {
	// calculate the new amount with the tax
	amt = amt + (amt * TAX_RATE);

	// return the new amount
	return amt;
}

var amount = 99.99;

amount = calculateFinalPurchaseAmount( amount );

console.log( amount.toFixed( 2 ) );		// "107.99"
```

Aunque `calculateFinalPurchaseAmount(..)` solo se llama una vez, organizar su funcionamiento ,en una función con nombre, por separado hace que el código que usa su lógica \(la declaración `amount = calculateFinal...`\) sea más limpio. Si la función tuviera más declaraciones, los beneficios serían aún más pronunciados.



