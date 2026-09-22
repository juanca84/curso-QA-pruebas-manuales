# GUÍA DEL DOCENTE — CLASE 4

## Gestión de Defectos, Bug Tracking y Pruebas de Regresión

**Curso:** Estrategia de Aseguramiento de la Calidad y Pruebas Manuales
**Duración:** 2 horas aproximadamente
**Modalidad:** Teórico-práctica
**Herramienta:** Jira

---

# 1. Propósito de la clase

La finalidad de esta clase es que el estudiante comprenda que el trabajo de QA no termina cuando encuentra un defecto.

El estudiante debe aprender a:

1. Identificar correctamente un defecto.
2. Documentarlo de manera profesional.
3. Comunicarlo al equipo.
4. Dar seguimiento a su ciclo de vida.
5. Verificar que la corrección realmente funcione.
6. Comprobar que una corrección no haya afectado otras funcionalidades.

La idea central de la clase es:

> **Encontrar un bug es solamente el comienzo del proceso.**

Un QA profesional debe proporcionar información suficientemente clara para que el equipo pueda comprender, reproducir, corregir y verificar el problema.

---

# 2. Objetivos de aprendizaje

Al finalizar la clase, el estudiante debe poder:

* Diferenciar **error, defecto y fallo**.
* Explicar qué es un **Bug Report**.
* Identificar las partes principales de un reporte.
* Crear reportes claros y reproducibles.
* Diferenciar **Severity** y **Priority**.
* Explicar el ciclo de vida de un defecto.
* Comprender qué es **Bug Tracking**.
* Registrar un defecto utilizando Jira.
* Explicar qué es un **Retest**.
* Explicar qué es **Regression Testing**.
* Diferenciar Retest de Regression Testing.

---

# 3. Enfoque metodológico

Se recomienda utilizar la siguiente distribución:

### 70 % — Explicación y conceptos

El docente explica:

* Defectos.
* Bug Reports.
* Severidad.
* Prioridad.
* Estados.
* Retest.
* Regression Testing.

### 20 % — Demostración

El docente demuestra cómo registrar un Bug en Jira.

### 10 % — Práctica

Los estudiantes crean un Bug Report y lo registran en Jira.

La herramienta no debe convertirse en el centro de la clase.

El objetivo no es:

> "Aprender a utilizar Jira."

El objetivo es:

> **Aprender a gestionar y comunicar defectos utilizando Jira como herramienta.**

---

# DIAPOSITIVA 1 — Título

## Gestión de Defectos y Pruebas de Regresión

### De encontrar un bug a verificar su solución

## Explicación del docente

Comenzar preguntando:

> "Cuando un tester encuentra un error en un sistema, ¿qué debería hacer?"

Escuchar algunas respuestas.

Probablemente los estudiantes respondan:

* Informarlo.
* Avisar al desarrollador.
* Crear un ticket.
* Corregirlo.

A partir de las respuestas explicar:

Encontrar un problema es solamente una parte del trabajo de QA.

Un proceso profesional requiere:

**Detectar → Documentar → Comunicar → Dar seguimiento → Verificar**

Explicar que durante esta clase se aprenderá precisamente ese proceso.

---

# DIAPOSITIVA 2 — Objetivos de aprendizaje

Leer los objetivos rápidamente y explicar que al finalizar la clase el estudiante debe poder realizar un proceso completo.

No es necesario explicar cada punto en profundidad todavía.

### Enfatizar

Hay tres habilidades especialmente importantes:

**1. Documentar**

Saber explicar un defecto.

**2. Gestionar**

Saber darle seguimiento.

**3. Verificar**

Saber comprobar que fue solucionado.

Decir:

> "Un QA que solamente encuentra bugs, pero no sabe documentarlos ni verificar las soluciones, está realizando solamente una parte del proceso de calidad."

---

# DIAPOSITIVA 3 — ¿Qué ocurre cuando encontramos un problema?

## Explicación

Esta diapositiva introduce la idea principal de la clase.

Explicar:

Cuando encontramos un comportamiento incorrecto, no debemos simplemente enviar un mensaje como:

> "Hay un error."

Ese mensaje no proporciona suficiente información.

El equipo necesita saber:

* ¿Dónde ocurrió?
* ¿Qué estaba haciendo el usuario?
* ¿Cómo reproducirlo?
* ¿Qué debería haber ocurrido?
* ¿Qué ocurrió realmente?
* ¿Qué impacto tiene?
* ¿En qué ambiente ocurrió?

### Ejemplo

Un mensaje como:

> "El carrito está mal."

No es suficiente.

Un reporte mejor sería:

