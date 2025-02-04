# Capítulo 2: Consultas de Medios (Media Queries)

## Introducción
Las consultas de medios son una de las características más revolucionarias de CSS3. Permiten adaptar el diseño y la presentación de una página web según el dispositivo o las características de la pantalla del usuario, como el tamaño o la orientación. Este enfoque asegura que las webs sean accesibles y óptimas para cualquier dispositivo, ya sea un monitor grande o un teléfono inteligente.

## Ventajas de las Consultas de Medios
1. **Diseños Adaptativos**: Permiten ajustar el contenido para diferentes dispositivos sin necesidad de crear versiones separadas del sitio.
2. **Facilidad de Implementación**: Evitan scripts complicados para detectar navegadores.
3. **Eficiencia**: Reducen la carga de trabajo y los problemas de mantenimiento al centralizar los estilos.

Por ejemplo, un menú horizontal en escritorio puede transformarse en uno vertical en móviles.

```css
ul { overflow: hidden; }
li { float: left; }
@media (max-width: 600px) {
  li { float: none; }
}
```

## Sintaxis
Las consultas de medios pueden usarse de tres formas:
1. **Enlace externo**:
   ```html
   <link href="estilo.css" rel="stylesheet" media="screen and (max-width: 600px)">
   ```
2. **@import en CSS**:
   ```css
   @import url('estilo.css') screen and (max-width: 600px);
   ```
3. **Reglas en el mismo CSS**:
   ```css
   @media screen and (max-width: 600px) {
       body { font-size: 14px; }
   }
   ```

## Características de Medios
1. **Ancho y Alto**:
   Permiten definir estilos según el tamaño del navegador.
   ```css
   @media (max-width: 480px) {
       body { background-color: lightgray; }
   }
   ```

2. **Relación de Aspecto**:
   Aplica reglas según la proporción de ancho y alto de la pantalla.
   ```css
   @media (aspect-ratio: 16/9) {
       video { width: 100%; }
   }
   ```

3. **Resolución (DPR)**:
   Diseños optimizados para pantallas de alta densidad.
   ```css
   @media (min-resolution: 2dppx) {
       img { content: url('imagen-hd.png'); }
   }
   ```

4. **Orientación**:
   Cambia estilos según si la pantalla está en modo retrato o paisaje.
   ```css
   @media (orientation: portrait) {
       nav { display: none; }
   }
   ```

## Desarrollo "Mobile-First"
El enfoque "mobile-first" implica diseñar primero para pantallas pequeñas y luego agregar estilos para dispositivos más grandes.
```css
/* Estilos básicos */
body {
    font-size: 14px;
}

/* Estilos para pantallas más grandes */
@media (min-width: 600px) {
    body {
        font-size: 16px;
    }
}
```

## Soporte en Navegadores
Las consultas de medios tienen soporte en todos los navegadores modernos, incluyendo Chrome, Firefox, Safari e Internet Explorer desde la versión 9.

## Conclusión
Las consultas de medios son esenciales para el diseño web moderno, permitiendo sitios responsivos que se adaptan a cualquier dispositivo. Son una herramienta poderosa y versátil que, combinada con buenas prácticas como "mobile-first", ofrece experiencias de usuario óptimas.
