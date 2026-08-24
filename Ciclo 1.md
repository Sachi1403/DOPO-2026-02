# SlotMachine - Ciclo 1

Simulador de máquina tragamonedas en Java/BlueJ basado en el problema *Slot Machine* (2025).

## Tecnologías y Requisitos
* **Lenguaje:** Java 8+ / BlueJ
* **Modelado:** Astah Professional (Diagramas UML)
* **Gráficos:** Paquete `shapes` extendido (`Canvas`, `Rectangle`)

---

## Decisiones de Diseño
* **Lista única:** `symbols` vive en `SlotMachine` y se comparte con `Wheel` (`{readOnly for Wheel}`).
* **Posiciones (base 1):** Ajustadas automáticamente con `clamp()`.
* **Manejo de errores:** Atributo `lastOk` guarda el estado. `report()` lanza `JOptionPane` solo si `isVisible == true`.
* **Ajuste de índices:** Métodos `adjustAfterDelete` y `adjustAfterInsert` en `Wheel` para mantener el color correcto tras cambios.

---

## Retrospectiva

### 1. Mini-ciclos definidos
* **MC1 (Estructura Base):** `SlotMachine()`, `makeVisible()`, `makeInvisible()`, `ok()`, `exit()`.
* **MC2 (Ruedas):** `addWheel()`, `delWheel()`, `relocateWheels()`.
* **MC3 (Símbolos):** Extensión de `Canvas` (colores CSS), `addSymbol()`, `delSymbol()`, `placeSymbol()`.
* **MC4 (Juego y Consultas):** `spin()`, `symbols()`, `configuration()`, `distinctSymbols()`, `isJackpot()`, `updateLook()`.

### 2. Estado actual
**100% completado** (MC1 a MC4).

### 3. Tiempo invertido
* **David Santiago:** 8 Horas
* **Juan Camilo:** 8 Horas
* **Total:** 16 Horas/Hombre

### 4. Mayor logro
Completar la entrega a tiempo mientras aprendíamos en el proceso

### 5. Mayor problema técnico y solución
Lograr que el diseño se viera bien, aparte de aprender a usar efectivamente Astah y BlueJ.

### 6. Trabajo en equipo
* **Bien:** Buena comunicación, división clara por mini-ciclos y compromiso de ambas partes.
* **A mejorar:** Integrar pruebas automatizadas (JUnit) desde el inicio. Mejorar habilidades de codificación (ganar experiencia)

### 7. Práctica XP más útil
**Diseño Sencillo (Simple Design)**, al mantener métodos cortos (menos de una pantalla) y modulares.

### 8. Referencias
1. Escuela Colombiana de Ingeniería. (2026). *DOPO: Proyecto Inicial Ciclo 1*.
2. Barker, J. (2005). *Beginning Java Objects*. Apress.
3. Oracle. (2023). *Java API Documentation*.
