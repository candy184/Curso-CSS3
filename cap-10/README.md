# Gradientes en CSS3

## 📖 Índice
- [Introducción](#introducción)
- [Gradientes lineales](#gradientes-lineales)
- [Gradientes radiales](#gradientes-radiales)
- [Uso de múltiples gradientes](#uso-de-múltiples-gradientes)
- [Conclusión](#conclusión)

---

## Introducción
CSS3 introduce los **gradientes**, una herramienta poderosa para generar fondos de color sin necesidad de imágenes. Existen dos tipos principales de gradientes: **lineales** y **radiales**, cada uno con múltiples opciones de personalización.

## 🎨 Gradientes lineales
Los **gradientes lineales** permiten crear transiciones de color a lo largo de una línea recta. Se definen con `linear-gradient()`.

```css
div {
    background: linear-gradient(to right, red, blue);
}
```
- **`to right`**: Indica la dirección del gradiente (puede ser `to left`, `to bottom`, etc.).
- **Colores**: Se pueden usar dos o más colores para la transición.

### ➕ Agregar puntos de color
Podemos definir **color-stops** para controlar dónde empieza y termina cada color.

```css
div {
    background: linear-gradient(to bottom, red 20%, yellow 50%, blue 80%);
}
```
Esto crea una transición más controlada entre los colores.

### 🔄 Gradientes repetitivos
Si queremos repetir un patrón de gradiente, usamos `repeating-linear-gradient()`:

```css
div {
    background: repeating-linear-gradient(45deg, red, yellow 20px, blue 40px);
}
```
Este código genera un patrón en diagonal que se repite cada 40px.

## 🌈 Gradientes radiales
Los **gradientes radiales** generan transiciones circulares o elípticas.

```css
div {
    background: radial-gradient(circle, red, yellow, blue);
}
```
- **`circle`**: Hace que el gradiente sea un círculo perfecto.
- **Colores**: Se pueden definir múltiples transiciones.

### 📏 Ajustar la forma y posición
Podemos cambiar el tamaño y posición del gradiente:

```css
div {
    background: radial-gradient(ellipse at top, red, yellow, blue);
}
```
Aquí, el gradiente se vuelve elíptico y su centro está en la parte superior.

## 🔄 Uso de múltiples gradientes
CSS3 permite combinar **varios gradientes** en un solo elemento.

```css
div {
    background: 
        radial-gradient(circle at center, red, transparent),
        linear-gradient(to right, blue, transparent);
}
```
Esto crea un efecto donde un gradiente circular se combina con otro lineal.

## ✅ Conclusión
Los gradientes en CSS3 permiten crear efectos visuales avanzados sin imágenes. Con `linear-gradient()` y `radial-gradient()`, podemos diseñar fondos atractivos y dinámicos con solo unas líneas de código.
