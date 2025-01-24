# Introducción a CSS3

### 1. ¿Qué es CSS3 y cómo surgió?
CSS3 es una evolución de CSS2.1 que introduce nuevas funcionalidades para estilizar páginas web. Su desarrollo comenzó en 1998, pero se consolidó con la necesidad de superar inconsistencias en los navegadores.

### 2. CSS3 es Modular
Para facilitar el desarrollo, CSS3 se dividió en módulos independientes, como "Media Queries" o "Selectores". Esto permite implementar y actualizar funcionalidades de forma aislada.

### 3. No existe "CSS3"
El término CSS3 se usa como referencia a los módulos desarrollados después de CSS2.1. Cada módulo tiene un nivel que indica su madurez, como "Selectores Nivel 3".

### 4. Proceso de Recomendación de los Módulos
El desarrollo de CSS3 sigue un proceso de revisión en varias etapas:
- **Borrador de Trabajo:** Documento inicial para revisión.
- **Recomendación Candidata:** Implementación por navegadores.
- **Recomendación Propuesta:** Revisión final antes de aprobación.
- **Recomendación:** Versión oficial del W3C.

### 5. Prefijos de Navegadores
Los prefijos (`-webkit-`, `-moz-`, etc.) permitieron experimentar con propiedades nuevas. Aunque útiles, su uso excesivo creó problemas de compatibilidad.

### 6. Introducción a la Sintaxis
La estructura básica de CSS3 es:
```css
selector {
    propiedad: valor;
}
```

### Ejemplo Práctico
```css
.box {
    -webkit-border-radius: 10px; 
    -moz-border-radius: 10px;  
    border-radius: 10px;       
}
```
---

## Ejemplo Completo
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta 
    name="viewport" 
    content="width=device-width, initial-scale=1.0">
    <title>Ejemplo CSS3</title>
    <style>
        .button {
            background-color: #6200ea;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .button:hover {
            background-color: #3700b3;
        }
    </style>
</head>
<body>
    <button class="button">Haz clic aquí</button>
</body>
</html>
```

Este ejemplo utiliza una transición suave y esquinas redondeadas, características destacadas de CSS3.

---

## Conclusión
CSS3 es una herramienta poderosa y en constante evolución que permite crear experiencias web dinámicas y atractivas. Su estructura modular facilita la adopción de nuevas funcionalidades sin comprometer la compatibilidad.
