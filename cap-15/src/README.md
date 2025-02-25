<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejemplo de Valores y Tamaño en CSS</title>
    <style>
        /* Uso de unidades relativas */
        html {
            font-size: 16px;
        }

        .container {
            width: 50vw; /* 50% del ancho de la ventana del navegador */
            height: 30vh; /* 30% de la altura de la ventana del navegador */
            background-color: lightblue;
            padding: 1rem; /* Relativo al tamaño de la fuente raíz */
            border: 5px solid navy;
            box-sizing: border-box; /* Incluye padding y borde en el tamaño total */
        }

        .dynamic-box {
            width: calc(100% - 20px); /* Calcula el ancho restando 20px */
            height: max-content; /* Toma el tamaño máximo del contenido */
            background-color: coral;
            padding: 10px;
            text-align: center;
        }
    </style>
</head>
<body>

    <div class="container">
        <div class="dynamic-box">
            ¡Este cuadro usa tamaños dinámicos!
        </div>
    </div>

</body>
</html>
