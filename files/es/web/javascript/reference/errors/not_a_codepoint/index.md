---
title: 'RangeError: argument is not a valid code point'
slug: Web/JavaScript/Reference/Errors/Not_a_codepoint
translation_of: Web/JavaScript/Reference/Errors/Not_a_codepoint
---
{{jsSidebar("Errors")}}

## Message

```
RangeError: {0} is not a valid code point (Firefox)
RangeError: Invalid code point {0} (Chrome)
```

## Tipo de error

{{jsxref("RangeError")}}

## ¿Qué estuvo mal?

El metodo {{jsxref("String.fromCodePoint()")}} acepta solamente _**code point**_ validos.

Un [code point](https://en.wikipedia.org/wiki/Code_point) es un valor en el conjunto de caracteres [Unicode](/es/docs/); esto es, un rango de enteros que va desde `0` a `0x10FFFF`.

Usando valores {{jsxref("NaN")}}, enteros negativos (`-1`), no enteros (`3.14`), o valores mayores a `0x10FFFF` (`1114111`) no trabajarian con este metodo.

## Ejemplos

### Casos invalidos

```js example-bad
String.fromCodePoint('_');      // RangeError
String.fromCodePoint(Infinity); // RangeError
String.fromCodePoint(-1);       // RangeError
String.fromCodePoint(3.14);     // RangeError
String.fromCodePoint(3e-2);     // RangeError
String.fromCodePoint(NaN);      // RangeError
```

### Casos validos

```js example-good
String.fromCodePoint(42);       // "*"
String.fromCodePoint(65, 90);   // "AZ"
String.fromCodePoint(0x404);    // "\u0404"
String.fromCodePoint(0x2F804);  // "\uD87E\uDC04"
String.fromCodePoint(194564);   // "\uD87E\uDC04"
String.fromCodePoint(0x1D306, 0x61, 0x1D307) // "\uD834\uDF06a\uD834\uDF07"
```

## Observe tambien

- {{jsxref("String.fromCodePoint()")}}
