---
title: Worker.terminate()
slug: Web/API/Worker/terminate
translation_of: Web/API/Worker/terminate
---
{{APIRef("Web Workers API")}}

El método **`terminate()`** de la interfaz {{domxref("Worker")}} termina inmediatamente el {{domxref("Worker")}}. Esto no ofrece la oportunidad de finalizar las operaciones que estuviera realizando el worker, termina la ejecución por completo.

## Sintaxis

```js
myWorker.terminate();
```

### Parámetros

Ninguno.

### Retorna

Nada.

## Ejemplo

El siguiente extracto de código muestra la creación de un objeto {{domxref("Worker")}} usando el constructor de {{domxref("Worker.Worker", "Worker()")}} y éste es inmediatamente terminado.

```js
var myWorker = new Worker('worker.js');

myWorker.terminate();
```

## Especificaciones

| Especificación                                                                                       | Estado                           | Comentario                                           |
| ---------------------------------------------------------------------------------------------------- | -------------------------------- | ---------------------------------------------------- |
| {{SpecName('HTML WHATWG', "#dom-worker-terminate", "Worker.postMessage()")}} | {{Spec2('HTML WHATWG')}} | No change from {{SpecName("Web Workers")}}. |
| {{SpecName('Web Workers', "#dom-worker-terminate", "Worker.postMessage()")}} | {{Spec2('Web Workers')}} | Definición inicial.                                  |

## Compatibilidad de navegadores

{{Compat("api.Worker.terminate")}}

## Mirar también

La interfaz {{domxref("Worker")}} a la que pertenece.
