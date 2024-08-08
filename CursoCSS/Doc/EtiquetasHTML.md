# Etiquetas HTML para Documentación

### Básicas
Estas etiquetas son fundamentales para cualquier documento HTML y son las primeras que se aprenden al estudiar HTML.

- `<!DOCTYPE>`: Define el tipo de documento y la versión de HTML.
- `<html>`: Raíz de un documento HTML.
- `<head>`: Contiene metadatos y enlaces a scripts y hojas de estilo.
- `<title>`: Título del documento.
- `<body>`: Contiene el contenido principal de la página.
- `<h1>` a `<h6>`: Encabezados de sección, de mayor a menor importancia.
- `<p>`: Párrafo.
- `<a>`: Enlace.
- `<img>`: Imagen.
- `<ul>`, `<ol>`, `<li>`: Listas desordenadas, ordenadas y elementos de lista.

### Intermedias
Estas etiquetas permiten una mayor interactividad y estructuración del contenido en la página web.

- `<table>`, `<tr>`, `<th>`, `<td>`: Elementos para crear tablas.
- `<form>`: Formulario para la entrada del usuario.
- `<input>`: Campo de entrada en un formulario.
- `<textarea>`: Área de texto en un formulario.
- `<button>`: Botón.
- `<select>`, `<option>`: Menús desplegables.
- `<div>`: Sección o contenedor de división en un documento.
- `<span>`: Sección en línea utilizada para agrupar o aplicar estilos.

### Avanzadas
Estas etiquetas son utilizadas para funcionalidades más específicas y avanzadas en HTML.

- `<canvas>`: Se utiliza para dibujar gráficos mediante scripting (como JavaScript).
- `<svg>`: Define gráficos vectoriales escalables directamente en HTML.
- `<audio>`, `<video>`: Incorporar sonido y vídeo.
- `<iframe>`: Incorpora otro documento HTML dentro del actual.
- `<script>`: Define un cliente de scripting, como JavaScript.
- `<link>`: Enlaza recursos externos como hojas de estilo CSS.
- `<meta>`: Proporciona metadatos que no se muestran directamente en la página web.

Cada conjunto de etiquetas permite un nivel de detalle y funcionalidad diferente en el diseño y desarrollo web. Si necesitas ejemplos específicos o más detalles sobre alguna etiqueta, ¡házmelo saber!

---

## Etiquetas Básicas

### `<!DOCTYPE>`
Define el tipo de documento HTML. Es esencial para asegurar que el navegador interprete correctamente el contenido.
```html
<!DOCTYPE html>
```

### `<html>`
Elemento raíz de un documento HTML.
```html
<html lang="en">
</html>
```

### `<head>`
Contiene metadatos, enlaces a hojas de estilo y scripts.
```html
<head>
  <title>Página de Ejemplo</title>
</head>
```

### `<body>`
Abarca todos los contenidos visibles de una página web como texto, imágenes, enlaces, etc.
```html
<body>
  <h1>Bienvenido a mi sitio web</h1>
  <p>Este es un párrafo de ejemplo.</p>
</body>
```

## Etiquetas Intermedias

### `<table>`
Usada para crear una tabla.
```html
<table>
  <tr>
    <th>Encabezado</th>
    <th>Otro Encabezado</th>
  </tr>
  <tr>
    <td>Dato 1</td>
    <td>Dato 2</td>
  </tr>
</table>
```

### `<form>`
Define un formulario para entrada del usuario.
```html
<form action="/submit" method="post">
  <label for="name">Nombre:</label>
  <input type="text" id="name" name="name">
  <input type="submit" value="Enviar">
</form>
```

### `<div>`
Contenedor genérico para agrupación de contenido.
```html
<div class="container">
  <p>Este div contiene un párrafo para estilizar.</p>
</div>
```

## Etiquetas Avanzadas

### `<canvas>`
Permite dibujar gráficos a través de scripting.
```html
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;">
  Tu navegador no soporta el elemento canvas.
</canvas>
```

### `<svg>`
Define gráficos vectoriales escalables en línea.
```html
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" stroke="black" stroke-width="3" fill="red" />
</svg>
```

### `<iframe>`
Incorpora otro documento HTML dentro del actual.
```html
<iframe src="https://www.example.com" width="300" height="200">
  Tu navegador no soporta iframes.
</iframe>
```

---

Estos ejemplos te proporcionan una guía básica de cómo incluir y describir las etiquetas HTML en un archivo Markdown para documentación o notas educativas. Cada sección está dividida por niveles de complejidad, facilitando la referencia y el aprendizaje. Si necesitas agregar más detalles o más etiquetas, ¡déjame saber!