> "Al cambiar la cantidad de un producto de 1 a 3 unidades y seleccionar 'Actualizar carrito', la cantidad cambia, pero el precio total permanece calculado para una sola unidad."

Ahora el desarrollador tiene mucha más información.

### Mensaje clave

> **La calidad de un Bug Report influye directamente en la capacidad del equipo para solucionar el problema.**

---

# DIAPOSITIVA 4 — Error, defecto y fallo

Este es uno de los conceptos fundamentales de la clase.

Explicar cuidadosamente la diferencia.

## Error — Error / Mistake

Es una acción, decisión o interpretación incorrecta realizada por una persona.

Puede ocurrir por:

* Falta de comprensión del requisito.
* Falta de comunicación.
* Error de programación.
* Falta de conocimiento.
* Descuidos.

## Defecto — Defect / Bug

Es una condición o problema presente en el software que puede provocar un comportamiento incorrecto.

El defecto puede estar:

* En el código.
* En una configuración.
* En una base de datos.
* En una regla de negocio.
* En una integración.

## Fallo — Failure

Es cuando el comportamiento incorrecto se manifiesta durante la ejecución del sistema.

### Explicación sencilla

Utilizar:

> **Error humano → Defecto → Fallo observable**

### Importante

No decir que todos los errores producen necesariamente un fallo visible.

Un defecto puede existir y no manifestarse hasta que se ejecuta una condición específica.

---

# DIAPOSITIVA 5 — Ejemplo

## Explicación del docente

Utilizar el ejemplo mostrado en la diapositiva.

### Requisito

> Un usuario menor de 18 años no puede registrarse.

Primero preguntar:

> "¿Qué debería hacer el sistema?"

Esperamos que los estudiantes respondan:

> Rechazar el registro.

Después explicar:

### Error

El desarrollador interpreta incorrectamente la regla.

### Defecto

La validación de edad fue implementada incorrectamente.

### Fallo

Durante la ejecución, el sistema permite registrar al usuario de 15 años.

### Pregunta

> "¿Qué observa directamente el tester?"

La respuesta correcta es:

> **El fallo.**

El tester observa el comportamiento del sistema.

Posteriormente, mediante el análisis, documenta el defecto.

### Punto importante

No confundir:

> "QA encuentra errores."

con:

> "QA observa fallos y reporta defectos."

Esta diferencia conceptual ayuda a los estudiantes a utilizar correctamente la terminología profesional.

---

# DIAPOSITIVA 6 — ¿Qué es un Bug Report?

## Explicación

Definir:

> Un Bug Report es un registro estructurado que documenta un comportamiento incorrecto encontrado en el software.

Explicar que su finalidad no es simplemente informar que existe un problema.

Debe ayudar a otra persona a:

1. Entenderlo.
2. Reproducirlo.
3. Analizarlo.
4. Corregirlo.
5. Verificar la solución.

### Ejemplo

Comparar:

❌

> "No funciona el carrito."

Con:

✅

> "Al modificar la cantidad de un producto y actualizar el carrito, la cantidad cambia pero el precio total no se recalcula."

Preguntar:

> "¿Cuál de los dos reportes sería más útil para desarrollo?"

La respuesta es evidente.

### Concepto clave

**Claro + Objetivo + Reproducible**

---

# DIAPOSITIVA 7 — Partes de un Bug Report

Explicar que no todos los proyectos utilizan exactamente los mismos campos.

El formato depende de:

* Organización.
* Metodología.
* Herramienta.
* Tipo de proyecto.
* Proceso de QA.

Pero existen elementos comunes.

## Explicar los campos principales

### ID

Identificador único del defecto.

### Título

Resumen breve del problema.

### Descripción

Explicación general.

### Precondiciones

Condiciones necesarias antes de reproducirlo.

### Pasos

Acciones realizadas para reproducirlo.

### Datos

Información utilizada durante la prueba.

### Expected Result

Lo que debería suceder.

### Actual Result

Lo que realmente ocurrió.

### Evidence

Información visual o técnica que ayuda a demostrar el problema.

### Environment

Dónde ocurrió.

### Severity

Impacto.

### Priority

Urgencia.

### Status

Estado actual del defecto.

---

# DIAPOSITIVA 8 — El título del bug

## Explicación

El título es una de las partes más importantes porque normalmente será lo primero que verá el equipo.

Debe permitir comprender rápidamente:

**Qué ocurre + dónde ocurre**

### Ejemplo incorrecto

> "No funciona."

Preguntar:

> "¿Qué no funciona?"

No sabemos.

### Otro ejemplo

> "Error en usuarios."

