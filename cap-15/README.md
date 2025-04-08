# Flexible Box Layout (Flexbox)

## Índice

- [Introducción](#introducción)
- [Declarando el Modelo de Caja Flexible](#declarando-el-modelo-de-caja-flexible)
- [Alineación con Flexbox](#alineación-con-flexbox)
  - [Dirección de los Elementos](#dirección-de-los-elementos)
  - [Alineación en el Eje Principal](#alineación-en-el-eje-principal)
  - [Alineación en el Eje Secundario](#alineación-en-el-eje-secundario)
- [Cambiando el Orden de los Elementos](#cambiando-el-orden-de-los-elementos)
- [Tamaño Flexible de los Elementos](#tamaño-flexible-de-los-elementos)
  - [Crecimiento de los Elementos](#crecimiento-de-los-elementos)
  - [Reducción de Tamaño](#reducción-de-tamaño)
  - [Tamaño Inicial](#tamaño-inicial)
- [Envolver Elementos en Varias Líneas](#envolver-elementos-en-varias-líneas)
- [Compatibilidad con Navegadores](#compatibilidad-con-navegadores)
- [Conclusión](#conclusión)

---

## Introducción

Flexbox es un modelo de diseño que facilita la alineación y distribución de elementos en una página web sin la necesidad de usar flotantes o posicionamiento complicado. Se adapta automáticamente al espacio disponible, haciendo que los elementos crezcan o se reduzcan según sea necesario.

## Declarando el Modelo de Caja Flexible

Para usar Flexbox, hay que definir un contenedor flexible. Esto se logra con la propiedad `display: flex;` en el elemento padre:

```css
.container {
  display: flex;
}
```

Esto convierte a los elementos hijos en elementos flexibles que pueden ajustarse automáticamente en el espacio disponible.

## Alineación con Flexbox

### Dirección de los Elementos
Por defecto, los elementos dentro de un contenedor flexible se organizan en una fila. Se puede cambiar esta dirección con `flex-direction`:

```css
.container {
  flex-direction: column;
}
```

Opciones:
- `row` (predeterminado): elementos en fila.
- `column`: elementos en columna.
- `row-reverse`: invierte el orden de la fila.
- `column-reverse`: invierte el orden de la columna.

### Alineación en el Eje Principal
Se controla con `justify-content` y define cómo se distribuyen los elementos a lo largo del eje principal:

```css
.container {
  justify-content: space-between;
}
```

Opciones:
- `flex-start`: alinea los elementos al inicio.
- `flex-end`: alinea los elementos al final.
- `center`: centra los elementos.
- `space-between`: espacio igual entre los elementos.
- `space-around`: espacio igual alrededor de los elementos.

### Alineación en el Eje Secundario
Se maneja con `align-items`, que controla cómo se alinean los elementos en el eje perpendicular al principal:

```css
.container {
  align-items: center;
}
```

Opciones:
- `flex-start`: elementos alineados en la parte superior.
- `flex-end`: alineados en la parte inferior.
- `center`: alineados en el centro.
- `stretch`: estira los elementos para ocupar todo el espacio disponible.

## Cambiando el Orden de los Elementos

Flexbox permite cambiar el orden de los elementos sin modificar el HTML, usando la propiedad `order`:

```css
.item-1 {
  order: 2;
}
.item-2 {
  order: 1;
}
```

Los elementos se organizarán en base a sus valores de `order`, de menor a mayor.

## Tamaño Flexible de los Elementos

### Crecimiento de los Elementos
Se usa `flex-grow` para que un elemento crezca y ocupe el espacio disponible:

```css
.item {
  flex-grow: 1;
}
```

Un elemento con `flex-grow: 2;` crecerá el doble que uno con `flex-grow: 1;`.

### Reducción de Tamaño
Si los elementos no caben en el contenedor, `flex-shrink` define cuánto debe reducirse cada uno:

```css
.item {
  flex-shrink: 1;
}
```

### Tamaño Inicial
Se establece con `flex-basis`, que define el tamaño inicial antes de aplicar crecimiento o reducción:

```css
.item {
  flex-basis: 100px;
}
```

## Envolver Elementos en Varias Líneas
Si hay demasiados elementos en un contenedor, se pueden acomodar en varias líneas con `flex-wrap`:

```css
.container {
  flex-wrap: wrap;
}
```

Opciones:
- `nowrap` (predeterminado): todos los elementos en una sola línea.
- `wrap`: los elementos se reparten en múltiples líneas si es necesario.
- `wrap-reverse`: igual que `wrap`, pero en orden inverso.

## Compatibilidad con Navegadores
Flexbox es compatible con todos los navegadores modernos, aunque versiones antiguas de Internet Explorer requieren prefijos específicos.

## Conclusión
Flexbox es una herramienta poderosa y flexible para crear diseños dinámicos y responsivos sin esfuerzo. Con sus propiedades, se pueden alinear y distribuir elementos de manera eficiente, mejorando la experiencia de desarrollo y diseño web.
