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
            border: 5px solid navy;
            box-sizing: border-box;
            background-color: lightblue;
            height: 30vh; 
            padding: 1rem;
            width: 50vw;
        }

        .dynamic-box {
            background-color: coral;
            height: max-content;
            padding: 10px;
            text-align: center;
            width: calc(100% - 20px);
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
