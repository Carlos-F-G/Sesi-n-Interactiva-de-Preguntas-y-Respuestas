

## ¿Qué es TypeScript y para qué se utiliza?


TypeScript es un lenguaje de programación desarrollado por Microsoft que extiende JavaScript agregando tipado estático opcional.
Se utiliza para desarrollar aplicaciones web a gran escala, mejorando la calidad del código y reduciendo errores en tiempo de desarrollo.

## ¿Cuáles son las principales diferencias entre TypeScript y JavaScript?
. 1- Tipado estático: TypeScript permite definir tipos para variables, funciones y objetos, mientras que JavaScript es dinámico.
. 2- Interfaces y Clases: TypeScript soporta interfaces y mejoras en la programación orientada a objetos.
. 3- Compatibilidad con ES6/ESNext: TypeScript permite usar características modernas de JavaScript, incluso antes de que sean compatibles en los navegadores.
. 4- Mejoras en depuración: TypeScript detecta errores en tiempo de compilación en lugar de en tiempo de ejecución.
. 5- Compatibilidad con JavaScript: Todo código JavaScript válido es también válido en TypeScript

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









