# Selectores en CSS3

Los selectores son fundamentales en CSS, ya que permiten aplicar estilos a elementos específicos de un documento HTML. Este capítulo explora los selectores introducidos en CSS3, brindando nuevas capacidades para diseñar páginas web de manera más flexible y precisa.

---

## 1. Selectores de Atributos
Los selectores de atributos permiten aplicar estilos basados en atributos HTML y sus valores. CSS3 introduce nuevos selectores para lograr coincidencias más flexibles.

### Selectores existentes en CSS2
1. **Selector simple de atributo:** Selecciona elementos que contienen un atributo específico.
   ```css
   E[attr] {
       color: blue;
   }
   ```
   _Ejemplo: Selecciona todos los elementos `<a>` con un atributo `rel` definido._

2. **Selector de valor exacto:** Selecciona elementos con un atributo igual a un valor.
   ```css
   E[attr="value"] {
       color: red;
   }
   ```

3. **Selector de valor parcial:** Busca un valor en una lista separada por espacios.
   ```css
   E[attr~="value"] {
       font-weight: bold;
   }
   ```

4. **Selector de atributo de lenguaje:** Selecciona atributos con valores que comienzan con un código de idioma.
   ```css
   E[lang|="es"] {
       background-color: yellow;
   }
   ```

### Nuevos Selectores en CSS3
1. **Selector de subcadena inicial:** Selecciona elementos cuyo atributo comienza con un valor específico.
   ```css
   a[href^="http"] {
       background-image: url('link.svg');
   }
   ```
   _Útil para identificar enlaces externos._

2. **Selector de subcadena final:** Selecciona elementos cuyo atributo termina con un valor específico.
   ```css
   a[href$=".pdf"] {
       background-image: url('pdf.svg');
   }
   ```
   _Permite añadir iconos basados en extensiones de archivo._

3. **Selector de subcadena arbitraria:** Selecciona elementos cuyo atributo contiene una subcadena específica en cualquier posición.
   ```css
   a[href*="example"] {
       color: green;
   }
   ```

### Combinación de selectores
Los selectores de atributos se pueden combinar para mayor especificidad.
```css
a[href^="http"][href*="secure"][href$=".com"] {
    border: 2px solid blue;
}
```
_Ejemplo: Selecciona enlaces HTTPS seguros con dominio `.com`._

---

## 2. Combinador de Hermanos Generales
CSS3 introduce el combinador de hermanos generales (`~`), que selecciona elementos hermanos precedidos por otro específico, sin necesidad de ser adyacentes.

### Ejemplo
```css
h2 ~ p {
    font-style: italic;
}
```
_Aplica estilos a todos los párrafos después de un `<h2>` en el mismo nivel del árbol DOM._

---

## 3. Compatibilidad entre Navegadores
CSS3 tiene soporte estable para los nuevos selectores en los navegadores modernos:
- **Chrome:** Compatible.
- **Firefox:** Compatible.
- **Safari:** Compatible.
- **Internet Explorer:** Limitado (no incluye IE6).

---

## Resumen
Los selectores de atributos y el combinador de hermanos generales amplían significativamente las posibilidades de diseño con CSS3. Estos nuevos métodos permiten seleccionar elementos con mayor precisión y reducen la necesidad de clases adicionales en el HTML, logrando un código más limpio y mantenible.
