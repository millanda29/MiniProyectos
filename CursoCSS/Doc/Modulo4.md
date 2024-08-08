### Módulo 4: Transiciones y Animaciones en CSS

Las transiciones y animaciones son herramientas poderosas en CSS que permiten agregar movimiento y respuestas visuales dinámicas a las interacciones de los usuarios en la web. Vamos a explorar cómo utilizarlas para mejorar la experiencia del usuario.

#### Conceptos Fundamentales de Transiciones en CSS

1. **Transiciones**: Permiten cambiar propiedades CSS de manera suave a lo largo del tiempo. Se usan principalmente para efectos al pasar el ratón o al cambiar el estado de un elemento.
   ```css
   .transition-box {
       width: 100px;
       height: 100px;
       background: blue;
       transition: background 0.5s ease-in-out;
   }

   .transition-box:hover {
       background: red;
   }
   ```

   En este ejemplo, el color de fondo del `.transition-box` cambiará de azul a rojo en 0.5 segundos de manera suave cuando el usuario pase el ratón por encima.

2. **Propiedades Animables**: No todas las propiedades CSS son animables. Propiedades comunes que sí lo son incluyen `opacity`, `color`, `background-color`, y la mayoría de las propiedades de transformación como `translate`, `scale`, y `rotate`.

#### Conceptos Fundamentales de Animaciones en CSS

1. **Keyframes**: Para crear animaciones más complejas que las transiciones, CSS permite definir `@keyframes`, que especifican los estilos en varios puntos durante la animación.
   ```css
   @keyframes example {
       0% { background-color: red; }
       50% { background-color: yellow; }
       100% { background-color: green; }
   }

   .animated-box {
       width: 100px;
       height: 100px;
       background: red;
       animation: example 2s infinite;
   }
   ```

   Aquí, `.animated-box` cambiará su color de fondo de rojo a amarillo, luego a verde, y repetirá el ciclo indefinidamente cada 2 segundos.

2. **Control de Animaciones**: Puedes controlar cómo y cuándo una animación debe correr usando propiedades como `animation-delay`, `animation-timing-function`, `animation-iteration-count`, y `animation-direction`.

#### Ejercicio Práctico: Aplicando Transiciones y Animaciones

1. **Añade HTML para los ejemplos de transiciones y animaciones**:
   ```html
   <div class="transition-box">Pasa el ratón por encima</div>
   <div class="animated-box">Observa la animación</div>
   ```

2. **Incorpora el CSS que hemos definido**:
   ```css
   /* Transiciones */
   .transition-box {
       width: 100px;
       height: 100px;
       background: blue;
       transition: background 0.5s ease-in-out;
       margin: 10px;
   }

   .transition-box:hover {
       background: red;
   }

   /* Animaciones */
   @keyframes example {
       0% { background-color: red; }
       50% { background-color: yellow; }
       100% { background-color: green; }
   }

   .animated-box {
       width: 100px;
       height: 100px;
       background: red;
       animation: example 2s infinite;
       margin: 10px;
   }
   ```

3. **Prueba y Observa**: Abre tu página en el navegador y mira las transiciones y animaciones en acción. Experimenta modificando los tiempos y los estilos para ver cómo cambia el comportamiento.

Las transiciones y animaciones pueden mejorar significativamente la interactividad y el atractivo visual de una página web.

Vamos a profundizar en algunos aspectos más avanzados de las transiciones y animaciones en CSS, explorando técnicas que pueden hacer que tus interfaces sean aún más dinámicas e interactivas.

### Aspectos Avanzados de Transiciones en CSS

1. **Transiciones con Múltiples Propiedades**: Puedes animar varias propiedades simultáneamente en un solo elemento, y cada propiedad puede tener su propio tiempo y función de easing.
   ```css
   .multi-transition-box {
       width: 100px;
       height: 100px;
       background: blue;
       opacity: 0.5;
       transition: background 0.5s ease, opacity 2s linear;
   }

   .multi-transition-box:hover {
       background: green;
       opacity: 1;
   }
   ```
   Aquí, tanto el color de fondo como la opacidad se animan al pasar el ratón, pero cada una con diferentes duraciones y funciones de easing.

2. **Uso de `transition-delay`**: Puedes especificar un retraso antes de que comience una transición, lo cual puede ser útil para crear efectos en cadena o esperar otros eventos en la página.
   ```css
   .delayed-transition-box {
       width: 100px;
       height: 100px;
       background: orange;
       transition: background 0.5s ease 1s; /* 1s delay */
   }

   .delayed-transition-box:hover {
       background: purple;
   }
   ```

### Aspectos Avanzados de Animaciones en CSS

1. **Manipulación de `animation-fill-mode`**: Esta propiedad define cómo un elemento estilizado con una animación debe aplicarse antes y después de que se ejecute.
   - `forwards`: El elemento mantendrá el estilo establecido por el último keyframe (útil para animaciones que no deben revertir a su estado inicial).
   - `backwards`: El elemento tomará el estilo del primer keyframe durante el tiempo de retraso definido por `animation-delay`.
   - `both`: Aplica las reglas de `forwards` y `backwards`.
   ```css
   @keyframes expand {
       0% { width: 100px; }
       100% { width: 200px; }
   }

   .expanding-box {
       width: 100px;
       height: 100px;
       background: teal;
       animation: expand 3s forwards;
   }
   ```

2. **`animation-timing-function` en Keyframes**: Puedes especificar una función de tiempo diferente para cada keyframe, permitiendo transiciones más complejas y naturales entre estados.
   ```css
   @keyframes color-pulse {
       0%, 100% { background: red; easing: ease-in; }
       50% { background: yellow; easing: ease-out; }
   }

   .pulsing-box {
       width: 100px;
       height: 100px;
       animation: color-pulse 2s infinite;
   }
   ```

3. **Control de la Dirección de la Animación**: La propiedad `animation-direction` permite definir si la animación debe correr hacia adelante, hacia atrás, alternar entre ambos, etc.
   - `normal`: La animación se reproduce tal como está definida.
   - `reverse`: La animación se reproduce en sentido inverso.
   - `alternate`: La animación se reproduce hacia adelante y luego hacia atrás, alternando con cada iteración.
   ```css
   .alternating-box {
       animation: color-pulse 2s infinite alternate;
   }
   ```

Estas técnicas avanzadas te permiten crear efectos visuales más ricos y controlados, mejorando la experiencia del usuario al interactuar con tu sitio web. ¿Hay alguna técnica específica o algún efecto visual que te gustaría ver implementado en un ejemplo práctico?