### Módulo 2: Flexbox

Flexbox es un módulo de diseño CSS muy poderoso y flexible, perfecto para crear layouts de página complejos de una manera más sencilla y predecible. Vamos a aprender los conceptos fundamentales y practicar con ejemplos.

#### Conceptos Fundamentales de Flexbox
1. **Contenedor Flex**: Declaras un contenedor flex usando `display: flex;` o `display: inline-flex;` en el elemento padre. Esto hará que todos sus hijos directos se comporten como ítems flexibles.
   ```css
   .container {
       display: flex;
   }
   ```

2. **Dirección Flex**: Puedes definir la dirección de los ítems flexibles con la propiedad `flex-direction`.
   - `row` (default): los ítems se colocan en una línea horizontal.
   - `column`: los ítems se apilan verticalmente.
   ```css
   .container {
       display: flex;
       flex-direction: row;
   }
   ```

3. **Justificación y Alineación**: Controla la distribución de ítems dentro del contenedor usando `justify-content` y `align-items`.
   - `justify-content`: alinea ítems horizontalmente y acepta valores como `flex-start`, `flex-end`, `center`, `space-between`, y `space-around`.
   - `align-items`: alinea ítems verticalmente y acepta valores como `flex-start`, `flex-end`, `center`, `stretch`, y `baseline`.
   ```css
   .container {
       display: flex;
       justify-content: space-between;
       align-items: center;
   }
   ```

4. **Flexibilidad de Ítems**: La propiedad `flex` en los ítems controla cómo cada uno crecerá o se encogerá en relación con el resto. Se compone de tres valores: `flex-grow`, `flex-shrink`, y `flex-basis`.
   ```css
   .item {
       flex: 1 1 auto; /* grow, shrink, basis */
   }
   ```

#### Ejercicio Práctico: Creando un Layout con Flexbox
Vamos a construir un layout sencillo que consiste en un header, un footer y tres columnas de contenido.

1. **Modifica tu `index.html`** para incluir un header, un footer y un contenedor principal con tres secciones:
   ```html
   <header>Encabezado</header>
   <div class="container">
       <div class="box">Box 1</div>
       <div class="box">Box 2</div>
       <div class="box">Box 3</div>
   </div>
   <footer>Pie de página</footer>
   ```

2. **Añade estilos CSS** para definir el layout:
   ```css
   header, footer {
       text-align: center;
       padding: 20px;
       background-color: #f3f3f3;
   }

   .container {
       display: flex;
       justify-content: space-around;
       padding: 20px;
   }

   .box {
       flex: 1; /* Cada box tomará el mismo espacio disponible */
       margin: 10px;
       padding: 20px;
       background-color: #e0e0e0;
       text-align: center;
   }
   ```

3. **Observa el Resultado**: Abre tu página en el navegador y mira cómo Flexbox ha organizado el layout de forma limpia y eficiente.

Flexbox es increíblemente útil para estos tipos de layouts y es ideal para interfaces responsivas.

Vamos a profundizar en algunos aspectos más avanzados de Flexbox para que puedas aprovechar al máximo esta poderosa herramienta y crear layouts más dinámicos y funcionales.

### Aspectos Avanzados de Flexbox

1. **Orden y Reordenamiento**: Flexbox permite controlar el orden visual de los elementos dentro del contenedor sin cambiar el HTML. Esto es útil para adaptar el diseño a diferentes pantallas o preferencias de usuario.
   ```css
   .container {
       display: flex;
   }

   .box {
       order: 2; /* Posición visual de este elemento */
   }

   .box:first-child {
       order: 1; /* Hacer que el primer elemento se muestre primero */
   }
   ```

2. **Alineación Individual de Ítems**: Además de alinear todos los ítems en un contenedor con `align-items`, puedes alinear individualmente cada ítem con `align-self`.
   ```css
   .container {
       display: flex;
       align-items: flex-start; /* Alineación inicial para todos los ítems */
   }

   .box {
       align-self: center; /* Alinea este ítem específico al centro verticalmente */
   }
   ```

3. **Crecimiento y Encogimiento Flexibles**: Puedes controlar cómo un elemento crece o se encoge en relación con el resto usando `flex-grow` y `flex-shrink`. Estas propiedades determinan el comportamiento de los ítems cuando el espacio disponible es mayor o menor que el total de los ítems.
   ```css
   .box {
       flex-grow: 1; /* Todos los ítems crecen para llenar el espacio disponible */
       flex-shrink: 0; /* Evita que los ítems se reduzcan */
   }
   ```

4. **Bases Flexibles**: La propiedad `flex-basis` establece el tamaño inicial de un ítem antes de que el espacio restante sea distribuido según `flex-grow` y `flex-shrink`.
   ```css
   .box {
       flex: 1 0 150px; /* grow, shrink, basis */
   }
   ```

5. **Ajuste Automático de Ítems**: Con `flex-wrap`, puedes controlar si los ítems deben envolverse o no al llegar al final de la línea del contenedor.
   ```css
   .container {
       display: flex;
       flex-wrap: wrap; /* Permite que los ítems se envuelvan en múltiples líneas */
   }
   ```

6. **Espaciado entre Ítems**: Utiliza `justify-content` para manejar el espaciado entre los ítems de manera efectiva.
   ```css
   .container {
       display: flex;
       justify-content: space-between; /* Distribuye el espacio disponible uniformemente entre los ítems */
   }
   ```

7. **Multilínea y Alineación de Líneas**: Cuando utilizas `flex-wrap`, puedes alinear las líneas múltiples con `align-content` si hay espacio vertical extra en el contenedor.
   ```css
   .container {
       display: flex;
       flex-wrap: wrap;
       align-content: space-around; /* Espacio distribuido uniformemente entre las líneas */
   }
   ```

Estos aspectos avanzados de Flexbox te permitirán crear interfaces más adaptativas y responsivas, aprovechando mejor el espacio y mejorando la usabilidad en diferentes dispositivos.