Sigue siendo demasiado general.

### Mejor

> "El sistema permite registrar usuarios menores de 18 años."

Ahora sabemos:

* Qué ocurre.
* En qué funcionalidad.
* Cuál es el comportamiento problemático.

### Enseñar una fórmula práctica

**[Componente/funcionalidad] + [comportamiento incorrecto]**

Ejemplo:

> "Carrito no actualiza el precio total al modificar la cantidad."

---

# DIAPOSITIVA 9 — Pasos para reproducir

## Explicación

Esta sección es fundamental.

Un desarrollador debería poder tomar el Bug Report y reproducir el problema sin tener que preguntarle constantemente al tester.

Explicar:

Los pasos deben ser:

* Claros.
* Ordenados.
* Específicos.
* Repetibles.

### Evitar

> "Entrar al sistema y probar."

Eso no es reproducible.

### Mejor

1. Ingresar al sistema.
2. Abrir el módulo Usuarios.
3. Seleccionar Nuevo usuario.
4. Introducir los datos.
5. Seleccionar Registrar.

### Pregunta

> "¿Qué pasaría si omitimos un paso importante?"

El desarrollador podría no conseguir reproducir el defecto.

---

# DIAPOSITIVA 10 — Resultado esperado vs. actual

## Explicación

Este concepto debe quedar muy claro.

### Expected Result

Representa el comportamiento esperado.

¿De dónde obtenemos esa expectativa?

Puede venir de:

* Requisito.
* Historia de usuario.
* Criterio de aceptación.
* Regla de negocio.
* Especificación.

### Actual Result

Describe exactamente qué ocurrió.

### Ejemplo

Expected:

> El sistema debe rechazar el registro.

Actual:

> El sistema permite completar el registro.

### Importante

El tester debe evitar escribir opiniones.

❌

> "El sistema está muy mal."

✅

> "El sistema permite completar el registro."

El segundo es objetivo y verificable.

---

# DIAPOSITIVA 11 — Evidencia

## Explicación

Explicar que la evidencia ayuda al equipo a comprender rápidamente el problema.

### Ejemplos

* Captura de pantalla.
* Video.
* Logs.
* Mensaje de error.
* Respuesta de API.
* Archivo descargado.
* Información del navegador.

### Pero enfatizar

La captura no reemplaza los pasos.

Un reporte como:

> "Adjunto captura."

no explica cómo reproducir el problema.

### Regla

> **La evidencia demuestra o complementa; el reporte explica.**

---

# DIAPOSITIVA 12 — ¿Qué es reproducibilidad?

## Explicación

Definir:

> Un defecto es reproducible cuando podemos ejecutar nuevamente las condiciones necesarias y observar el mismo comportamiento incorrecto.

Explicar que la reproducibilidad facilita muchísimo el trabajo del equipo.

### Preguntar

> "¿Qué creen que ocurre si QA reporta un problema y desarrollo nunca puede reproducirlo?"

Puede ocurrir:

* Retraso.
* Solicitudes de información adicional.
* Dificultad para encontrar la causa.
* Posible cierre del reporte como no reproducible.

### Introducir "Intermittent"

No todos los defectos son reproducibles al 100%.

Un defecto puede ser:

**Always reproducible**

Ocurre siempre.

**Intermittent**

Ocurre solamente algunas veces.

En un defecto intermitente, QA debe proporcionar la mayor cantidad de información posible:

* Hora.
* Usuario.
* Datos.
* Ambiente.
* Frecuencia.
* Logs.
* Video.

---

# DIAPOSITIVA 13 — ¿Qué es la severidad?

## Explicación

Definir:

> Severity representa el impacto que tiene el defecto sobre el sistema o el negocio.

Explicar que los nombres pueden variar entre organizaciones.

Por ejemplo:

* Critical
* High
* Medium
* Low

### Critical

Puede impedir una función esencial o dejar el sistema inutilizable.

### High

Afecta una funcionalidad importante.

### Medium

Afecta parcialmente una funcionalidad.

### Low

Tiene impacto reducido.

### Importante

La severidad debe justificarse por el impacto.

No se debe asignar:

> "High porque parece grave."

Debe explicarse:

> "High porque impide completar el proceso principal de compra."

---

# DIAPOSITIVA 14 — ¿Qué es la prioridad?

## Explicación

Definir:

> Priority representa la urgencia con la que el equipo debería atender un defecto.

Puede utilizar:

* High.
* Medium.
* Low.

Dependiendo del proyecto puede utilizarse:

* P1.
* P2.
* P3.
* etc.

### Pregunta

