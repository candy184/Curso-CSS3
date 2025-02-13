# Pseudo-clases y Pseudo-elementos en CSS3

## 📖 Índice
- [Introducción](#introducción)
- [Pseudo-clases](#-pseudo-clases)
  - [Pseudo-clases estructurales](#1️⃣-pseudo-clases-estructurales)
  - [Otras pseudo-clases importantes](#2️⃣-otras-pseudo-clases-importantes)
  - [Pseudo-clases para formularios](#3️⃣-pseudo-clases-para-formularios)
- [Pseudo-elementos](#-pseudo-elementos)
- [Conclusión](#-conclusión)

---

## Introducción
CSS3 ha introducido mejoras significativas en la forma en que seleccionamos y estilizamos elementos en una página web. Este capítulo cubre las **pseudo-clases** y **pseudo-elementos**, que permiten aplicar estilos avanzados sin necesidad de modificar el HTML.

## 📌 Pseudo-clases
Las pseudo-clases nos permiten aplicar estilos a elementos en función de su estado, posición o interacción con el usuario.

### 1️⃣ Pseudo-clases estructurales
Estas nos ayudan a seleccionar elementos basados en su ubicación en el árbol DOM.

- **`:nth-child(n)`**: Selecciona elementos basados en su posición en relación con su padre.
  ```css
  p:nth-child(2) {
      color: blue;
  }
  ```
  Aplica color azul al segundo párrafo dentro de un contenedor.

- **`:nth-of-type(n)`**: Funciona como `nth-child`, pero solo cuenta elementos de un mismo tipo.

- **`:first-child` y `:last-child`**: Seleccionan el primer y último hijo de un contenedor.
  ```css
  p:first-child {
      font-weight: bold;
  }
  ```
  El primer párrafo dentro de un div tendrá texto en negrita.

- **`:only-child`**: Selecciona un elemento si es el único hijo de su contenedor.

### 2️⃣ Otras pseudo-clases importantes

- **`:target`**: Permite estilizar un elemento cuando es referenciado por un enlace.
  ```css
  #seccion1:target {
      background-color: yellow;
  }
  ```
  Si se accede a `#seccion1` a través de un enlace, su fondo se vuelve amarillo.

- **`:empty`**: Selecciona elementos sin contenido (ni texto ni hijos).

- **`:not(selector)`**: Excluye elementos que coincidan con el selector dado.
  ```css
  div:not(.especial) {
      border: 1px solid black;
  }
  ```
  Aplica un borde negro a todos los `div` que **no** tengan la clase `especial`.

### 3️⃣ Pseudo-clases para formularios
CSS3 permite estilizar formularios según su estado.

- **`:required` y `:optional`**: Seleccionan campos obligatorios u opcionales.
- **`:valid` y `:invalid`**: Aplican estilos según la validez del campo.
- **`:in-range` y `:out-of-range`**: Determinan si un valor está dentro del rango permitido.
  ```css
  input:valid {
      border: 2px solid green;
  }
  ```
  Un campo con un valor válido tendrá un borde verde.

## 🎨 Pseudo-elementos
Los pseudo-elementos permiten estilizar partes específicas de un elemento sin necesidad de modificar el HTML.

- **`::first-line`**: Aplica estilos a la primera línea de un texto.
- **`::first-letter`**: Estiliza la primera letra de un texto.
  ```css
  p::first-letter {
      font-size: 2em;
      color: red;
  }
  ```
  La primera letra de un párrafo será roja y más grande.

- **`::before` y `::after`**: Añaden contenido antes o después de un elemento.
  ```css
  h1::before {
      content: "🔥 ";
  }
  ```
  Antes de cada `h1`, se agregará un emoji de fuego.

- **`::selection`**: Estiliza el texto seleccionado por el usuario.
  ```css
  ::selection {
      background: black;
      color: white;
  }
  ```
  El texto seleccionado tendrá fondo negro y letras blancas.

## ✅ Conclusión
Las pseudo-clases y pseudo-elementos permiten un control detallado del estilo sin necesidad de alterar la estructura HTML. CSS3 nos ofrece herramientas poderosas para mejorar la apariencia y la interacción de los sitios web de manera eficiente.
