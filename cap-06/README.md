# Efectos de Texto y Estilos Tipográficos en CSS3

## 📖 Índice
- [Introducción](#introducción)
- [Efectos de sombra con text-shadow](#efectos-de-sombra-con-text-shadow)
- [Manejo del desbordamiento de texto](#manejo-del-desbordamiento-de-texto)
- [Alineación y espaciado del texto](#alineación-y-espaciado-del-texto)
- [Control de la ruptura de palabras](#control-de-la-ruptura-de-palabras)
- [Uso de la propiedad resize](#uso-de-la-propiedad-resize)
- [Conclusión](#conclusión)

---

## Introducción
CSS3 ha mejorado el control tipográfico con nuevas propiedades que permiten estilizar el texto de manera más avanzada. Entre ellas destacan los efectos de sombra, alineación, espaciado y manipulación del texto en relación con su contenedor.

## 🎨 Efectos de sombra con text-shadow
La propiedad `text-shadow` permite aplicar sombras al texto para mejorar su apariencia o crear efectos visuales llamativos.

```css
h1 {
    text-shadow: 3px 3px 5px rgba(0, 0, 0, 0.5);
}
```
Este código aplica una sombra negra semitransparente a los títulos `<h1>`.

También es posible agregar múltiples sombras:

```css
h1 {
    text-shadow: 0 2px rgba(0,0,0,0.3),
                 0 4px rgba(0,0,0,0.2),
                 0 6px rgba(0,0,0,0.1);
}
```
Cada sombra se posiciona con diferente opacidad para lograr un efecto de profundidad.

## 🔍 Manejo del desbordamiento de texto
Cuando un texto excede el tamaño de su contenedor, podemos controlar su visualización con `text-overflow`.

```css
p {
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}
```
Este código evita que el texto se desborde y muestra puntos suspensivos (`...`) cuando el contenido es demasiado largo.

## 📏 Alineación y espaciado del texto
CSS3 introduce nuevas opciones de alineación como `text-align-last`, que permite definir la alineación de la última línea de un párrafo.

```css
p {
    text-align: justify;
    text-align-last: right;
}
```
Este código justifica el texto pero alinea la última línea a la derecha.

## 🔠 Control de la ruptura de palabras
Para definir cómo las palabras se dividen en líneas, se pueden usar `word-wrap` y `hyphens`.

```css
p {
    word-wrap: break-word;
}
```
Esto permite que las palabras largas se dividan para evitar el desbordamiento.

Para habilitar la separación de palabras automática con guiones:

```css
p {
    hyphens: auto;
}
```
Los navegadores insertarán guiones en los lugares apropiados según el idioma del texto.

## 📏 Uso de la propiedad resize
La propiedad `resize` permite a los usuarios redimensionar elementos de texto.

```css
textarea {
    resize: both;
    overflow: auto;
}
```
Este código permite redimensionar un `<textarea>` en ambas direcciones.

## ✅ Conclusión
CSS3 proporciona un conjunto avanzado de propiedades tipográficas que mejoran la apariencia y usabilidad del texto en la web. Desde efectos visuales como `text-shadow` hasta herramientas de control de alineación y espaciado, estas mejoras facilitan la creación de contenido más atractivo y accesible.