> "¿Qué tan pronto necesitamos solucionar esto?"

Eso corresponde a prioridad.

---

# DIAPOSITIVA 15 — Severidad vs. Prioridad

Este es un punto donde normalmente existe confusión.

Escribir en la pizarra:

**Severity = Impacto**

**Priority = Urgencia**

### Ejemplo

Error ortográfico en la página principal.

Puede tener:

**Severity: Low**

Porque no rompe una funcionalidad.

Pero podría tener:

**Priority: High**

si la página será presentada públicamente mañana.

### Otro ejemplo

Un error muy grave en una funcionalidad interna que casi nunca se utiliza.

Puede tener:

**Severity: High**

pero una prioridad diferente dependiendo del contexto del negocio.

### Mensaje importante

> **Severity y Priority pueden coincidir, pero no necesariamente tienen que hacerlo.**

---

# DIAPOSITIVA 16 — ¿Quién decide la prioridad?

## Explicación

Aquí debemos evitar enseñar que QA es quien "manda" la prioridad.

QA proporciona información sobre:

* Impacto.
* Reproducibilidad.
* Alcance.
* Riesgo.
* Condiciones del defecto.

Pero la prioridad puede ser determinada por diferentes participantes.

Por ejemplo:

* Product Owner.
* Cliente.
* Project Manager.
* QA.
* Desarrollo.
* Negocio.

### Ejemplo

QA informa:

> "El defecto impide completar pagos."

El Product Owner puede determinar que debe solucionarse inmediatamente debido a la cercanía del lanzamiento.

### Idea clave

> **QA aporta evidencia y contexto; la prioridad puede ser una decisión del equipo o del negocio.**

---

# DIAPOSITIVA 17 — Ciclo de vida de un defecto

## Explicación

Mostrar visualmente:

**NEW → ASSIGNED → IN PROGRESS → FIXED → RETEST → CLOSED**

Explicar que este es un ejemplo de flujo.

No todos los proyectos utilizan exactamente los mismos estados.

### Preguntar

> "¿Qué creen que significa Fixed?"

Escuchar respuestas.

Después aclarar:

**Fixed no significa Closed.**

Fixed significa que desarrollo indica que realizó una corrección.

Todavía falta que QA la verifique.

---

# DIAPOSITIVA 18 — ¿Qué significa cada estado?

Explicar cada estado con un ejemplo sencillo.

### NEW

QA acaba de reportar el defecto.

### ASSIGNED

Se asignó a un responsable.

### IN PROGRESS

Se está trabajando en la solución.

### FIXED

Desarrollo indica que el problema fue corregido.

### RETEST

QA verifica la corrección.

### CLOSED

QA confirma que el problema está solucionado.

### REOPEN

El problema continúa o volvió a aparecer.

### Concepto fundamental

El flujo no siempre es lineal.

Puede ocurrir:

**FIXED → RETEST → REOPEN → IN PROGRESS → FIXED**

Esto puede repetirse hasta solucionar correctamente el defecto.

---

# DIAPOSITIVA 19 — ¿Qué es Jira?

## Explicación

Presentar Jira como una herramienta utilizada para gestionar el trabajo de los equipos.

Puede utilizarse para:

* Bugs.
* Tareas.
* Historias de usuario.
* Incidencias.
* Seguimiento del trabajo.

### Para QA

Jira puede permitir:

* Registrar defectos.
* Adjuntar evidencia.
* Asignar responsables.
* Cambiar estados.
* Añadir comentarios.
* Dar seguimiento.
* Mantener historial.

### Aclaración

Jira es una herramienta.

No es el concepto de QA.

No es Bug Tracking.

Es una herramienta que puede utilizarse para implementar un proceso de seguimiento.

---

# DIAPOSITIVA 20 — Bug Tracking

## Explicación

Definir:

> Bug Tracking es el proceso de registrar, organizar y realizar seguimiento a los defectos durante su ciclo de vida.

### Ejemplo

Sin Bug Tracking:

> "Le escribí al desarrollador por WhatsApp que había un problema."

Después de unos días:

> "¿Qué problema era?"

No existe un seguimiento adecuado.

Con Bug Tracking:

El equipo puede consultar:

* Qué defecto existe.
* Cuándo fue reportado.
* Quién lo reportó.
* Quién trabaja en él.
* Su prioridad.
* Su estado.
* Evidencia.
* Historial.

### Frase clave

> **Jira es la herramienta; Bug Tracking es el proceso.**

---

# DIAPOSITIVA 21 — Antes de registrar un bug

## Explicación

Esta diapositiva enseña una buena práctica.

Antes de crear un Bug, QA debe detenerse y analizar.

