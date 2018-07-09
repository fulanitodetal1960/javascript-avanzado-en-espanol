# 1.8 Condicionales

"¿Desea agregar los protectores de pantalla adicionales a su compra, por $ 9.99?". El empleado de la tienda telefónica le ha pedido que tome una decisión. Y puede que necesite consultar primero el estado actual de su cartera o cuenta bancaria para responder a esa pregunta. Pero, obviamente, esto es sólo una simple pregunta "sí o no".

Hay bastantes maneras de expresar condicionales \(decisiones\) en nuestros programas.

La más común es la instrucción `if`. Esencialmente, usted está diciendo: "Si esta condición es cierta, haga lo siguiente ...". Por ejemplo:

```js
var bank_balance = 302.13;
var amount = 99.99;

if (amount < bank_balance) {
	console.log( "I want to buy this phone!" );
}
```

La instrucción `if` requiere una expresión entre paréntesis `()` que puede tratarse como verdadero o falso. En este programa, hemos proporcionado la expresión `amount < bank_balance`, que se evaluará como `true` o `false` dependiendo de la cantidad almacenada en la variable `bank_balance`.

Incluso puede proporcionar una alternativa por si la condición no es verdadera, llamada cláusula `else`. Examine esto:

```js
const ACCESSORY_PRICE = 9.99;

var bank_balance = 302.13;
var amount = 99.99;

amount = amount * 2;

// can we afford the extra purchase?
if ( amount < bank_balance ) {
	console.log( "I'll take the accessory!" );
	amount = amount + ACCESSORY_PRICE;
}
// otherwise:
else {
	console.log( "No, thanks." );
}
```

Aquí, si `amount < bank_balance` es `true`, imprimiremos "¡Tomaré el accesorio!" Y agregue 9.99 a nuestra variable `amount`. De lo contrario, la cláusula `else` dice que simplemente responderemos cortésmente con "No, gracias". Y dejar la cantidad sin cambios.

Como vimos en el apartado "Valores y Tipos" anteriormente, los valores que ya no son del tipo esperado son a menudo transformados al tipo esperado. La sentencia `if` espera un booleano, pero si se pasa algo que no sea ya booleano, se producira la coerción de tipo.

JavaScript define una lista de valores específicos que se consideran "falsos" porque cuando se transforman a un booleano, se convierten en `'false'` - estos incluyen valores como `0` y `""`. Cualquier otro valor que no esté en la lista de "falsos" es automáticamente `"true"` - cuando se transforma a un booleano se convierten en verdaderos. Los valores verdaderos incluyen cosas como 99.99 y "free". Vea "Truthy & Falsy" en el Capítulo 2 para más información.

Ademas de `if` existen otras formas de condicionales. Por ejemplo, la instrucción `switch` puede usarse como una abreviatura para una serie de instrucciones `if..else` \(vea el Capítulo 2\). Los bucles \(ver "Loops"\) usan un condicional para determinar si el bucle debe continuar o detenerse.

**Nota**: Para obtener información más detallada sobre las transformaciones que puedan producirse implícitamente en las expresiones de los condicionales en los ejemplos de prueba, consulte el Capítulo 4 de esta serie con el título _Tipos y Gramática_.



