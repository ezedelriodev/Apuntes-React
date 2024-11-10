<div align='center'>
  <img height="60" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/539px-React-icon.svg.png">
  <h1>Resumen y detalles de documentación React</h1>

  <sup>Deja tu :star: si te gusta el proyecto.</sup>

</div>

## Índice

- [Índice](#índice)
    - [**¿Qué es React?**](#qué-es-react)



#### **¿Qué es React?**
**React** es una biblioteca de JavaScript desarrollada por Facebook para construir interfaces de usuario, principalmente en aplicaciones web de una sola página (SPA, Single Page Applications). Está enfocada en crear componentes reutilizables que se pueden combinar para construir interfaces complejas de forma eficiente. React se destaca por su rapidez, modularidad y un enfoque declarativo que facilita la creación y mantenimiento de interfaces de usuario dinámicas y reactivas.

Aquí tienes un resumen de los conceptos clave en React:

1. **Componentes**
   
- React organiza las aplicaciones en componentes, que son bloques de construcción independientes y reutilizables.
  
- Cada componente representa una parte de la interfaz de usuario (como un botón, un formulario o un encabezado) y puede tener su propia lógica y estilo.
  
- Los componentes pueden anidarse y combinarse para construir interfaces más complejas.

Ejemplo básico de un componente en React:


```js
function Bienvenida(props) { //un componente es una función 👀
  return <h1>Hola, {props.nombre}</h1>;
}
```  

1. **JSX (JavaScript XML)**
   
- React utiliza JSX, una extensión de JavaScript que permite escribir HTML directamente en el código JavaScript.
  
- Aunque JSX se parece a HTML, permite integrar lógica de JavaScript fácilmente, lo que hace que la interfaz sea más declarativa y expresiva.
```js
const elemento = <h1>¡Hola, mundo!</h1>;
```

3. **Virtual DOM**  
- React utiliza un DOM Virtual (Virtual DOM) para actualizar la interfaz de usuario de forma eficiente.
  
- En lugar de modificar el DOM real (que es lento), React crea una copia virtual del DOM en memoria. Cuando el estado de la aplicación cambia, React compara el Virtual DOM con el DOM real y actualiza solo las partes que cambiaron.
  
- Este proceso se llama reconciliación y permite que React sea rápido incluso en aplicaciones complejas.  
  

4. **Estado y Propiedades (Props)**  
- **Props**: Son los datos que los componentes reciben de otros componentes. Los props son inmutables, lo que significa que no se pueden modificar dentro del componente que los recibe.
  
- **Estado (State)**: Es un objeto que guarda datos internos del componente. A diferencia de los props, el estado es mutable y controlado dentro del componente. Cuando el estado cambia, el componente se vuelve a renderizar para reflejar los cambios.

Ejemplo de uso de estado en un componente funcional usando **useState**:

```js
import React, { useState } from 'react';

function Contador() {
  const [contador, setContador] = useState(0);

  return (
    <div>
      <p>Contador: {contador}</p>
      <button onClick={() => setContador(contador + 1)}>
        Incrementar
      </button>
    </div>
  );
}
```

5. **Hooks**  
- Los Hooks son funciones que permiten usar el estado y otras características de React en componentes funcionales).

- El hook más común es **useState** para manejar el estado, pero también hay otros como **useEffect** (para efectos secundarios) y **useContext** (para el contexto global de la aplicación).


6. **Unidirectional Data Flow (Flujo de datos unidireccional)**  
- En React, los datos fluyen en una única dirección, de los componentes padres a los componentes hijos. Esto hace que sea más fácil controlar el estado de la aplicación y depurar el flujo de datos.
  
- Si un componente necesita modificar algún dato, lo hace a través de su propio estado o utilizando funciones pasadas como props desde el componente padre.

**[⬆ Volver a índice](#índice)**

---

**INCORPORAR: PIENSA EN REACT**