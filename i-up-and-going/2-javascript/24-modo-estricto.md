## 2.4 Modo estricto

ES5 agregó un "modo estricto" al lenguaje, que trata las reglas de forma más rigurosa para ciertos comportamientos. Generalmente, estas restricciones se consideran como un conjunto de directrices para mantener el código más seguro. Además, la adhesión al modo estricto hace que su código en general sea más optimizable por el motor. El modo estricto es un gran triunfo para el código, y deberías usarlo para todos tus programas.

Puede optar por el modo estricto para una función individual, o para un archivo completo, dependiendo de donde se especifique el modo estricto:

```js
function foo() {
	"use strict";

	// este código esta en modo estricto

	function bar() {
		// este código esta en modo estricto
	}
}

// este código 'no' esta en modo estricto
```

Comparelo con esto:

```js
"use strict";

function foo() {
	// este código esta en modo estricto

	function bar() {
		// este código esta en modo estricto
	}
}

// este código esta en modo estricto
```

Con el modo estricto una diferencia clave \(una mejora!\) es rechazar la declaración implícita de variables globales automáticas al omitir `var`:

```js
function foo() {
	"use strict";	// activa el modo etsricto
	a = 1;		// `var` olvidada, es igual a ReferenceError
}

foo();
```

Si activa el modo estricto en su código, y obtiene errores, o el código comienza a comportarse con errores, su tentación podría ser evitar el modo estricto. Pero ese instinto sería una mala idea al complacerle. Si el modo estricto causa problemas en su programa, casi seguro que es una señal de que tiene cosas en su programa que debe arreglar.

No sólo el modo estricto mantendrá su código de forma más segura, y no sólo hará que su código sea más optimizable, sino que también representa la dirección futura en la que va el lenguaje. Sería más fácil para ti acostumbrarte al modo estricto ahora, que seguir posponiéndolo, ¡después será más difícil de convertirlo!

Nota: Para obtener más información sobre el modo estricto, consulte el Capítulo 5 del título Tipos y Gramática de esta serie.
