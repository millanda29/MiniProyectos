### Módulo 3: CSS Grid

CSS Grid es un poderoso sistema de layout bidimensional que te permite controlar tanto las filas como las columnas, facilitando la creación de diseños complejos de manera intuitiva y eficaz.

#### Conceptos Fundamentales de CSS Grid
1. **Contenedor Grid**: Al igual que en Flexbox, defines un contenedor grid aplicando `display: grid;` o `display: inline-grid;` en un elemento.
   ```css
   .grid-container {
       display: grid;
   }
   ```

2. **Definir Filas y Columnas**: Puedes especificar el tamaño de las filas y columnas utilizando `grid-template-rows` y `grid-template-columns`.
   ```css
   .grid-container {
       display: grid;
       grid-template-columns: 1fr 2fr 1fr; /* 3 columnas */
       grid-template-rows: 100px auto 100px; /* 3 filas */
   }
   ```

3. **Posicionamiento de Elementos**: CSS Grid te permite colocar elementos en cualquier celda del grid y abarcar múltiples filas o columnas.
   ```css
   .item1 {
       grid-column: 1 / 3; /* Ocupa desde la primera hasta antes de la tercera columna */
       grid-row: 1; /* Ocupa la primera fila */
   }
   ```

4. **Alineación de Elementos**: Similar a Flexbox, puedes alinear elementos dentro de sus celdas con `justify-items`, `align-items`, `justify-content`, y `align-content`.
   ```css
   .grid-container {
       display: grid;
       align-items: center; /* Alinea verticalmente */
       justify-items: center; /* Alinea horizontalmente */
   }
   ```

#### Ejercicio Práctico: Crear un Layout Complejo con CSS Grid
Construyamos un layout más complejo que incluya un área de header, sidebar, contenido principal y footer.

1. **Modifica tu `index.html`** para adaptarlo a un diseño de grid:
   ```html
   <div class="grid-container">
       <header>Header</header>
       <aside>Sidebar</aside>
       <main>Main Content</main>
       <footer>Footer</footer>
   </div>
   ```

2. **Añade estilos CSS** para configurar el grid:
   ```css
   .grid-container {
       display: grid;
       grid-template-columns: 200px 1fr; /* Sidebar y contenido */
       grid-template-rows: 100px auto 100px; /* Header, contenido, footer */
       gap: 10px; /* Espacio entre las celdas del grid */
       height: 100vh; /* Altura total de la ventana de visualización */
   }

   header, footer {
       grid-column: 1 / -1; /* Ocupan toda la anchura */
       background-color: #ccc;
       text-align: center;
       padding: 20px;
   }

   aside {
       background-color: #f0f0f0;
       padding: 20px;
   }

   main {
       background-color: #fff;
       padding: 20px;
   }
   ```

3. **Observa el Resultado**: Abre tu página en el navegador para ver cómo CSS Grid organiza los elementos en un patrón de layout complejo.

CSS Grid es ideal para crear diseños web que necesitan estructuras más rígidas y precisas comparado con Flexbox, que es más adecuado para componentes de layout lineales.
