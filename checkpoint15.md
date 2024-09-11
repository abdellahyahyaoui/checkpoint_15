# 1. ¿Qué es Axios? ¿Qué beneficios tiene?

### a) ¿Qué es Axios?
Axios es una **biblioteca de JavaScript** utilizada para hacer solicitudes HTTP desde el navegador o Node.js. Está basada en **promesas** y se utiliza principalmente para interactuar con APIs, ya sea para obtener, enviar o modificar datos.

### b) ¿Cuándo lo utilizarás?
Utilizarás Axios cuando necesites hacer peticiones HTTP, como **GET**, **POST**, **PUT** o **DELETE**. Es muy común en aplicaciones web que consumen APIs externas o en proyectos donde necesitas enviar datos al servidor o recuperarlos.

### c) ¿Qué beneficios tiene?
- **Basado en Promesas:** Simplifica el manejo de respuestas asíncronas comparado con `XMLHttpRequest`.
- **Interceptors:** Permite configurar interceptores para manejar respuestas o errores globalmente.
- **Soporte para JSON:** Axios convierte las respuestas JSON automáticamente en objetos JavaScript.
- **Manejo de errores:** Proporciona una manera más clara de gestionar errores.
- **Compatibilidad con Node.js:** Funciona tanto en aplicaciones front-end como back-end.
  
### d) Mejores prácticas:
- **Uso de interceptores:** Úsalos para manejar tokens de autenticación de manera automática.
- **Modulariza las solicitudes:** Separa las configuraciones de solicitudes en un archivo propio para mayor legibilidad.
- **Manejo de errores:** Implementa correctamente `try-catch` o métodos `then-catch` para manejar fallos.

### e) Errores comunes:
- **No manejar errores adecuadamente:** No utilizar el bloque `catch` para gestionar respuestas fallidas.
- **Olvidar await o then:** No manejar promesas correctamente al hacer peticiones asíncronas.

### f) Sintaxis:
```javascript
axios.get('https://api.example.com/datos')
  .then(response => {
    console.log(response.data);
  })
  .catch(error => {
    console.error("Error en la solicitud:", error);
  });
  ```
## 2. ¿Por qué es útil React DevTools?

### a) ¿Qué es React DevTools?
React DevTools es una **extensión de navegador** que permite inspeccionar, analizar y depurar aplicaciones React. Muestra una vista jerárquica de los componentes, su estado, y las propiedades (**props**) que pasan entre ellos.

### b) ¿Cuándo lo utilizarás?
Lo usarás cuando necesites **depurar** o **monitorear** una aplicación React, especialmente en la fase de desarrollo. Es útil cuando quieres ver cómo cambia el estado o las props de los componentes.

### c) ¿Qué beneficios tiene?
- **Visualización de componentes:** Muestra una estructura en árbol de todos los componentes React.
- **Inspección de `props` y estado:** Permite ver el valor actual de las `props` y el estado en tiempo real.
- **Optimización de rendimiento:** Ofrece herramientas para detectar componentes que están siendo renderizados innecesariamente.
- **Depuración fácil:** Facilita el rastreo de cambios en el estado o `props` sin necesidad de insertar `console.log` en tu código.

### d) Mejores prácticas:
- **Inspeccionar componentes individuales:** Úsalo para ver cómo fluyen las `props` entre componentes.
- **Monitorear el estado:** Útil para revisar cómo cambia el estado y asegurarse de que el flujo de datos sea correcto.
- **Detectar problemas de rendimiento:** Úsalo para identificar los componentes que se renderizan innecesariamente, lo que puede mejorar el rendimiento.

### e) Errores comunes:
- **No usar la extensión correctamente:** No aprovechar la herramienta para identificar problemas de rendimiento, lo que puede llevar a aplicaciones React ineficientes.
- **No realizar pruebas de estado:** No inspeccionar el estado cuando el comportamiento no es el esperado.

### f) Sintaxis:
No tiene una sintaxis directa de código, ya que es una **herramienta gráfica**. Una vez instalada la extensión, simplemente abres el DevTools en el navegador (F12) y verás una pestaña llamada "React" donde puedes interactuar con la jerarquía de componentes.

---

## 3. ¿Qué es un event listener?

### a) ¿Qué es un event listener?
Un **event listener** es una función que "escucha" un evento en particular, como un **clic**, un **movimiento de ratón**, o una **pulsación de teclado**, y ejecuta una acción en respuesta a ese evento. Es fundamental en la **interactividad** de una página web.

### b) ¿Cuándo lo utilizarás?
Lo usarás cuando quieras que una acción específica ocurra en respuesta a un **evento del usuario**, como cuando hacen clic en un botón o envían un formulario.

### c) ¿Qué beneficios tiene?
- **Interactividad:** Permite crear aplicaciones interactivas donde las acciones del usuario desencadenan comportamientos en la página.
- **Flexibilidad:** Puedes agregar o eliminar event listeners en tiempo real según las necesidades de la aplicación.
- **Modularidad:** Separa la lógica del comportamiento de la interfaz visual.

### d) Mejores prácticas:
- **Remover listeners no utilizados:** Si dejas un listener activo cuando ya no es necesario, puede afectar el rendimiento.
- **Delegación de eventos:** Para optimizar el rendimiento, usa **delegación de eventos** cuando tengas muchos elementos dinámicos. Esto implica asignar el listener a un elemento padre en lugar de a cada elemento individual.
- **Usar funciones separadas:** Evita usar funciones anónimas dentro de un event listener. Usa funciones nombradas para hacer el código más legible y reutilizable.

### e) Errores comunes:
- **No remover event listeners:** No eliminar los listeners cuando ya no son necesarios puede causar fugas de memoria.
- **Listeners duplicados:** Agregar múltiples listeners al mismo evento accidentalmente puede causar que el evento se dispare más veces de lo esperado.
- **Olvidar pasar el parámetro del evento:** No pasar el evento como argumento a la función puede hacer que pierdas información importante, como la posición del clic o el elemento que lo activó.

### f) Sintaxis:
```javascript
document.getElementById('miBoton').addEventListener('click', function() {
  alert('¡Botón clicado!');
});
