# Capítulo 11

## 🎨 Gradientes Lineales
Un gradiente lineal es aquel donde los colores cambian a lo largo de una línea recta.

### 🔹 1. Creación de un Gradiente Lineal
Se define con la función `linear-gradient()` dentro de `background-image`.

```css
background-image: linear-gradient(to right, blue, white);
```

Esto genera un degradado de azul a blanco de izquierda a derecha.

### 🔹 2. Dirección del Gradiente
Podemos especificar la dirección del degradado:

- **Palabras clave**: `to top`, `to bottom`, `to left`, `to right`.
- **Grados**: Se pueden usar valores en grados (`deg`).

```css
background-image: linear-gradient(45deg, red, yellow);
```

Esto crea un degradado de rojo a amarillo en un ángulo de 45 grados.

### 🔹 3. Múltiples Paradas de Color
Podemos agregar más colores intermedios con puntos de parada:

```css
background-image: linear-gradient(to right, red, blue 50%, green);
```

El color azul aparecerá en el 50% del ancho del degradado.

### 🔹 4. Gradientes Lineales Repetitivos
Podemos repetir un gradiente con `repeating-linear-gradient()`:

```css
background-image: repeating-linear-gradient(45deg, black, white 10px);
```

Esto genera franjas diagonales alternando negro y blanco cada 10px.

---

## 🌈 Gradientes Radiales
Los gradientes radiales parten de un punto central y se expanden en círculo o elipse.

### 🔹 1. Creación de un Gradiente Radial
Se define con la función `radial-gradient()`:

```css
background-image: radial-gradient(circle, red, yellow, green);
```

Esto crea un degradado circular con transiciones entre rojo, amarillo y verde.

### 🔹 2. Posicionamiento y Tamaño
Podemos especificar la posición del centro del degradado y su tamaño:

```css
background-image: radial-gradient(circle at top left, purple, orange);
```

### 🔹 3. Múltiples Paradas de Color
Podemos usar valores específicos para definir en qué punto del gradiente aparece cada color:

```css
background-image: radial-gradient(circle, red 20%, blue 50%, green 80%);
```

### 🔹 4. Gradientes Radiales Repetitivos
Similar a los lineales, podemos repetir gradientes radiales:

```css
background-image: repeating-radial-gradient(circle, black, white 20%);
```

Esto crea anillos concéntricos en blanco y negro.

---

## 🖌️ Múltiples Gradientes
Podemos combinar múltiples gradientes en una misma propiedad `background-image` separándolos con comas:

```css
background-image: 
  linear-gradient(to bottom, rgba(0,0,0,0.5), transparent),
  radial-gradient(circle at top, yellow, transparent);
```

Esto superpone un gradiente lineal oscuro con un gradiente radial amarillo.

---

## 📌 Conclusión
Los gradientes en CSS3 son una herramienta poderosa para mejorar el diseño web sin necesidad de imágenes. Permiten crear fondos atractivos y patrones sofisticados de manera eficiente y flexible.
