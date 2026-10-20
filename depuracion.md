# 🐞 Bloque D · Mi informe de depuración

Rellena una ficha por bug. Sustituye cada `____` por lo que hayas visto TÚ en las DevTools.
Ejemplo de cómo se escribe una variable vista en el panel «Ámbito» (Scope): `i = 1`, `texto = "3"`.

## 👀 Ejemplo (ya resuelto) · Total del ticket

- **Síntoma:** sale 85 € y debería salir 105 €.
- **Breakpoint en:** `caja.js:17` (la línea `const linea = lineas[i];`)
- **Lo que vi:** en la primera parada `i = 1` y `linea` es el Zelda: el Tetris (posición 0) no se suma nunca.
- **Por qué falla:** el bucle empieza en 1 y los arrays empiezan en 0.
- **Arreglo:** `for (let i = 0; ...)`.

## Bug 1 · Añadir unidades

- **Síntoma:** Sale 23 en vez de 5 (los concatena, no los suma)
- **Breakpoint en:** `caja.js:26`
- **Lo que vi:** He visto tres variables en Scope, dos de ellas valian como números, pero una como texto.
- **Por qué falla:** Como el valor que se añade va entre comillas, lo reconoce como un texto. Entonces lo que hace el "+" es concatenar en vez de sumar.
- **Arreglo:** Lo he arreglado convirtiendo en número `textoDelUsuario`.

## Bug 2 · Stock de cada producto

- **Síntoma:** Devuelve `sin datos`en vez de 0
- **Breakpoint en:** `caja.js:36`
- **Lo que vi:** Vi que el `producto.stock=0`, sin embargo el `stock="sin datos`
- **Por qué falla:** El `||`cambia el valor por `sin datos`porque el 0 es falsy.
- **Arreglo:** Cambiar `||`por `??`.

## Bug 3 · Ordenar por precio

- **Síntoma:** ____
- **Breakpoint en:** ____
- **Lo que vi:** ____
- **Por qué falla:** ____
- **Arreglo:** ____

## Bug 4 · Descuento por volumen

- **Síntoma:** ____
- **Breakpoint en:** ____ *(prueba un breakpoint condicional: `unidades === 4`)*
- **Lo que vi:** ____
- **Por qué falla:** ____
- **Arreglo:** ____
