---
title: border-inline-start-width
slug: Web/CSS/border-inline-start-width
translation_of: Web/CSS/border-inline-start-width
---
{{CSSRef}}{{SeeCompatTable}}

La propiedad de [CSS](/es/docs/Web/CSS) **`border-inline-start-width`** define el ancho del borde lógico inicial en línea de un elemento, que se asigna al estilo de borde físico dependiendo del modo de escritura, la direccionalidad y la orientación del texto del elemento. Esto corresponde a las propiedades {{cssxref("border-top-width")}} y {{cssxref("border-bottom-width")}}, o {{cssxref("border-left-width")}}, y {{cssxref("border-right-width")}} dependiendo de los valores definidos por {{cssxref("writing-mode")}}, {{cssxref("direction")}}, y {{cssxref("text-orientation")}}.

{{EmbedInteractiveExample("pages/css/border-inline-start-width.html")}}

## Sintaxis

```css
/* <'border-width'> values */
border-inline-start-width: 5px;
border-inline-start-width: thick;
```

Propiedades relacionadas son {{cssxref("border-block-start-width")}}, {{cssxref("border-block-end-width")}}, and {{cssxref("border-inline-end-width")}}, que definen los otros anchos del borde del elemento.

{{cssinfo}}

### Valores

- `<'border-width'>`
  - : El ancho del borde. Mira {{ cssxref("border-width") }}.

### Sintaxis formal

{{csssyntax}}

## Ejemplo

### Contenido HTML

```html
<div>
  <p class="exampleText">Example text</p>
</div>
```

### Contenido CSS

```css
div {
  background-color: yellow;
  width: 120px;
  height: 120px;
}

.exampleText {
  writing-mode: vertical-lr;
  border: 1px solid blue;
  border-inline-start-width: 5px;
}
```

{{EmbedLiveSample("Ejemplo", 140, 140)}}

## Especificación

| Especificación                                                                                                                               | Estado                                           | Comentario          |
| -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ | ------------------- |
| {{SpecName("CSS Logical Properties", "#propdef-border-inline-start-width", "border-inline-start-width")}} | {{Spec2("CSS Logical Properties")}} | Definición inicial. |

## Compatibilidad en navegadores

{{Compat("css.properties.border-inline-start-width")}}

## Mira también

- Esta propiedad se asigna a una de las propiedades del borde físico:{{cssxref("border-top-width")}}, {{cssxref("border-right-width")}}, {{cssxref("border-bottom-width")}}, y {{cssxref("border-left-width")}}
- {{cssxref("writing-mode")}}, {{cssxref("direction")}}, {{cssxref("text-orientation")}}
