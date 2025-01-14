

## ¿Qué es TypeScript y para qué se utiliza?


TypeScript es un superset tipado de JavaScript desarrollado por Microsoft. Extiende JavaScript al agregar tipado estático opcional y herramientas avanzadas para el desarrollo. Se compila a JavaScript puro, lo que lo hace compatible con cualquier navegador o entorno donde se ejecute JavaScript.

Se utiliza principalmente para:

- Mejorar la detección temprana de errores en el código.
- Facilitar el mantenimiento y escalabilidad en proyectos grandes.
- Proporcionar mejor autocompletado e integración con editores de código como VSCode.
- Implementar conceptos avanzados como interfaces, genéricos y clases en un entorno seguro.


## ¿Cuáles son las principales diferencias entre TypeScript y JavaScript?

| Característica               | JavaScript | TypeScript |
|------------------------------|-----------|-----------|
| **Tipado**                   | Dinámico (las variables pueden cambiar de tipo) | Estático (las variables tienen un tipo fijo si se declara) |
| **Errores en código**        | Se detectan solo en tiempo de ejecución | Se detectan en tiempo de desarrollo |
| **Soporte de Interfaces**    | No tiene interfaces | Soporta interfaces para definir estructuras de datos |
| **Modularidad**              | Usa módulos de ES6 | Usa módulos de ES6 con un tipado más seguro |
| **Compatibilidad**           | Funciona en navegadores sin compilación previa | Necesita compilarse a JavaScript para ejecutarse |
| **Compatibilidad con JavaScript** | Nativo | Totalmente compatible (todo código JS válido es TS válido) |


## ¿Cuáles son las principales diferencias entre TypeScript y JavaScript?

¿Por qué es útil TypeScript en el desarrollo de aplicaciones ReactJS?

TypeScript mejora la calidad del código en React proporcionando:

- Autocompletado y ayuda en editores como VSCode.
- Reducción de errores por tipado incorrecto en componentes y props.
- Mejor mantenimiento del código en proyectos grandes.
- Mayor claridad y documentación automática del código.

## ¿Qué es el sistema de tipos en TypeScript y cómo ayuda a evitar errores en tiempo de desarrollo?

El sistema de tipos en TypeScript define el tipo de valores que pueden ser utilizados en variables, funciones y objetos.
Esto ayuda a evitar errores al detectar inconsistencias antes de ejecutar el código, lo que mejora la seguridad y robustez del programa.


### 2. Ejercicio Práctico: Definiendo Tipos e Inferencia

Aquí tienes una función en ReactJS con TypeScript para definir los tipos de un array de doctores:


// Definiendo tipos en TypeScript
type Doctor = {
  id: number;
  nombre: string;
  especialidad: string;
};

// Función que recibe un array de doctores y devuelve sus nombres
const obtenerNombresDoctores = (doctores: Doctor[]): string[] => {
  return doctores.map(doctor => doctor.nombre);
};

// Uso de la función
const doctoresEjemplo: Doctor[] = [
  { id: 1, nombre: "Dr. Pérez", especialidad: "Cardiología" },
  { id: 2, nombre: "Dra. López", especialidad: "Pediatría" }
];

console.log(obtenerNombresDoctores(doctoresEjemplo));


# Aquí TypeScript infiere automáticamente los tipos en el método map().


### 3. Definición de Interfaces y Clases en TypeScript

Definimos una interfaz y una clase que implemente esa interfaz para gestionar información de doctores:


// Definiendo una interfaz para los datos de un doctor
interface IDoctor {
  id: number;
  nombre: string;
  especialidad: string;
  actualizarEspecialidad(nuevaEspecialidad: string): void;
}

// Implementando la interfaz en una clase
class Doctor implements IDoctor {
  constructor(
    public id: number,
    public nombre: string,
    public especialidad: string
  ) {}

  actualizarEspecialidad(nuevaEspecialidad: string): void {
    this.especialidad = nuevaEspecialidad;
  }
}

// Creando una instancia y actualizando especialidad
const doctor1 = new Doctor(1, "Dr. Pérez", "Cardiología");
doctor1.actualizarEspecialidad("Neurología");
console.log(doctor1);

### 4. TypeScript y ReactJS: Implementación Básica en un Componente

 componente de React en TypeScript que recibe datos de un doctor como props:

 import React from "react";

// Definiendo la interfaz para las props del componente
interface DoctorProps {
  id: number;
  nombre: string;
  especialidad: string;
}

// Componente funcional en React con TypeScript
const DoctorCard: React.FC<DoctorProps> = ({ id, nombre, especialidad }) => {
  return (
    <div>
      <h2>{nombre}</h2>
      <p>Especialidad: {especialidad}</p>
      <small>ID: {id}</small>
    </div>
  );
};

// Uso del componente con datos de prueba
const App: React.FC = () => {
  return (
    <div>
      <DoctorCard id={1} nombre="Dr. Pérez" especialidad="Cardiología" />
    </div>
  );
};

export default App;


### 5. Ventajas de TypeScript en el Desarrollo con ReactJS

Las ventajas más importantes de TypeScript en React incluyen:

1- Prevención de errores en tiempo de desarrollo → Al definir tipos para props y estados, se evitan errores comunes antes de ejecutar la aplicación.
2- Autocompletado y ayuda en el editor → Herramientas como VSCode pueden sugerir propiedades y métodos automáticamente.
3- Mejor mantenimiento y escalabilidad → En proyectos grandes, la claridad del código es fundamental.
4- Compatibilidad con JavaScript → Se puede integrar progresivamente TypeScript sin necesidad de reescribir todo el código.


# Ejemplo de ventaja:

Si se usa JavaScript puro y pasamos id como string en lugar de number, la aplicación podría fallar en tiempo de ejecución.
En TypeScript, se detectaría inmediatamente como un error en el editor.









