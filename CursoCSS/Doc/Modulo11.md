### Módulo 11: Accesibilidad en CSS

La accesibilidad es un aspecto fundamental del diseño web, asegurando que los sitios sean utilizables para todas las personas, incluidas aquellas con discapacidades. En este módulo, exploraremos cómo el CSS puede ser utilizado para mejorar la accesibilidad.

#### Principios de Accesibilidad en CSS

1. **Contraste de Colores**: Asegurar que los textos tengan suficiente contraste con sus fondos para que sean legibles por usuarios con problemas de visión.
   - **Herramienta**: Utiliza herramientas como WebAIM's Color Contrast Checker para verificar el contraste de tus colores.

2. **Tamaño y Escalabilidad del Texto**: Permitir que el texto sea redimensionado sin perder funcionalidad o legibilidad.
   - **Práctica**: Usa unidades relativas como `em` o `rem` para los tamaños de fuente para soportar la escalabilidad del texto.

3. **Enfoque Visible**: Asegurar que todos los elementos interactivos tengan un indicador de foco claro para ayudar a los usuarios que dependen de teclados para navegar.
   - **CSS**:
     ```css
     a:focus, button:focus {
         outline: 3px solid blue;
     }
     ```

4. **Media Queries para Medios de Asistencia**: Utilizar media queries específicas para adaptar el diseño a las necesidades de los usuarios de lectores de pantalla y otras tecnologías de asistencia.
   - **Ejemplo**:
     ```css
     @media screen and (prefers-reduced-motion: reduce) {
         animation: none;
     }
     ```

#### Ejercicios Prácticos: Mejorando la Accesibilidad con CSS

**Ejercicio 1: Mejora del Contraste**
1. **Objetivo**: Asegurar que todos los elementos de texto en tu sitio cumplan con las directrices de contraste mínimo.
2. **Tareas**:
   - Evalúa el contraste de colores de tu sitio utilizando herramientas de contraste de color.
   - Ajusta los colores en tu CSS para mejorar el contraste donde sea necesario.

**Ejercicio 2: Implementación de Tamaños de Texto Flexibles**
1. **Objetivo**: Hacer que el texto de tu sitio sea fácilmente escalable para soportar las preferencias de los usuarios.
2. **Tareas**:
   - Convierte todos los tamaños de texto fijos a unidades relativas.
   - Prueba la escalabilidad del texto ajustando las configuraciones de tamaño de texto del navegador.

**Ejercicio 3: Refinamiento del Enfoque Visible**
1. **Objetivo**: Mejorar la visibilidad del enfoque para elementos interactivos.
2. **Tareas**:
   - Revisa y modifica los estilos de enfoque para asegurar que sean claramente visibles en todos los elementos interactivos.

### Discusión y Reflexión

Reflexiona sobre cómo la implementación de estas prácticas de accesibilidad afecta la experiencia general del usuario:
- **Impacto en la Usabilidad**: ¿Cómo han mejorado las modificaciones la accesibilidad de tu sitio para usuarios con diversas necesidades?
- **Retos Encarados**: ¿Qué desafíos encontraste al implementar estas características de accesibilidad y cómo los superaste?

Implementar una accesibilidad efectiva es esencial para crear un web inclusiva. ¿Hay algún otro aspecto de la accesibilidad o alguna otra área del desarrollo web que te gustaría explorar más a fondo?