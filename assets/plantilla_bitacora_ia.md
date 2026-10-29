# 📜 Bitácora de Uso de IA en el Colegio Mágico (Entrega en PR)

> **Instrucciones:** Copia todo este contenido y pégalo en la descripción de tu Pull Request (PR).  
> **Recordatorio:** Este informe vale el **20% de tu calificación final** y debe ser redactado con tus propias palabras (sin utilizar IA para generar el texto del reporte).

---

## 🧙‍♂️ Datos del Aprendiz
* **Nombre del Estudiante:** [Santiago Fonseca Ramirez]
* **Usuario de GitHub:** [[Fonseca28](https://github.com/Fonseca28)]
* **Herramientas de IA utilizadas:** [Claude,OpenCode]

---

## 🔍 Bitácora del Reto 5: El Transmutador de Estados (Filtros y Estabilidad)

### 1. Prompt Principal Formulado
> *Pega aquí el prompt exacto que le diste a la IA:*
```text
[# RETO 5: MOTOR DE BÚSQUEDA, FILTROS COMBINADOS Y ESTABILIDAD

## Objetivo
Completar el Reto 5 en `caldero.component.ts`: implementar
`getPocionesFiltradas()` y `calcularEstabilidadCaldero()` para que pasen los
tests 5.1 a 5.9. Haz el cambio mínimo necesario.

## Dónde está lo que debes hacer
Busca en `caldero.component.ts` los comentarios `TODO: Reto 5` (motor de
búsqueda y filtros combinados, y estabilidad del caldero). Sigue exactamente lo
que dicen. Revisa también en el spec los tests 5.1 a 5.9 para ver qué exigen.

## Requisitos clave
- `getPocionesFiltradas()` devuelve una copia filtrada y ordenada de
  `this.pociones`. Los filtros son: texto (nombre o descripción, sin distinguir
  mayúsculas, vacío = no filtra), tipo de magia (distinto de 'TODAS') y solo
  peligrosas (`nivelPeligro > 7`). El orden por `nivelPeligro` se aplica después
  de los filtros.
- `calcularEstabilidadCaldero()` devuelve 'CRÍTICO' con 2 o más pociones de
  peligro >= 8, 'INESTABLE' con al menos 1 de peligro >= 5 y 'SEGURO' en los
  demás casos.

## Restricciones
- No modificar `this.pociones` ni ordenarlo directamente (usar una copia).
- No modificar archivos `*.spec.ts` ni debilitar pruebas.
- Mantener nombres de propiedades, métodos y tipos actuales.
- No tocar los Retos 3, 4 y 6 ni lo que ya funciona.
- No agregar dependencias ni refactorizar código ajeno al reto.

## Flujo de trabajo
1. Leer el archivo y el spec antes de editar.
2. Explicarme en español, con ejemplos sencillos, qué hace el código actual.
3. Implementar la solución.
4. Ejecutar `npm run test:ci` y mostrarme el resultado real (sin afirmar que
   pasa si no se ejecutó).
5. Revisar el diff: solo debe cambiar el archivo del Reto 5.
6. [GIT: commit/push según lo que yo decida]

## Explicación
Explícame qué hace cada filtro, por qué se usa una copia del arreglo y cómo
funciona el ordenamiento. No avances al Reto 6 hasta terminar este.

## Reporte final
Archivos modificados, cambios, tests ejecutados con resultado real y pendientes.]
```

### 2. ¿Qué respuesta te entregó la IA?
*Describe brevemente la solución que te propuso:*
- [Implementé dos métodos en caldero.component.ts:

getPocionesFiltradas()
Crea una copia de this.pociones con [...this.pociones] para no mutar el arreglo original.
Aplica tres filtros combinados con &&:
Texto: convierte filtroTexto a minúsculas y busca coincidencia en nombre o descripcion; si está vacío, no filtra.
Tipo de magia: si filtroTipoMagia !== 'TODAS', exige que coincida con tipoMagia.
Peligrosas: si filtroSoloPeligrosas es true, exige nivelPeligro > 7.
Ordena el resultado por nivelPeligro después de filtrar: ascendente (a - b) si ordenAscendente es true, descendente (b - a) si es false.
calcularEstabilidadCaldero()
Cuenta las pociones con nivelPeligro >= 8: si hay 2 o más, devuelve 'CRÍTICO'.
Si no, comprueba si existe al menos una con nivelPeligro >= 5: devuelve 'INESTABLE'.
En caso contrario, devuelve 'SEGURO'.]

### 3. Ajustes y Correcciones Manuales
*¿La solución funcionó a la primera? ¿Qué tuviste que corregir o adaptar para que pasaran las pruebas del Tribunal?*
- [funciono a la primera]

---

## ⏳ Bitácora del Reto 6: El Giratiempo (Undo / Redo Inmutable)

### 1. Prompt Principal Formulado
> *Pega aquí el prompt exacto que le diste a la IA:*
```text
[Escribe aquí tu prompt]
```

### 2. ¿Cómo abordó la IA la inmutabilidad de los objetos?
*Explica qué método te sugirió para clonar el arreglo de pociones sin mutar las referencias originales (ej. map con spread operator, structuredClone, etc.):*
- [Tu explicación]

### 3. Depuración de Errores con la IA
*Si una prueba de Jasmine falló, ¿cómo usaste la IA para encontrar el bug?*
- [Tu experiencia de depuración]

---

## 🎨 Resumen del Reto Creativo (Reto 7 - 30%)
* **Nombre de tu Artefacto Mágico:** [Ej: El Mapa del Merodeador, Tienda de Varitas Ollivander, etc.]
* **¿Qué hace tu artefacto y cómo interactúa el usuario?**
  - [Descripción de funcionalidades]
* **¿Qué hooks de ciclo de vida implementaste?**
  - [Ej: ngOnInit para cargar datos, ngOnDestroy para limpiar timers]
* **¿Qué directivas y enlaces utilizaste?**
  - [Ej: @if para estados de victoria, @for para hechizos, [(ngModel)] para renombrar]

---

## 💡 Reflexión Crítica del Aprendiz
*¿En qué momentos sentiste que la IA te ahorró tiempo y en qué momentos una mala respuesta te retrasó?*
- [Tu reflexión honesta con tus propias palabras]
