# GLOSARIO
En esta parte explicare cada parte del codigo y la funcion a desarrollar para su funcionamento.

---

## Estructura

Está compuesto por varias secciones HTML:

### `<!DOCTYPE html>` 
Nos indica que es un archivo HTML5.

### `<html lang="es">`  
Nos ayuda a definir el idioma del documento.

---

## `<head>` -Es la Cabecera del documento

Ayuda a configurar la información básica de la pagina:

- `<meta charset="UTF-8">`: Asegura que los caracteres funcionen correctamente.
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Hace que la pagina se adapte de manera responsiva lo cual hara que esta se vea bien en cualquier dispositivo donde se este usando.
- `<title>Glorario</title>`: Es el título que aparecera en la pestaña del navegador.
- `<link rel="stylesheet" href="estilo.css">`: Nos ayuda a conectar un archivo CSS para aplicar los estilos a la pagina.

---

##  `<header>` - Encabezado principal

Es el que contiene el título y el centrado de la página:

- Glosario de Términos sobre Análisis y Desarrollo de Software

## Formulario para cambiar de página (A-M / N-Z)
Se muestra un formulario que nos permite ir a la otra pagina del glosario:

- La cual nos muestra un menu desplegable y nos lleva a la pagina escogida.


<form action="" method="get">
  <label for="section">Ir a la página:</label>
  <select id="section" name="section" onchange="location = this.value;">
    <option value="">Seleccione la página</option>
    <option value="index.html">A - M</option>
    <option value="pagina_2.html">N - Z</option>
  </select>
</form>


---


# `<main>` Contenido del glosario

Aquí nos muestra todo el glosario dividido por letras. En la cual cada sección tiene:

- Un título con la letra, como (A) y nos muestra una lista de terminos con la definicion de esa letra la cual se encuentra en una lista no ordenada.

## Ejemplo:

<section id="A">
  <h2>A</h2>
  <ul>
    <li><strong>Algoritmo:</strong> Conjunto ordenado de pasos o instrucciones para resolver un problema.</li>
    <li><strong>Análisis de Requisitos:</strong> Proceso de identificar lo que el sistema debe hacer.</li>
  </ul>
</section>

# `<footer>` - Pie de página
Es la parte que da cierre a la pagina mostrando el año de creación: 

- <footer>
  <p>© 2025 </p>
</footer>




