# Imágenes de Bordes y Efectos de Caja en CSS3

## 📖 Índice
- [Introducción](#introducción)
- [Uso de imágenes en los bordes](#uso-de-imágenes-en-los-bordes)
- [Propiedades principales de border-image](#propiedades-principales-de-border-image)
- [Sombras en cajas con box-shadow](#sombras-en-cajas-con-box-shadow)
- [Bordes redondeados con border-radius](#bordes-redondeados-con-border-radius)
- [Conclusión](#conclusión)

---

## Introducción
CSS3 ha mejorado la forma en que podemos decorar los bordes y cajas en la web. Ahora podemos usar imágenes personalizadas como bordes, agregar sombras realistas y redondear los bordes sin necesidad de imágenes extra.

## 🎨 Uso de imágenes en los bordes
La propiedad `border-image` permite utilizar imágenes en lugar de los bordes tradicionales.

```css
.box {
    border: 20px solid transparent;
    border-image-source: url('border.png');
    border-image-slice: 30;
}
```
Esto aplica una imagen como borde alrededor del elemento `.box`.

## 🖼 Propiedades principales de border-image
CSS3 introduce varias propiedades para personalizar imágenes en los bordes:

- **`border-image-source`**: Define la imagen utilizada para el borde.
- **`border-image-slice`**: Divide la imagen en secciones para que se ajuste al borde.
- **`border-image-width`**: Controla el grosor del borde.
- **`border-image-repeat`**: Define cómo se repite la imagen (`stretch`, `repeat`, `round`).

Ejemplo con todas las propiedades:

```css
.box {
    border: 10px solid transparent;
    border-image: url('border.png') 30 fill / 10px / 5px round;
}
```

## 🌟 Sombras en cajas con box-shadow
La propiedad `box-shadow` permite agregar sombras realistas a los elementos.

```css
.shadow-box {
    width: 200px;
    height: 100px;
    background: white;
    box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.5);
}
```
- El primer valor es el desplazamiento horizontal.
- El segundo, el desplazamiento vertical.
- El tercero, el desenfoque.
- El cuarto, el color de la sombra.

También podemos agregar múltiples sombras separadas por comas.

```css
.multi-shadow {
    box-shadow: 2px 2px 10px black, -2px -2px 10px gray;
}
```

## 🔵 Bordes redondeados con border-radius
La propiedad `border-radius` permite crear esquinas redondeadas sin imágenes.

```css
.round-box {
    width: 150px;
    height: 150px;
    background: lightblue;
    border-radius: 20px;
}
```
También se pueden crear círculos perfectos con:

```css
.circle {
    width: 100px;
    height: 100px;
    background: red;
    border-radius: 50%;
}
```

## ✅ Conclusión
Las nuevas propiedades de CSS3 permiten un control avanzado sobre los bordes y cajas, reduciendo la necesidad de imágenes adicionales y mejorando el rendimiento. Ahora podemos aplicar sombras, imágenes en bordes y bordes redondeados con solo unas pocas líneas de código.
