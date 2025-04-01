# Capítulo 14: Transiciones y Animaciones en CSS3

## 📌 Introducción
Las transiciones y animaciones en CSS3 permiten agregar efectos visuales a los elementos sin necesidad de JavaScript. Las **transiciones** ocurren cuando una propiedad cambia de valor, mientras que las **animaciones** permiten crear movimientos más complejos con diferentes etapas.

---

## 🎭 Transiciones en CSS3

### 🔹 1. Propiedades de Transición
Las transiciones se definen con la propiedad `transition` y pueden configurarse mediante cuatro subpropiedades:

- **`transition-property`**: Define la propiedad CSS que se animará.
- **`transition-duration`**: Determina la duración del efecto.
- **`transition-timing-function`**: Controla la velocidad del cambio (ejemplo: `ease`, `linear`, `ease-in-out`).
- **`transition-delay`**: Especifica un retraso antes de que comience la transición.

Ejemplo:

```css
div {
    background-color: blue;
    transition: background-color 2s ease-in-out;
}
div:hover {
    background-color: red;
}
```

### 🔹 2. Transiciones Múltiples
Podemos aplicar transiciones a varias propiedades simultáneamente:

```css
div {
    width: 100px;
    height: 100px;
    transition: width 2s, height 2s;
}
div:hover {
    width: 200px;
    height: 200px;
}
```

---

## 🎬 Animaciones en CSS3

Las animaciones permiten definir múltiples estados intermedios en un efecto visual.

### 🔹 1. Uso de `@keyframes`
La regla `@keyframes` define los pasos de una animación.

```css
@keyframes mover {
    0% { transform: translateX(0); }
    50% { transform: translateX(100px); }
    100% { transform: translateX(0); }
}
```

### 🔹 2. Propiedades de Animación
Las animaciones se configuran con la propiedad `animation`, que incluye:

- **`animation-name`**: Nombre de la animación.
- **`animation-duration`**: Duración del efecto.
- **`animation-timing-function`**: Tipo de aceleración.
- **`animation-delay`**: Retraso antes de iniciar la animación.
- **`animation-iteration-count`**: Número de repeticiones (`infinite` para repetirse siempre).
- **`animation-direction`**: Dirección de la animación (`normal`, `reverse`, `alternate`).

Ejemplo:

```css
div {
    animation: mover 3s infinite alternate;
}
```

### 🔹 3. Múltiples Animaciones
Se pueden aplicar varias animaciones separadas por comas:

```css
div {
    animation: mover 3s infinite, girar 2s infinite;
}
```

---

## 📌 Conclusión
Las transiciones y animaciones en CSS3 permiten agregar efectos dinámicos a los sitios web sin necesidad de JavaScript. Usadas correctamente, mejoran la experiencia del usuario de manera atractiva y eficiente.