### Pregunta 1

> ¿Realmente es un defecto?

No todo comportamiento inesperado es necesariamente un bug.

Puede tratarse de:

* Requisito incorrectamente entendido.
* Comportamiento esperado.
* Configuración.
* Datos incorrectos.
* Problema de ambiente.

### Pregunta 2

> ¿Puedo reproducirlo?

Si puedo reproducirlo, puedo proporcionar pasos concretos.

### Pregunta 3

> ¿Tengo suficiente información?

Debo poder explicar:

**Qué hice → Qué esperaba → Qué ocurrió**

---

# DIAPOSITIVA 22 — Demostración en Jira

## Preparación del docente

Antes de comenzar la demostración:

* Tener Jira disponible.
* Tener un proyecto preparado.
* Tener permisos para crear Issues.
* Preparar una captura de evidencia.
* Tener listo el ejemplo del Bug.

### Explicar

Ahora vamos a pasar de la teoría a una herramienta real.

El objetivo no es memorizar dónde están los botones.

Vamos a observar cómo los conceptos aprendidos se representan en una herramienta.

### Demostración

1. Crear un nuevo Issue.
2. Seleccionar **Bug**.
3. Escribir Summary.
4. Agregar Description.
5. Agregar Steps.
6. Expected Result.
7. Actual Result.
8. Priority.
9. Severity, si está disponible.
10. Environment.
11. Adjuntar evidencia.
12. Crear el Issue.

### Durante la demostración

No llenar los campos rápidamente.

En cada campo preguntar:

> "¿Qué información deberíamos colocar aquí?"

De esta manera los estudiantes participan en la creación del Bug.

---

# DIAPOSITIVA 23 — Ejemplo de Bug en Jira

## Explicación

Mostrar cómo se transforma la teoría en un ticket real.

### Summary

> El sistema permite registrar usuarios menores de 18 años.

Preguntar:

> "¿Podemos entender el problema leyendo solamente el Summary?"

Sí.

### Description

Aquí damos contexto.

Explicar que no necesitamos escribir una historia enorme.

La descripción debe ayudar a entender:

* Dónde ocurre.
* En qué contexto.
* Qué comportamiento se observó.

### Preconditions

Son las condiciones necesarias antes de iniciar los pasos.

---

# DIAPOSITIVA 24 — Ejemplo de Bug en Jira

## Steps to reproduce

Explicar que esta sección debe ser suficientemente precisa para que otra persona pueda reproducir el defecto.

### Expected Result

Debe basarse en:

* Requisito.
* Regla de negocio.
* Criterio de aceptación.

### Actual Result

Debe describir lo que ocurrió.

### Recomendación

Enseñar a los estudiantes a separar claramente:

**Expected = debería ocurrir**

**Actual = ocurrió**

No mezclar ambos.

---

# DIAPOSITIVA 25 — Ejemplo de Bug en Jira

## Severity

Explicar por qué se asignó High.

No decir simplemente:

> "Porque es importante."

Decir:

> "Porque permite crear usuarios que no cumplen una regla de negocio."

### Priority

Explicar que High significa que el equipo considera necesario atenderlo con alta urgencia.

### Evidence

Mostrar cómo se adjunta una captura.

### Environment

Explicar que el comportamiento puede variar dependiendo del ambiente.

Ejemplos:

* QA.
* Staging.
* Production.
* Navegador.
* Sistema operativo.
* Versión de aplicación.

---

# DIAPOSITIVA 26 — ¿Qué ocurre después de crear el Bug?

## Explicación

Aquí comienza el seguimiento.

Mostrar:

**QA**

↓

**Bug Report**

↓

**Equipo**

↓

**Desarrollo**

↓

**Fix**

↓

**QA**

Preguntar:

> "¿Quién decide que el bug está solucionado?"

Aclarar:

Desarrollo puede indicar:

> "Fixed."

Pero QA debe verificarlo.

### Concepto fundamental

> **La corrección declarada por desarrollo debe ser validada por QA.**

---

# DIAPOSITIVA 27 — ¿Qué es Retest?

## Explicación

Definir:

> Retest es volver a ejecutar la prueba que originalmente detectó el defecto para verificar si la corrección funciona.

### Ejemplo

Bug:

> El sistema permite registrar usuarios menores de 18 años.

Después del fix:

QA vuelve a utilizar:

* La misma funcionalidad.
* Las mismas condiciones.
* El escenario que originalmente produjo el problema.

### Pregunta

> "¿Qué estamos comprobando?"

Que el defecto original haya sido solucionado.

---

# DIAPOSITIVA 28 — Resultado del Retest

