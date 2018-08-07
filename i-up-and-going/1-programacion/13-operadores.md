## Operadores

Los operadores son los que realizan acciones sobre variables y valores. Ya hemos visto dos operadores de JavaScript, el `=` y el `*`.

El operador `*` realiza la multiplicación matemática. Muy simple, ¿verdad?

El operador igual  `=`  se utiliza en la asignación: primero calculamos el valor en el lado derecho \(valor origen\) de `=` y luego se lo asignamos a la variable que especificamos en el lado izquierdo \(variable destino\).

**Advertencia**: Esto puede parecer una extraña inversion de orden de la asignación. En lugar de `a = 42`, algunos podrían preferir invertir el orden, de modo que el valor de origen esté a la izquierda y la variable de destino esté a la derecha, como `42 -> a` (¡esto no es valido en JavaScript!). Desafortunadamente, la forma correcta es `a = 42`, y variaciones similares, son bastante frecuente en los lenguajes de programación modernos. Si no se siente comodo, dedique un tiempo a ensayar este orden en su mente para acostumbrarse a él.

Examine esto:

```js
a = 2;
b = a + 1;
```

Aquí, asignamos el valor 2 a la variable 'a'. A continuación, obtenemos el valor de la variable 'a' \(todavía 2\), le agregamos 1 resultando en el valor 3, luego almacenamos ese valor en la variable 'b'.

Si bien técnicamente no es un operador, necesitará la palabra clave `var` en cada programa, ya que es la forma principal de declarar \(crear\) variables \(consulte "Variables"\).

Siempre debe declarar la variable por su nombre antes de usarla. Pero solo necesita declarar una variable una vez para cada alcance (consulte "Scope"); después de eso puede usarse tantas veces  como sea necesario. Por ejemplo:

```js
var a = 20;

a = a + 1;
a = a * 2;

console.log( a );	// 42
```

Éstos son algunos de los operadores más comunes en JavaScript:

* Asignación: = como en  a = 2.
* Matemáticas: **'+'** \(adición\), **'-'** \(sustracción\), **'\*'** \(multiplicación\) y **'/'** \(división\), como en `a*3`.
* Asignación Compuesta : **'+ ='**, **'- ='**, **'\* ='**, y **'/ ='** son operadores compuestos que combinan una operación matemática con asignación, como en `a + = 2` \(igual que `a = a + 2`\).
* Incremento / Decremento: **'++'** \(incremento\), **'--'** \(decremento\), como en `a ++` \(similar a `a = a + 1`\).
* Acceso a la propiedad del objeto:. Como en **'console.log \(\)'**. Los objetos son valores que contienen otros valores en determinadas ubicaciones denominadas propiedades. `obj.a` significa un valor de objeto llamado obj con una propiedad del nombre a. Las propiedades se pueden acceder alternativamente como `obj \["a"\]`. Consulte el Capítulo 2.
* Igualdad: == \(suelto-igual\), === \(estricto-igual\),! = \(Suelto no-igual\),! == \(estricto no igual\), como en a == b.
* Consulte "Valores y Tipos" y el Capítulo 2.
* Comparación: **'<'**\(menor que\), **'>'**\(mayor que\), **'<='** \(menor o igual que\), **'>='** \(mayor o igual que\), como en `a <= b`.
* Consulte "Valores y Tipos" y el Capítulo 2.
* Lógico: **'&&'** \(y\), **'\|\|'** \(O\), como en `a || b` que selecciona a o b. Estos operadores se usan para expresar condicionales compuestos \(ver "Condicionales"\), como si a o b es verdadero.

**Nota**: Para obtener más detalles y cobertura de operadores que no se mencionan aquí, consulte "Expresiones y operadores" de Mozilla Developer Network \(MDN\) [\(https://developer.mozilla.org/en-US/docs/Web/JavaScript / Guía / Expresiones\_y\_Operadores\).](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators)
