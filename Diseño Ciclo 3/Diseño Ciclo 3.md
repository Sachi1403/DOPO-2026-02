# Retrospectiva del Proyecto - Desarrollo Orientado por Objetos (DOPO)


## 1. ¿Cuál fue el tiempo total invertido en el laboratorio por cada uno de ustedes? (Horas)
* **David Aldana:** 7 horas.
* **Juan Camilo Alvarez:** 7 horas.
* **Total del equipo:** 14 horas.

## 2. ¿Cuál es el estado actual del laboratorio? ¿Por qué?
Logramos cumplir con los tres requisitos funcionales principales del tercer ciclo: 
1. La extensión de `SlotMachine` para inicializar y gestionar las ruedas y símbolos aleatoriamente (Req. 13).
2. La implementación del algoritmo en `SlotMachineContest` para resolver el problema de la maratón (Req. 14).
3. La simulación visual de las acciones necesarias para ganar (Req. 15).
Además, el diseño en Astah fue refactorizado para cumplir estrictamente con los requisitos (corrigiendo dependencias, constructores y tipos de retorno como matrices `int[][]`).

## 3. Considerando las prácticas XP del laboratorio, ¿cuál fue la más útil? ¿por qué?
La práctica XP más útil en este ciclo fue el **Designing (Diseño iterativo / MDD)** complementado con **Testing**. 
Utilizar la herramienta Astah para modelar primero la dependencia entre `SlotMachineContest` y `SlotMachine` nos permitió entender que la máquina tragamonedas debía actuar únicamente como herramienta de prueba (Testing Tool) y no resolver el problema por sí misma. Planificar los mini-ciclos antes de escribir el código en Java evitó errores de arquitectura.

## 4. ¿Cuál consideran fue el mayor logro? ¿Por qué?
Nuestro mayor logro fue la correcta separación de responsabilidades entre el modelo del dominio (`SlotMachine`, `Wheel`, `Symbol`) y el solucionador (`SlotMachineContest`).

## 5. ¿Cuál consideran que fue el mayor problema técnico? ¿Qué hicieron para resolverlo?
Inicialmente tuvimos problemas con la definición de los constructores (que erróneamente tenían tipo de retorno `void`) y la definición de las matrices bidimensionales. 
*Solución:* Revisamos los fundamentos de diseño, eliminamos los tipos de retorno de los constructores en el Property View de Astah y ajustamos las firmas de los métodos según los requisitos de diseño entregados.

## 6. ¿Qué hicieron bien como equipo? ¿Qué se comprometen a hacer para mejorar los resultados?
* **Lo que hicimos bien:** Tuvimos una excelente comunicación para dividir las tareas; mientras uno se enfocaba en pulir las clases y relaciones en Astah, el otro estructuraba los casos de prueba de unidad (`SlotMachineContestTest`).
* **Compromiso:** Nos comprometemos a ser más rigurosos con la planificación de los *mini-ciclos* desde el día uno de la iteración, para no dejar la documentación y las pruebas de aceptación de JUnit para el último momento.

## 7. ¿Qué referencias usaron? ¿Cuál fue la más útil? Incluyan citas con estándares adecuados.
1. Escuela Colombiana de Ingeniería Julio Garavito. (2026). *DOPO-I03-2026-02: Proyecto Inicial 2026-2 (Ciclo 3)*. Documento interno de la asignatura. (Referencia principal para los requisitos del problema de la maratón).
2. *Desarrollo orientado por objetos (DOPO)*. Texto guía del curso. (Extremadamente útil para la estructuración de colecciones, constructores y metodologías MDD/BDD).
3. Oracle. (n.d.). *Java Platform, Standard Edition 8 API Specification*. Recuperado de https://docs.oracle.com/javase/8/docs/api/ (Útil para el manejo de las estructuras de datos y matrices).
