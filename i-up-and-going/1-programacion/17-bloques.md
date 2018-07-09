# 1.7 Bloques

El cliente de la tienda telefónica debe pasar por una serie de pasos para completar la compra mientras compra su teléfono nuevo.

Del mismo modo, dentro del código a menudo necesitamos agrupar una serie de declaraciones, a las cuales llamamos bloque. En JavaScript, un bloque se define envolviendo una o más declaraciones dentro de un par de llaves {..}. Examine esto:

```js
var amount = 99.99;

// un bloque general
{
	amount = amount * 2;
	console.log( amount );	// 199.98
}
```

Este tipo general de bloque independiente `{..}` es válido, pero no es muy común verlo en los programas de JS. Por lo general, los bloques se adjuntan a alguna instrucción de control, como una instrucción `if` \(consulte los "Condicionales"\) o a un bucle \(consulte los "Loops"\). Por ejemplo:

```js
var amount = 99.99;

// is amount big enough?
if (amount > 10) {			// <-- block attached to `if`
	amount = amount * 2;
	console.log( amount );	// 199.98
}
```

Vamos a explicar la declaracion `if` en la siguiente sección, pero como puede ver, el bloque `{..}` con sus dos declaraciones se adjunta a un `if (amount > 10)`; Las declaraciones dentro del bloque sólo se procesarán si pasa el condicional.

Nota: A diferencia de la mayoría de otras sentencias como `console.log(amount);`, una instrucción de bloque no necesita un punto y coma \(;\) para concluirlo.



