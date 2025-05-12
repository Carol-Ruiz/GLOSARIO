# GLOSARIO
En esta parte explicaré cada sección del código y la función que cumple para su funcionamiento.


---

## Estructura

La estructura está compuesta por varias secciones HTML:

-  `<!DOCTYPE html>` 
Nos indica que es un archivo HTML5.

- `<html lang="es">`  
Nos ayuda a definir el idioma del documento.

---

## `<head>` Metadatos y Recursos del Documento

Ayuda a configurar la información básica de la pagina:

- `<meta charset="UTF-8">`: Asegura que los caracteres funcionen correctamente.
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Hace que la página se adapte de manera responsiva lo cual hará que esta se vea bien en cualquier dispositivo donde se este usando.
- `<title>Glosario</title>`: Es el título que aparecera en la pestaña del navegador.
- `<link rel="stylesheet" href="estilo.css">`: Nos ayuda a conectar un archivo CSS para aplicar los estilos a la página.

---

##  `<header>` Encabezado principal
```
<header>
  <center><h1>Glosario de Términos sobre Análisis y Desarrollo de Software</h1></center>
</header>
```

- `<header>`: Es una etiqueta semántica que agrupa el encabezado del sitio.
- `<center>`: Ayuda a alinear el título en el centro.
- `<h1>`: Contiene el título principal de la página: (Glosario de Términos sobre Análisis y Desarrollo de Software).

## Formulario para cambiar de página (A-M / N-Z)
Se muestra un formulario que nos permite ir a la otra página del glosario:

- La cual nos muestra un menú  desplegable y nos lleva a la página escogida.

```
<form action="" method="get">
  <label for="section">Ir a la página:</label>
  <select id="section" name="section" onchange="location = this.value;">
    <option value="">Seleccione la página</option>
    <option value="index.html">A - M</option>
    <option value="pagina_2.html">N - Z</option>
  </select>
</form>
```

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
```
<main>
  <section id="A">
    <h2>A</h2>
    <ul>
      <li><strong>...</strong> Definición...</li>
    </ul>
  </section>
  ...
```

- `<main>`: Es un contenedor semántico del contenido principal del sitio web.

- `<section>`: Sirve para agrupar cada letra del abecedario con sus términos.

- `id="A"`: Sirve para crear anclas que permiten que el menú de las letras funcione de manera adecuada.

- `<h2>`: Se usa para agregar un subtítulo para cada sección en este caso agrega la letra del abecedario.

- `<ul>`: Se usa para crear una lista no ordenada para  mostrar los términos.

- `<li>`: Se usa para representar cada término de la lista.

- `<strong>`: Sirve para resaltar el término destacado.

# `<footer>` - Pie de página
Es la parte que da cierre a la página, mostrando el año de creación: 

```
<footer>
  <p>© 2025 </p>
</footer>
```

<footer>
  <p>© 2025 </p>
</footer>


- `<footer>`: Es un contenedor semántico que representa el pie de página.

- `<p>`:Se utiliza para mostrar el año. 

---

## EXPLICACIÓN DEL CSS

Aca describire el funcionamento del archivo `estilo.css`, el cual define el diseño visual. 

---

## Estilos Generales

### `body`
Sirve para dar una apariencia amigable y legible tanto para el sitio como para el usuario.
```
body {
    font-family: 'Arial', sans-serif;
    background-color: #ebcbe4;
    color: #333;
    line-height: 1.6;
    padding: 20px;
}
```
- `font-family`:Establece una fuente tipográfica; en este caso se usa Arial.
- `background-color`:define el color de fondo de la página.
- `color`: Es el color del texto principal.
- `line-height`: Sirve para dar un espaciado entre las lineas del texto.
- `padding`: sirve para dar un espacio interno a los bordes del body ayudando que el contenido no quede pegado en los extremos de la pantalla.

### `Header`

```
header {
    background: #443053;
    color: #d38080;
    padding: 10px;
    text-align: center;
}
```

- `background:`Define el color de fondo del encabezado, ayudando a crear contraste.
- `color:`Es el color del texto que resalta sobre el fondo.
- `padding:`Le da espacio interno al texto.
- `text-align:` Sirve para centrar el contenido que tiene el encabezado. 

### `h1 (Título principal)`
```
h1 {
    font-family: 'Permanent Marker'; 
    font-size: 2.2em; 
    font-weight: bold; 
    color: #d398ee;
    letter-spacing: 1px; 
}
```
- `font-family`: Es la fuente que personaliza el titulo.
- `font-size`: Se usa para aumentar el tamaño del texto..
- `font-weight`: Se usa para aumentar el grosor del texto.
`color`: Le da el color al título.
`letter-spacing`: Sirve para darle un espacio a las letras y mejorar el estilo visual.

## Navegación (nav, .navigation-form, y select)

### `nav, .navigation-form`
Sirve para centrar los formularios de navegación y les da un espacio vertical para separarlos del resto del contenido. 
```
nav, .navigation-form {
    text-align: center;
    margin: 20px 0;
}
```
### `nav select, .navigation-form select`

- Ayuda a darle un estilo uniforme a los `<select>`:

- `padding y font-size:` Mejoran la usabilidad.

- `margin:` Separación entre elementos.

- `border-radius:` Bordes redondeados, visualmente más agradables.

- `border:` Color acorde con el tema.

- `outline:` Evita borde predeterminado del navegador.

- `transition:` Suaviza los cambios de estilo.


```
nav select, .navigation-form select {
    padding: 6px;
    font-size: 1em;
    margin: 10px;
    border-radius: 5px;
    border: 1px solid #989dec;
    outline: none;
    transition: all 0.3s ease;
}

```
Le da un color al borde al darle clic.
```
nav select:focus, .navigation-form select:focus {
    border-color: #4A90E2;
}

```

## `main` 
```
main {
    display: grid;
    grid-template-columns: 1fr;
    gap: 20px;
}
```
- `display:`Permite que las secciones se organizen verticalmente.

- `grid-template-columns:` Sirve para que la columna ocupe el ancho disponible.

- `gap:`  Sirve para dar espacio entre las secciones del glosario.

## `section`

```
section {
    background-color: #c6a8ec;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    padding: 20px;
}
```

- `background-color:` Ayuda a distinguir cada sección del glosario.

- `border-radius:` Sirve para redondear las esquinas en el diseño.

- `box-shadow:` Se usa para sombrear y generar profundidad entre las secciones.

- `padding:` Ayuda a dar espacio interno para una mejor comodidad visual.

## `h2`

```
section h2 {
    color: #2b1a7a;
    margin-bottom: 10px;
}

```
- `color:` Le da color a los  títulos de cada  término .

- `margin-bottom:`Le da espacio al titulo y la letra entre los términos.

## `Lista de términos`
Se usa para eliminar las viñetas de las listas.
```
section ul {
    list-style-type: none;
}

```
Genera un espacio entre los términos del glosario

```
section li {
    margin-bottom: 10px;
}
```
Sirve para resaltar el término del glosario en negrita.

```
section li strong {
    color: #262036;
    font-size: 1.1em;
}
```
## `Footer`
```
footer {
    text-align: center;
    margin-top: 40px;
    padding: 20px;
    background-color: #443053;
    color: #d398ee;
    font-size: 1em;
    border-radius: 8px;
}
```

- `text-align:` Sirve para centrar el texto en la página.
- `margin-top:` Sirve para separar el contenido principal 
- `padding:` Sirve para darle un espaciado interno.
- `background-color y color:` Sirve para darle el mismo color visual que el del header.
- `border-radius:` Sirve para que los bordes estén redondeados.