Explicar los dos caminos.

## Caso 1 — PASS

El defecto ya no ocurre.

Entonces:

**Retest → PASS → CLOSED**

si el proceso del proyecto así lo establece.

## Caso 2 — FAIL

El problema todavía existe.

Entonces:

**Retest → FAIL → REOPEN**

### Importante

También puede ocurrir que el comportamiento haya cambiado parcialmente.

En ese caso QA debe analizar si:

* El defecto original continúa.
* Apareció un nuevo defecto.
* La corrección no cumple completamente el requisito.

---

# DIAPOSITIVA 29 — ¿Qué es Regression Testing?

## Explicación

Este concepto debe explicarse lentamente porque suele confundirse con Retest.

Definir:

> Regression Testing busca comprobar que los cambios realizados no hayan introducido problemas en funcionalidades que anteriormente funcionaban.

### Pregunta principal

> "¿La corrección rompió algo más?"

### Ejemplo

Se modifica la lógica de registro de usuarios.

Aunque el defecto original sea corregido, podemos comprobar:

* Registro.
* Edición.
* Consulta.
* Eliminación.
* Login.
* Reportes relacionados.

---

# DIAPOSITIVA 30 — Ejemplo de Regression Testing

## Explicación

Explicar que no necesariamente debemos probar absolutamente todo el sistema.

La extensión de la regresión depende de:

* Alcance del cambio.
* Riesgo.
* Dependencias.
* Funcionalidades afectadas.
* Tiempo disponible.
* Importancia del sistema.

### Concepto importante

La regresión puede ser:

**Focalizada**

Sobre funcionalidades relacionadas con el cambio.

**Amplia**

Sobre una parte significativa del sistema.

**Completa**

Sobre todo el sistema o un conjunto muy amplio de funcionalidades.

No es necesario entrar profundamente en estrategias de automatización todavía.

---

# DIAPOSITIVA 31 — Retest vs Regression

Esta es una de las diapositivas más importantes.

## Explicación

Utilizar una frase sencilla:

> **Retest pregunta: "¿Se arregló?"**

> **Regression pregunta: "¿Qué más pudo romperse?"**

### Retest

Se concentra en el defecto original.

### Regression

Busca efectos secundarios del cambio.

### Ejemplo

Se arregló:

> "El precio total del carrito no se actualiza."

Retest:

> Cambiar cantidad y comprobar que el precio ahora se actualiza.

Regression:

> Comprobar agregar productos, eliminar productos, modificar cantidades, checkout y otras funciones relacionadas.

---

# DIAPOSITIVA 32 — Ejemplo completo

## Explicación

Utilizar esta diapositiva para conectar todos los conceptos.

### Flujo completo

**1. Se encuentra el problema**

↓

**2. Se documenta**

↓

**3. Desarrollo analiza**

↓

**4. Desarrollo corrige**

↓

**5. QA realiza Retest**

↓

**6. QA realiza Regression**

↓

**7. Se cierra el defecto**

### Pregunta para los estudiantes

> "¿En qué momento intervino QA?"

Respuesta:

En varias etapas:

* Detección.
* Documentación.
* Análisis/comunicación.
* Retest.
* Regression.
* Cierre.

Esto ayuda a romper la idea de que QA solamente "prueba al final".

---

# DIAPOSITIVA 33 — Actividad práctica

## Explicación

Ahora comienza la actividad.

Presentar el escenario:

Un sistema de compras permite:

1. Iniciar sesión.
2. Agregar un producto.
3. Cambiar la cantidad.
4. Actualizar el carrito.

El problema:

> La cantidad cambia correctamente, pero el precio total no se actualiza.

### Antes de escribir el Bug

Preguntar:

> "¿Cuál es el comportamiento esperado?"

Esperar:

> El precio total debe actualizarse de acuerdo con la nueva cantidad.

Después:

> "¿Cuál es el comportamiento actual?"

> El precio permanece incorrecto.

---

# DIAPOSITIVA 34 — Actividad: información del Bug

## Trabajo de los estudiantes

Los estudiantes deben construir el Bug Report.

### 1. Título

Debe ser específico.

Ejemplo esperado:

> "El precio total del carrito no se actualiza al modificar la cantidad del producto."

### 2. Pasos

Deben permitir reproducir el problema.

### 3. Expected

El precio total debe recalcularse.

### 4. Actual

El precio total permanece con el valor anterior.

### 5. Severity

El estudiante debe justificar su decisión.

### 6. Priority

Debe justificar la urgencia.

### 7. Evidence

Debe explicar qué evidencia adjuntaría.

