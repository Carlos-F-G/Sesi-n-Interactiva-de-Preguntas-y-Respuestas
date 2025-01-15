# Módulo 5: Sesión Interactiva de Preguntas y Respuestas:
## Introducción a TypeScript en ReactJS
<br>
<br>
<br>
<br>

## 1 ¿Qué es TypeScript y para qué se utiliza?


TypeScript es un superset tipado de JavaScript desarrollado por Microsoft. Extiende JavaScript al agregar tipado estático opcional y herramientas avanzadas para el desarrollo. Se compila a JavaScript puro, lo que lo hace compatible con cualquier navegador o entorno donde se ejecute JavaScript.

<br>

### Se utiliza principalmente para:

- Mejorar la detección temprana de errores en el código.
- Facilitar el mantenimiento y escalabilidad en proyectos grandes.
- Proporcionar mejor autocompletado e integración con editores de código como VSCode.
- Implementar conceptos avanzados como interfaces, genéricos y clases en un entorno seguro

  <br>
  <br>
  <br>


## ¿Cuáles son las principales diferencias entre TypeScript y JavaScript?

<br>


| Característica               | JavaScript | TypeScript |
|------------------------------|-----------|-----------|
| 1- **Tipado**                   | Dinámico (las variables pueden cambiar de tipo) | Estático (las variables tienen un tipo fijo si se declara) |
| 2- **Errores en código**        | Se detectan solo en tiempo de ejecución | Se detectan en tiempo de desarrollo |
| 3- **Soporte de Interfaces**    | No tiene interfaces | Soporta interfaces para definir estructuras de datos |
| 4- **Modularidad**              | Usa módulos de ES6 | Usa módulos de ES6 con un tipado más seguro |
| 5- **Compatibilidad**           | Funciona en navegadores sin compilación previa | Necesita compilarse a JavaScript para ejecutarse |
| 6- **Compatibilidad con JavaScript** | Nativo | Totalmente compatible (todo código JS válido es TS válido) |

<br>
<br>
<br>



## ¿Por qué es útil TypeScript en el desarrollo de aplicaciones ReactJS?


### TypeScript mejora la calidad del código en React proporcionando:


### 1- Mejorar la seguridad del código

  Detecta errores antes de que se ejecuten en el navegador.
  Evita pasar props incorrectas en los componentes.
  
### 2- Autocompletado y sugerencias en el editor

Gracias al tipado, los editores como VSCode pueden sugerir métodos y propiedades automáticamente.
  
### 3- Mejor mantenimiento y escalabilidad

Hace que los proyectos sean más fáciles de entender en equipos grandes.
Facilita la refactorización del código sin miedo a romper funcionalidades.

### 4- Facilitar la documentación

Los tipos actúan como documentación para otros desarrolladores.

  <br>
  <br>
  <br>
  

## ¿Qué es el sistema de tipos en TypeScript y cómo ayuda a evitar errores en tiempo de desarrollo?

El sistema de tipos de TypeScript define los tipos de datos que pueden usarse en variables, funciones y objetos. Este sistema ayuda a prevenir errores antes de que el código se ejecute.
<br>

###los beneficios del sistema de tipos pueden:

### -Evita errores de tipo
- Previene operaciones inválidas, como sumar un número con un string.
### -Facilita la lectura del código
- Los desarrolladores pueden entender qué tipo de datos esperan las funciones sin revisar la implementación.
### -Mejor integración con IDEs
- Los editores pueden sugerir funciones y propiedades basadas en los tipos definidos.
### -Ayuda a la refactorización
- Si un tipo cambia, TypeScript alerta de los lugares donde hay conflictos.

  <br>
  <br>
  <br>

## 2- Ejercicio Práctico: Definiendo Tipos e Inferencia

### Definir Tipos en TypeScript

Primero, se define los tipos adecuados para representar la información de un doctor

![image](https://github.com/user-attachments/assets/3d35ddff-c06b-454a-93f2-3ab5a9a3b99c)


Aquí, TypeScript nos asegura que cada doctor tenga un id, un nombre y una especialidad con tipos correctos.

  <br>
  <br>
  <br>

### Creando la Función con Tipado Correcto

Aquí se implementa la función que recibe un array de doctores y devuelve un array con sus nombres:

![image](https://github.com/user-attachments/assets/11c1683f-0438-48cb-bacb-e0becc48d312)


- Parámetro doctores: Doctor[]
Indica que doctores es un array de objetos de tipo Doctor.
- Valor de retorno: string[]
Garantiza que la función devuelve un array de strings (los nombres de los doctores).
- TypeScript infiere automáticamente los tipos dentro de .map()
Como doctor es de tipo Doctor, doctor.nombre es un string.
  
<br>
<br>
<br>

## 3- Definición de Interfaces y Clases en TypeScript


- Se define una interfaz y una clase que implemente esa interfaz para gestionar información de doctores:

  ![image](https://github.com/user-attachments/assets/9a45880c-d615-4a4c-8442-a85b1ee44faf)

  <br>


## 4- TypeScript y ReactJS: Implementación Básica en un Componente

- Componente de React en TypeScript que recibe datos de un doctor como props:

![image](https://github.com/user-attachments/assets/a2578c0a-4402-4168-adb5-e160dd7a87b6)

<br>
<br>
<br>

## 5- Ventajas de TypeScript en el Desarrollo con ReactJS

Las ventajas más importantes de TypeScript en React incluyen:

### -Prevención de errores en tiempo de desarrollo
Al definir tipos para props y estados, se evitan errores comunes antes de ejecutar la aplicación.
### -Autocompletado y ayuda en el editor
Herramientas como VSCode pueden sugerir propiedades y métodos automáticamente.
### -Mejor mantenimiento y escalabilidad
En proyectos grandes, la claridad del código es fundamental.
### -Compatibilidad con JavaScript
Se puede integrar progresivamente TypeScript sin necesidad de reescribir todo el código.









