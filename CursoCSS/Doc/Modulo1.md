Empezaremos con el módulo sobre Selectores Avanzados en CSS.

### Módulo 1: CSS Intermedio - Selectores Avanzados

#### Teoría:
Los selectores avanzados te permiten apuntar a elementos específicos con mayor precisión que los selectores básicos. Incluyen selectores de atributos, pseudo-clases y pseudo-elementos.

#### Ejercicios Intermedios
1. **Selector de atributo**: 
   - Crea tres botones con atributos `data-level="easy"`, `data-level="medium"`, y `data-level="hard"`. Aplica estilos diferentes a cada botón según su nivel de dificultad.

2. **Pseudo-clases**:
   - En una lista de ítems, utiliza `:nth-child` para colorear de manera alternativa los ítems (por ejemplo, los ítems impares de azul y los pares de verde).

3. **Pseudo-elementos**:
   - Añade un párrafo de texto y utiliza `::first-letter` para aumentar el tamaño y cambiar el color de la primera letra.

#### Ejercicios Avanzados
1. **Combinación de selectores**:
   - Utiliza un selector combinado para cambiar el estilo de un elemento que sea tanto `:hover` como `:last-child` de su contenedor.

2. **Estilos condicionales con pseudo-clases**:
   - Aplica estilos diferentes a un campo de entrada (`input`) dependiendo de si el valor es válido o no, usando las pseudo-clases `:valid` y `:invalid`.

3. **Estilización avanzada con pseudo-elementos**:
   - En los títulos de tu página, utiliza `::before` para añadir un ícono decorativo antes del texto del título.

### Configuración para empezar:
Asegúrate de tener tu entorno listo:
- Un editor de texto como Visual Studio Code.
- Un navegador moderno para probar los estilos.

### Comenzando:
1. **Crea una estructura básica en tu HTML** para probar los selectores:
   ```html
   <button data-level="easy">Fácil</button>
   <button data-level="medium">Medio</button>
   <button data-level="hard">Difícil</button>
   <ul>
       <li>Ítem 1</li>
       <li>Ítem 2</li>
       <li>Ítem 3</li>
       <li>Ítem 4</li>
   </ul>
   <p>Este es un párrafo de ejemplo.</p>
   <input type="text" placeholder="Introduce texto...">
   ```

2. **Aplica CSS** para los ejercicios mencionados:
   ```css
   /* Selectores de atributo */
   button[data-level="easy"] { background-color: green; }
   button[data-level="medium"] { background-color: orange; }
   button[data-level="hard"] { background-color: red; }

   /* Pseudo-clases */
   ul li:nth-child(odd) { background-color: blue; }
   ul li:nth-child(even) { background-color: green; }

   /* Pseudo-elementos */
   p::first-letter { font-size: 2em; color: red; }

   /* Estilos avanzados */
   input:valid { border: 2px solid green; }
   input:invalid { border: 2px solid red; }
   ```

3. **Revisa tu trabajo**: Abre tu archivo HTML en un navegador y verifica que los estilos se apliquen correctamente.