### Importante

No dar inmediatamente las respuestas.

Primero dejar que los estudiantes razonen.

---

# DIAPOSITIVA 35 — Actividad en Jira

## Explicación

Ahora deben llevar su análisis a Jira.

### Proceso

Primero:

**Pensar → Analizar → Documentar**

Después:

**Registrar en Jira**

Esto es importante porque evita que el estudiante aprenda Jira como una secuencia mecánica de botones.

### Mientras trabajan

El docente debe revisar especialmente:

* Títulos demasiado generales.
* Pasos incompletos.
* Expected y Actual mezclados.
* Severidad sin justificación.
* Prioridad confundida con severidad.
* Falta de evidencia.

---

# DIAPOSITIVA 36 — Situación posterior

Presentar:

> "Fixed. Please retest."

Preguntar:

> "¿Qué significa esto?"

Esperamos:

> Desarrollo indica que corrigió el defecto y solicita que QA lo vuelva a probar.

### Pregunta

> "¿Qué prueba hacemos primero?"

Respuesta:

**Retest.**

Explicar:

Debemos volver a ejecutar el escenario que produjo el defecto.

---

# DIAPOSITIVA 37 — Después del Retest

## Caso A

El precio ahora se actualiza correctamente.

**Retest → PASS**

Pero el trabajo todavía puede continuar con:

**Regression Testing**

## Caso B

El precio sigue incorrecto.

**Retest → FAIL**

↓

**REOPEN**

### Pregunta

> "¿Qué debería escribir QA si reabre el defecto?"

Debe proporcionar evidencia actualizada y explicar claramente que el comportamiento incorrecto continúa.

---

# DIAPOSITIVA 38 — ¿Qué aprendimos?

## Explicación

Utilizar esta diapositiva como resumen conceptual.

### Detectar

Identificar comportamientos incorrectos.

### Documentar

Explicar el problema de forma clara y reproducible.

### Comunicar

Proporcionar información útil al equipo.

### Verificar

Comprobar la corrección.

### Prevenir

Buscar efectos secundarios mediante Regression Testing.

### Mensaje

> QA participa durante todo el ciclo de gestión del defecto, no solamente cuando ejecuta una prueba.

---

# DIAPOSITIVA 39 — Conceptos clave

Realizar una revisión rápida.

Preguntar a los estudiantes:

### ¿Qué es un Error?

Esperar:

> Acción o decisión incorrecta realizada por una persona.

### ¿Qué es un Defecto?

> Problema existente en el software.

### ¿Qué es un Fallo?

> Comportamiento incorrecto observable durante la ejecución.

### ¿Qué es Severity?

> Impacto.

### ¿Qué es Priority?

> Urgencia.

### ¿Qué es Retest?

> Verificar la corrección.

### ¿Qué es Regression?

> Buscar efectos secundarios.

---

# DIAPOSITIVA 40 — Preguntas de cierre

Utilizar estas preguntas como evaluación oral rápida.

## Pregunta 1

> ¿Un Bug Report debe contener solamente una captura?

Respuesta:

**No.**

La evidencia complementa el reporte.

---

## Pregunta 2

> ¿Fixed significa que QA ya terminó?

Respuesta:

**No.**

QA debe verificar la corrección.

---

## Pregunta 3

> ¿Qué diferencia existe entre Retest y Regression?

Respuesta:

> Retest verifica el defecto corregido.

> Regression busca efectos secundarios.

---

## Pregunta 4

> ¿Jira es Bug Tracking?

Respuesta:

**No.**

Jira es una herramienta que puede utilizarse para realizar Bug Tracking.

---

# DIAPOSITIVA 41 — Mensaje final

Leer el mensaje:

> "Un buen QA no dice solamente: Encontré un bug."

Después explicar:

Un profesional de QA debe ser capaz de decir:

* Qué ocurrió.
* Dónde ocurrió.
* Cómo reproducirlo.
* Qué debería ocurrir.
* Qué ocurrió realmente.
* Qué impacto tiene.
* Qué evidencia existe.
* Si fue corregido.
* Si la corrección afectó otras funcionalidades.

### Cierre

> **La calidad también significa comunicar correctamente los problemas.**

---

# 4. Conceptos fundamentales que el docente debe reforzar

## 4.1 Error, defecto y fallo

No permitir que los estudiantes utilicen estos términos como sinónimos.

### Error

Está relacionado con la acción humana.

### Defecto

Está presente en el producto/software.

### Fallo

Es la manifestación observable durante la ejecución.

---

## 4.2 Bug Report

Un Bug Report profesional debe permitir que alguien que no estuvo presente durante la prueba pueda entender el problema.

