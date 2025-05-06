# Web Fonts en CSS3

## 📖 Índice
- [Introducción](#introducción)
- [El uso de @font-face](#el-uso-de-font-face)
- [Formatos de fuentes compatibles](#formatos-de-fuentes-compatibles)
- [Servicios de fuentes web](#servicios-de-fuentes-web)
- [Cargando fuentes de manera eficiente](#cargando-fuentes-de-manera-eficiente)
- [Conclusión](#conclusión)

---

## Introducción
El uso de fuentes personalizadas en la web ha evolucionado gracias a la regla **@font-face** en CSS3. Esta regla permite cargar fuentes externas y usarlas en cualquier sitio web sin depender de las fuentes instaladas en el sistema del usuario.

## 📌 El uso de @font-face
La regla `@font-face` permite definir fuentes personalizadas y utilizarlas en la página. Ejemplo:

```css
@font-face {
    font-family: 'MiFuente';
    src: url('MiFuente.woff2') format('woff2'),
         url('MiFuente.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}

h1 {
    font-family: 'MiFuente', sans-serif;
}
```

Este código define una fuente llamada `MiFuente` y la aplica a todos los elementos `<h1>`.

## 🎨 Formatos de fuentes compatibles
Para asegurar la compatibilidad con todos los navegadores, se recomienda incluir varios formatos de fuentes:

- **WOFF2**: Mejor compresión y recomendado para navegadores modernos.
- **WOFF**: Soportado en la mayoría de los navegadores.
- **TTF/OTF**: Compatible pero menos eficiente en la web.
- **EOT**: Necesario para versiones antiguas de Internet Explorer.

## 🌐 Servicios de fuentes web
En lugar de alojar las fuentes manualmente, se pueden utilizar servicios de terceros como:

- **Google Fonts** ([fonts.google.com](https://fonts.google.com/)): Gratuito y fácil de integrar.
- **Adobe Fonts (Typekit)** ([fonts.adobe.com](https://fonts.adobe.com/)): Biblioteca premium con integración en Adobe.
- **Font Squirrel** ([www.fontsquirrel.com](https://www.fontsquirrel.com/)): Ofrece fuentes gratuitas para uso web.

Para utilizar Google Fonts, simplemente agrega este enlace en tu HTML:

```html
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
```

Y en tu CSS:

```css
body {
    font-family: 'Roboto', sans-serif;
}
```

## ⚡ Cargando fuentes de manera eficiente
Las fuentes externas pueden afectar el rendimiento de la web, causando el efecto **Flash of Unstyled Text (FoUT)**. Para evitarlo:

- Usa `font-display: swap;` en `@font-face` para cargar una fuente alternativa mientras se descarga la principal.
- Minimiza la cantidad de fuentes y pesos de letra cargados.
- Usa el **Web Font Loader** ([GitHub](https://github.com/typekit/webfontloader)) para manejar la carga de fuentes con JavaScript.

Ejemplo con `font-display`:

```css
@font-face {
    font-family: 'MiFuente';
    src: url('MiFuente.woff2') format('woff2');
    font-display: swap;
}
```

## ✅ Conclusión
El uso de **@font-face** y los servicios de fuentes web han revolucionado el diseño en la web, permitiendo una tipografía más rica y accesible sin depender de fuentes instaladas en los dispositivos de los usuarios.
