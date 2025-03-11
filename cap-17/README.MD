# CSS Grid Layout

## Índice

- [Introducción](#introducción)
- [Conceptos Básicos de CSS Grid](#conceptos-básicos-de-css-grid)
  - [Definiendo una Grid](#definiendo-una-grid)
  - [Filas y Columnas](#filas-y-columnas)
  - [Espaciado entre Elementos](#espaciado-entre-elementos)
- [Alineación y Distribución](#alineación-y-distribución)
  - [Justificación y Alineación](#justificación-y-alineación)
  - [Uso de grid-auto-flow](#uso-de-grid-auto-flow)
- [Áreas de Grid](#áreas-de-grid)
- [Conclusión](#conclusión)

---

## Introducción

CSS Grid Layout es un sistema de diseño bidimensional que permite crear estructuras de página complejas con facilidad. A diferencia de Flexbox, que se enfoca en una dimensión (horizontal o vertical), Grid maneja ambas dimensiones simultáneamente.

## Conceptos Básicos de CSS Grid

### Definiendo una Grid
Para convertir un contenedor en una cuadrícula, se usa display: grid;:

css
.container {
  display: grid;
}


### Filas y Columnas
Se pueden definir filas y columnas usando grid-template-columns y grid-template-rows:

css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 100px 200px;
}


### Espaciado entre Elementos
La propiedad gap define el espacio entre filas y columnas:

css
.container {
  gap: 10px;
}


## Alineación y Distribución

### Justificación y Alineación
Grid permite alinear contenido dentro del contenedor usando justify-items y align-items:

css
.container {
  justify-items: center;
  align-items: center;
}


### Uso de grid-auto-flow
Controla el flujo automático de los elementos en la cuadrícula:

css
.container {
  grid-auto-flow: row;
}


## Áreas de Grid
Se pueden definir áreas específicas dentro de la cuadrícula para ubicar elementos:

css
.container {
  grid-template-areas: 
    "header header"
    "sidebar main";
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main { grid-area: main; }


## Conclusión
CSS Grid es una herramienta poderosa para diseñar interfaces web flexibles y organizadas. Permite crear diseños complejos con menos código y mayor control sobre la disposición de los elementos en pantalla.