Debe responder:

**¿Qué pasó?**

**¿Dónde pasó?**

**¿Cómo lo reproduzco?**

**¿Qué debería pasar?**

**¿Qué pasó realmente?**

**¿Qué impacto tiene?**

---

## 4.3 Severity

No significa "qué tan molesto es".

Representa el impacto del defecto.

---

## 4.4 Priority

No significa necesariamente "qué tan grave es".

Representa la urgencia de atención.

---

## 4.5 Retest

Pregunta:

> **¿Se corrigió el defecto?**

---

## 4.6 Regression

Pregunta:

> **¿La modificación afectó algo que antes funcionaba?**

---

# 5. Errores frecuentes de los estudiantes

Durante la práctica, prestar especial atención a estos errores.

### Error 1 — Títulos genéricos

❌ "Error en carrito."

Enseñar a mejorar:

✅ "El precio total no se actualiza al modificar la cantidad del producto."

---

### Error 2 — No separar Expected y Actual

❌

> "El precio no se actualiza, debería actualizarse."

Mejor:

**Expected:**

> El precio total debe recalcularse según la cantidad.

**Actual:**

> El precio total permanece sin cambios.

---

### Error 3 — Confundir Severity y Priority

Recordar:

> **Severity = Impacto**

> **Priority = Urgencia**

---

### Error 4 — Pensar que Fixed significa Closed

Explicar:

> Fixed es una afirmación de que se realizó una corrección.

> Closed requiere la validación correspondiente según el proceso del equipo.

---

### Error 5 — Pensar que Retest y Regression son lo mismo

Recordar:

> **Retest = comprobar el arreglo.**

> **Regression = comprobar efectos secundarios.**

---

### Error 6 — Crear el Bug inmediatamente

Enseñar que antes de registrar un defecto debemos analizarlo.

**Observar → Reproducir → Analizar → Documentar → Reportar**

---

# 6. Preguntas que puede realizar el docente durante la clase

### Sobre Bug Reports

> ¿Qué información necesitaría un desarrollador para reproducir este problema?

> ¿Podrías reproducirlo solamente con tu reporte?

> ¿Qué información falta?

### Sobre Severity

> ¿Qué impacto tiene este defecto?

> ¿Impide utilizar una funcionalidad?

### Sobre Priority

> ¿Qué tan urgente sería solucionarlo?

> ¿Quién podría participar en esta decisión?

### Sobre Retest

> Si desarrollo dice "Fixed", ¿qué hacemos?

### Sobre Regression

> ¿Qué otras funcionalidades podrían verse afectadas por este cambio?

### Sobre Jira

> ¿Jira es el proceso o la herramienta?

---

# 7. Actividad práctica — Respuesta esperada del docente

Para el escenario del carrito, una posible solución sería:

### Summary

> El precio total del carrito no se actualiza al modificar la cantidad del producto.

### Preconditions

* Usuario autenticado.
* Existe al menos un producto disponible.
* El producto fue agregado al carrito.

### Steps

1. Iniciar sesión.
2. Agregar un producto al carrito.
3. Cambiar la cantidad de 1 a 3.
4. Seleccionar **Actualizar carrito**.

### Expected Result

El precio total debe recalcularse de acuerdo con la nueva cantidad.

### Actual Result

La cantidad cambia, pero el precio total permanece calculado para la cantidad anterior.

### Evidence

Captura o video mostrando:

* Cantidad seleccionada.
* Precio unitario.
* Precio total.

### Severity

El estudiante debe justificar su elección según el impacto.

### Priority

El estudiante debe justificarla según la urgencia y el contexto del negocio.

**Importante:** no exigir que todos asignen exactamente la misma severidad o prioridad si pueden justificar razonablemente su decisión. El objetivo es aprender a **argumentar la clasificación**.

---

# 8. Cierre de la clase

Finalizar con una pregunta:

> "Si mañana empiezan a trabajar como QA y encuentran un defecto, ¿qué deberían hacer?"

La respuesta esperada debe incluir:

1. Reproducir el problema.
2. Analizarlo.
3. Documentarlo.
4. Adjuntar evidencia.
5. Clasificarlo.
6. Registrarlo.
7. Dar seguimiento.
8. Realizar Retest después de la corrección.
9. Realizar Regression Testing cuando corresponda.
10. Cerrar el defecto después de la validación correspondiente.

### Idea final para los estudiantes

> **Un QA profesional no solamente encuentra defectos; genera información de calidad para que el equipo pueda resolverlos y verifica que las soluciones no introduzcan nuevos problemas.**
