# GUÍA DEL DOCENTE

## Módulo: Estrategia de Aseguramiento de la Calidad y Pruebas Manuales

### Clase 6 — Usabilidad, Accesibilidad y Test Plan Management

**Duración:** 2 horas
**Unidades:** U6 + U7
**Modalidad:** Teoría + demostración + laboratorio + ejercicio integrador

---

# 1. PROPÓSITO DE LA CLASE

Esta clase representa el cierre del módulo.

Durante las clases anteriores los estudiantes aprendieron a:

* Comprender requisitos.
* Analizar requisitos desde QA.
* Diseñar casos de prueba.
* Aplicar técnicas de diseño.
* Ejecutar pruebas manuales.
* Reportar defectos.
* Realizar pruebas de API.
* Utilizar Postman.

En esta clase se incorporan dos perspectivas adicionales:

### Perspectiva del usuario

> ¿El sistema es fácil de utilizar y accesible?

### Perspectiva de gestión

> ¿Cómo organizamos y planificamos todas las actividades de testing?

Por eso la clase se divide en:

**U6 — Usabilidad y Accesibilidad**

y

**U7 — Test Plan Management**

---

# 2. OBJETIVOS DE APRENDIZAJE

Al finalizar la clase, el estudiante podrá:

1. Explicar qué es usabilidad.
2. Identificar problemas básicos de usabilidad.
3. Explicar qué es accesibilidad.
4. Reconocer los cuatro principios POUR de WCAG.
5. Utilizar WAVE para realizar una revisión inicial de accesibilidad.
6. Comprender las limitaciones de las herramientas automáticas.
7. Realizar una prueba básica de navegación mediante teclado.
8. Registrar hallazgos de usabilidad y accesibilidad.
9. Explicar qué es un Test Plan.
10. Identificar sus principales componentes.
11. Comprender el propósito general de ISO/IEC/IEEE 29119.
12. Explicar qué es un Master Test Plan.
13. Elaborar un Mini Test Plan.

---

# 3. DISTRIBUCIÓN DEL TIEMPO

| Bloque | Actividad                  |      Tiempo |
| ------ | -------------------------- | ----------: |
| 1      | Introducción               |      10 min |
| 2      | Usabilidad                 |      15 min |
| 3      | Laboratorio de usabilidad  |      15 min |
| 4      | Accesibilidad + WCAG       |      15 min |
| 5      | Laboratorio WAVE + teclado |      20 min |
| 6      | Test Plan Management       |      20 min |
| 7      | ISO 29119 + MTP            |      10 min |
| 8      | Mini Test Plan             |      10 min |
| 9      | Cierre                     |       5 min |
|        | **Total**                  | **120 min** |

---

# DIAPOSITIVA 1 — PORTADA

## Estrategia de Aseguramiento de la Calidad y Pruebas Manuales

### Clase 6

Usabilidad · Accesibilidad · Test Plan Management

## Qué debe explicar el docente

Presentar esta clase como el cierre del módulo.

Decir:

> "Durante las clases anteriores hemos aprendido cómo analizar requisitos, diseñar pruebas, ejecutarlas, reportar defectos y probar APIs. Hoy vamos a ampliar nuestra visión de calidad y finalmente veremos cómo planificar todo ese trabajo."

Explicar que esta clase tiene dos grandes preguntas:

> "¿El sistema funciona correctamente?"

y ahora:

> "¿Es fácil y accesible para el usuario?"

Después:

> "¿Cómo organizamos todas esas pruebas dentro de un proyecto?"

---

# DIAPOSITIVA 2 — ¿QUÉ VEREMOS HOY?

Explicar brevemente cada punto.

No detenerse demasiado aquí.

Indicar que habrá dos laboratorios:

### Laboratorio 1

Evaluación de **usabilidad**.

### Laboratorio 2

Evaluación de **accesibilidad utilizando WAVE**.

Y finalmente:

### Ejercicio integrador

Construcción de un **Mini Test Plan**.

## Pregunta al grupo

> "¿Cuál de estos temas creen que está más relacionado con el trabajo diario de un QA?"

Permitir algunas respuestas.

La idea es demostrar que **todos están relacionados**.

---

# DIAPOSITIVA 3 — ¿QUÉ HEMOS APRENDIDO?

Esta diapositiva sirve para conectar todo el módulo.

Mostrar:

Requisitos
↓
Diseño
↓
Ejecución
↓
Defectos
↓
API Testing
↓
Usabilidad y Accesibilidad
↓
Planificación

## Explicación

Recordar brevemente:

### Clase 1

Fundamentos de QA y testing.

### Clase 2

Requisitos y STLC.

### Clase 3

Diseño de casos de prueba.

### Clase 4

Bug Tracking y Reporting.

### Clase 5

API Testing con Postman.

### Clase 6

Usabilidad, accesibilidad y planificación.

## Pregunta clave

> "Si todas las pruebas funcionales pasan, ¿podemos afirmar que el software tiene buena calidad?"

### Respuesta esperada

No necesariamente.

Puede:

* Ser difícil de usar.
* Tener problemas de accesibilidad.
* Presentar mala experiencia de usuario.
* No funcionar adecuadamente con teclado o tecnologías de asistencia.

---

# UNIDAD 6 — USABILIDAD

# DIAPOSITIVA 4 — ¿QUÉ ES LA USABILIDAD?

Definición:

> La usabilidad es la capacidad de un sistema para permitir que los usuarios alcancen sus objetivos de manera efectiva, eficiente y satisfactoria.

## Explicar los tres conceptos

### Efectividad

¿El usuario consigue realizar la tarea?

### Eficiencia

¿Puede realizarla sin pasos o esfuerzo innecesario?

### Satisfacción

¿La experiencia resulta clara y adecuada?

No es necesario profundizar en teorías de UX.

## Ejemplo

Supongamos una página donde comprar un producto.

El usuario debe:

1. Buscar producto.
2. Abrir producto.
3. Agregar al carrito.
4. Ir al carrito.
5. Confirmar compra.

Si el usuario entiende claramente cada paso, la interfaz puede ser usable.

Si existen botones ambiguos, navegación confusa o pasos innecesarios, tenemos posibles problemas de usabilidad.

## Mensaje importante

> "Un sistema puede funcionar técnicamente y aun así ser difícil de utilizar."

---

# DIAPOSITIVA 5 — ¿QUÉ OBSERVA QA?

Explicar cada pregunta.

### ¿Entiendo?

El usuario debería comprender qué debe hacer.

### ¿Sé dónde estoy?

La navegación debe proporcionar orientación.

### ¿Puedo hacerlo fácilmente?

Debemos detectar pasos innecesarios.

### ¿Qué ocurre si me equivoco?

El sistema debe ayudar al usuario a recuperarse.

### ¿El sistema me informa?

Debe existir retroalimentación.

## Pregunta

> "Si presiono un botón y no ocurre nada visible, ¿qué problema tenemos?"

Respuesta:

Puede existir un problema de feedback o incluso un defecto funcional, dependiendo del comportamiento esperado.

---

# DIAPOSITIVA 6 — EJEMPLO DE PROBLEMA DE USABILIDAD

Explicar:

El botón dice:

> "Continuar"

pero no queda claro qué ocurrirá.

Por ejemplo, podría:

* Guardar información.
* Pasar al siguiente paso.
* Confirmar una compra.
* Enviar un formulario.

## Pregunta

> "¿El botón está necesariamente mal?"

Respuesta:

No necesariamente.

Depende del contexto y del objetivo de la interfaz.

Lo importante es:

> ¿El usuario puede entender claramente la acción?

## Enseñanza QA

No debemos reportar todo lo que personalmente "no nos gusta".

Debemos justificar el hallazgo mediante:

* comportamiento;
* contexto;
* objetivo del usuario;
* impacto.

---

# DIAPOSITIVA 7 — OTROS PROBLEMAS DE USABILIDAD

Explicar rápidamente cada ejemplo.

### Navegación confusa

El usuario no encuentra cómo regresar o avanzar.

### Botones poco claros

No queda claro qué acción ejecutan.

### Información desorganizada

El contenido importante es difícil de encontrar.

### Mensajes incomprensibles

El usuario recibe un error técnico que no sabe interpretar.

### Pasos innecesarios

La tarea requiere acciones que no aportan valor.

### Inconsistencia

Dos botones similares tienen comportamientos diferentes.

### Falta de confirmación

El usuario realiza una acción pero no sabe si fue exitosa.

## Mensaje clave

> "QA no solamente verifica si una acción funciona; también puede evaluar si la interacción permite al usuario alcanzar su objetivo de manera clara."

---

# DIAPOSITIVA 8 — LABORATORIO: EVALUEMOS UNA WEB

## Objetivo

Los estudiantes deben encontrar un problema real de usabilidad.

## Instrucciones

1. Abrir la página seleccionada.
2. Observar la interfaz.
3. Elegir una tarea que un usuario intentaría realizar.
4. Recorrer la interfaz.
5. Identificar una dificultad.
6. Documentarla.

## Importante

No queremos que busquen errores técnicos.

Queremos que piensen:

> "Soy un usuario. ¿Qué me dificulta completar mi objetivo?"

---

# DIAPOSITIVA 9 — CHECKLIST DE USABILIDAD

Pedir a los estudiantes que utilicen la tabla como guía.

## Navegación

> ¿Sé dónde estoy?

## Claridad

> ¿Entiendo qué debo hacer?

## Acciones

> ¿Los botones son claros?

## Información

> ¿Está organizada?

## Errores

> ¿Sé cómo solucionar un error?

## Feedback

> ¿El sistema informa lo ocurrido?

## Consistencia

> ¿Los elementos funcionan de manera coherente?

---

# DIAPOSITIVA 10 — REPORTA TU HALLAZGO

Aquí hacemos conexión directa con la **Clase 4**.

Recordar la estructura del Bug Report.

### Título

Debe describir el problema.

### Descripción

Explica qué ocurre.

### Impacto

Explica por qué importa.

### Evidencia

Captura o información adicional.

## Ejemplo

**Título:**

> El botón no indica claramente la acción que realizará.

**Descripción:**

> El usuario encuentra un botón denominado "Continuar", pero la interfaz no indica cuál será el siguiente paso.

**Impacto:**

> Puede generar incertidumbre y dificultar la navegación.

## Pregunta

> "¿Esto necesariamente es un bug funcional?"

Respuesta:

No. Puede ser un **hallazgo de usabilidad**.

Dependiendo del sistema y del proceso utilizado, puede registrarse como:

* Usability issue.
* Defect.
* Improvement.

---

# DIAPOSITIVA 11 — ¿QUÉ ES ACCESIBILIDAD?

Explicar:

La accesibilidad busca que las personas puedan utilizar el sistema independientemente de diferentes capacidades o necesidades.

Podemos mencionar:

* Personas con discapacidad visual.
* Personas con discapacidad auditiva.
* Personas con dificultades motoras.
* Personas con dificultades cognitivas.

Pero evitar presentar la accesibilidad únicamente como algo relacionado con discapacidad.

También puede beneficiar a usuarios que:

* utilizan dispositivos diferentes;
* tienen conexiones limitadas;
* utilizan el sistema en condiciones especiales.

## Mensaje clave

> "La accesibilidad busca eliminar barreras innecesarias para utilizar el software."

---

# DIAPOSITIVA 12 — USABILIDAD ≠ ACCESIBILIDAD

Esta distinción es muy importante.

### Usabilidad

> ¿Es fácil utilizar el sistema?

### Accesibilidad

> ¿Puede utilizarlo una persona con diferentes capacidades y necesidades?

## Ejemplo

Un formulario puede ser muy fácil de utilizar con mouse.

Pero si no puede utilizarse mediante teclado:

> Puede presentar un problema de accesibilidad.

## Idea para el estudiante

Las dos disciplinas están relacionadas, pero **no son exactamente lo mismo**.

---

# DIAPOSITIVA 13 — WCAG

Explicar:

**WCAG = Web Content Accessibility Guidelines**

Son las **Pautas de Accesibilidad para el Contenido Web**.

Indicar que proporcionan recomendaciones para mejorar la accesibilidad.

No intentar explicar toda WCAG.

Nuestro objetivo es que el estudiante recuerde:

> WCAG organiza la accesibilidad web alrededor de cuatro principios: POUR.

---

# DIAPOSITIVA 14 — P: PERCEPTIBLE

Explicar:

El usuario debe poder percibir la información.

### Ejemplos

* Texto alternativo para imágenes.
* Contraste adecuado.
* Información que no dependa solamente del color.

## Ejemplo

Incorrecto:

> 🔴 significa error.

Pero no existe ninguna otra indicación.

Mejor:

> 🔴 Error: la contraseña es incorrecta.

El color complementa la información, pero no es la única fuente.

---

# DIAPOSITIVA 15 — O: OPERABLE

La interfaz debe poder utilizarse.

### Ejemplo principal

Navegación mediante teclado.

Preguntar:

> "¿Qué pasa si una persona no puede utilizar un mouse?"

Debe poder interactuar con los controles mediante mecanismos alternativos apropiados.

## Prueba QA

Utilizar:

TAB

SHIFT + TAB

ENTER

SPACE

---

# DIAPOSITIVA 16 — U: COMPRENSIBLE

La información y funcionamiento deben ser comprensibles.

### Ejemplos

Un mensaje como:

> "Error 500."

no ayuda mucho al usuario.

Un mensaje más útil podría indicar:

> "No pudimos completar la operación. Inténtalo nuevamente."

En un contexto de testing debemos distinguir:

* mensaje técnico para logs;
* mensaje útil para el usuario.

---

# DIAPOSITIVA 17 — R: ROBUSTO

Explicar que el contenido debería funcionar correctamente con diferentes tecnologías y agentes de usuario.

Mencionar:

* Diferentes navegadores.
* Tecnologías de asistencia.
* Lectores de pantalla.

No profundizar en implementación técnica.

## Idea clave

> "La interfaz no debe depender de una única forma de interacción o interpretación."

---

# DIAPOSITIVA 18 — POUR EN UNA SOLA VISTA

Esta diapositiva sirve para memorizar.

### P

**Perceptible**

¿Puedo percibir la información?

### O

**Operable**

¿Puedo utilizar los controles?

### U

**Comprensible**

¿Entiendo la información?

### R

**Robusto**

¿Funciona correctamente con diferentes tecnologías?

## Técnica didáctica

Pedir al grupo que repita:

> **P — O — U — R**

Después hacer preguntas aleatorias:

> "Si el problema es que no puedo utilizar un botón con teclado, ¿qué principio?"

Respuesta:

**Operable.**

> "Si una imagen no tiene información alternativa, ¿qué principio?"

Respuesta:

**Perceptible.**

---

# DIAPOSITIVA 19 — HERRAMIENTA WAVE

Abrir en vivo:

[WAVE Accessibility Evaluation Tool](https://wave.webaim.org/?utm_source=chatgpt.com)

## Antes de la demostración

Explicar:

> "Vamos a utilizar una herramienta automática para obtener indicadores iniciales de accesibilidad."

Mostrar cómo:

1. Introducir URL.
2. Ejecutar análisis.
3. Revisar indicadores.
4. Seleccionar un elemento.
5. Leer la explicación.

## No convertir esto en una clase de WAVE

El objetivo no es aprender todas sus funcionalidades.

El objetivo es:

> **Aprender a utilizar una herramienta como apoyo al trabajo de QA.**

---

# DIAPOSITIVA 20 — ¿QUÉ DEBEMOS BUSCAR?

Explicar:

### Errors

Problemas identificados automáticamente.

### Alerts

Elementos que necesitan revisión humana.

### Contrast

Posibles problemas de contraste.

### Forms

Revisión de formularios y etiquetas.

### Structure

Estructura semántica del documento.

## Advertencia

No enseñar:

> "Todo lo rojo es un bug."

Enseñar:

> "Todo resultado debe ser analizado por QA."

---

# DIAPOSITIVA 21 — WAVE NO REEMPLAZA A QA

Esta es una de las diapositivas más importantes de la clase.

Explicar:

Una herramienta automática:

* detecta determinados patrones;
* acelera la revisión;
* proporciona evidencia;
* ayuda a encontrar posibles problemas.

Pero no puede evaluar completamente:

* intención;
* contexto;
* experiencia;
* facilidad de uso;
* todas las interacciones;
* todas las necesidades del usuario.

## Frase para enfatizar

> **"Automatizar la detección no significa automatizar el criterio del QA."**

---

# DIAPOSITIVA 22 — PRUEBA MANUAL: SOLO TECLADO

Pedir a los estudiantes que dejen de utilizar el mouse.

### TAB

Avanzar.

### SHIFT + TAB

Retroceder.

### ENTER

Activar elementos compatibles.

### SPACE

Interactuar con controles compatibles.

## Preguntas

1. ¿Todos los elementos interactivos son alcanzables?
2. ¿El foco es visible?
3. ¿Puedo saber dónde estoy?
4. ¿Puedo completar la tarea?
5. ¿Me quedo atrapado en algún elemento?

---

# DIAPOSITIVA 23 — LABORATORIO: RESULTADO

Los estudiantes deben producir tres resultados:

### 1. Problema de usabilidad

Detectado mediante observación.

### 2. Problema de accesibilidad

Detectado mediante WAVE o análisis manual.

### 3. Resultado de teclado

Indicar si pudieron completar la tarea y qué dificultades encontraron.

## Formato sugerido

**Título**

**Descripción**

**Impacto**

**Evidencia**

Esto puede entregarse como ejercicio corto.

---

# UNIDAD 7 — TEST PLAN MANAGEMENT

# DIAPOSITIVA 24 — DE PROBAR A PLANIFICAR

Aquí debemos cambiar la mentalidad.

Decir:

> "Hasta ahora hemos estado pensando principalmente como testers que ejecutan pruebas."

Ahora:

> "Vamos a pensar como QA que participa en la planificación."

## Pregunta

> "Antes de empezar a probar un sistema, ¿qué necesitamos saber?"

Esperar respuestas como:

* Qué probar.
* Cuándo.
* Cómo.
* Con qué datos.
* En qué ambiente.
* Quién lo hará.

---

# DIAPOSITIVA 25 — ¿QUÉ ES UN TEST PLAN?

Definición:

> Un Test Plan es un documento que define cómo se organizarán y ejecutarán las actividades de testing de un proyecto.

Explicar que no necesariamente existe una única plantilla universal.

La estructura puede cambiar dependiendo de:

* empresa;
* proyecto;
* metodología;
* tamaño;
* riesgos.

Pero normalmente encontraremos información relacionada con:

* alcance;
* estrategia;
* recursos;
* ambiente;
* riesgos;
* criterios;
* entregables.

---

# DIAPOSITIVA 26 — COMPONENTES DE UN TEST PLAN

Explicar cada componente brevemente.

### Objetivo

Qué queremos lograr.

### Alcance

Qué se probará.

### Fuera de alcance

Qué no se probará.

### Estrategia

Cómo se realizarán las pruebas.

### Tipos de pruebas

Qué técnicas o niveles se utilizarán.

### Recursos

Personas, herramientas y ambientes.

### Ambiente

Dónde se probará.

### Datos

Qué información se necesita.

### Riesgos

Qué puede afectar el testing.

### Criterios de entrada

Cuándo se puede comenzar.

### Criterios de salida

Cuándo podemos terminar.

### Entregables

Qué resultados generará QA.

---

# DIAPOSITIVA 27 — CRITERIOS DE ENTRADA Y SALIDA

Este concepto merece explicación adicional.

## Criterios de entrada

Son condiciones necesarias antes de comenzar.

Ejemplo:

> La versión está desplegada en QA.

> Las funcionalidades incluidas están disponibles.

## Criterios de salida

Condiciones que deben cumplirse para cerrar una etapa.

Ejemplo:

> Los casos críticos fueron ejecutados.

> No existen defectos críticos abiertos.

## Pregunta

> "¿Significa que si encontramos un bug debemos detener todas las pruebas?"

Respuesta:

No necesariamente.

Depende de:

* severidad;
* impacto;
* riesgo;
* alcance;
* estrategia del proyecto.

---

# DIAPOSITIVA 28 — ISO/IEC/IEEE 29119

Explicar que esta familia de estándares proporciona un marco relacionado con el testing de software.

### 29119-1

Conceptos y vocabulario.

### 29119-2

Procesos de testing.

### 29119-3

Documentación.

## Importante

No decir que la norma "obliga a todas las empresas a utilizar exactamente esta plantilla".

La explicación correcta para este curso es:

> "Proporciona un marco y buenas prácticas estandarizadas para organizar procesos y documentación de pruebas."

## Pregunta

> "¿Para qué nos sirve conocer una norma como QA?"

Respuesta esperada:

Para comprender que el testing puede gestionarse de manera estructurada y documentada.

---

# DIAPOSITIVA 29 — MASTER TEST PLAN

Explicar:

Un **Master Test Plan** proporciona una visión global de la estrategia y organización del testing cuando existen múltiples áreas, niveles o actividades.

### Ejemplo

Un proyecto grande puede tener:

* pruebas funcionales;
* API;
* integración;
* rendimiento;
* accesibilidad;
* seguridad.

El MTP permite visualizar cómo se organiza el esfuerzo global.

## Aclaración

No pedir a los estudiantes que memoricen una estructura específica de MTP.

Lo importante es comprender:

> **MTP = visión global de la estrategia de testing.**

---

# DIAPOSITIVA 30 — EJERCICIO INTEGRADOR

## Sistema de compras

Presentar el escenario:

> "Tenemos un sistema de compras donde el usuario puede buscar productos, agregarlos al carrito, modificar cantidades y realizar una compra."

## Trabajo

Los estudiantes deben crear un Mini Test Plan.

### Deben definir

**Objetivo**

¿Por qué probaremos?

**Alcance**

¿Qué probaremos?

**Fuera de alcance**

¿Qué no probaremos?

**Tipos de pruebas**

¿Cómo lo probaremos?

**Ambiente**

¿Dónde?

**Riesgo**

¿Qué podría afectar?

**Criterio de entrada**

¿Qué necesitamos antes de comenzar?

**Criterio de salida**

¿Qué necesitamos para finalizar?

---

# SOLUCIÓN ORIENTATIVA PARA EL DOCENTE

No mostrar inmediatamente.

Primero permitir que trabajen.

Después comparar.

### Objetivo

> Verificar el correcto funcionamiento de las principales funcionalidades del proceso de compra.

### Alcance

* Búsqueda de productos.
* Carrito.
* Modificación de cantidades.
* Compra.

### Fuera de alcance

> Administración interna de productos.

### Tipos de pruebas

* Funcionales.
* Exploratorias.
* Regresión.
* Usabilidad.
* Accesibilidad.

### Ambiente

> Ambiente QA con navegador compatible y datos de prueba.

### Riesgo

> Indisponibilidad del ambiente de pruebas.

### Criterio de entrada

> Las funcionalidades están desplegadas y disponibles en QA.

### Criterio de salida

> Los casos críticos fueron ejecutados y no existen defectos críticos abiertos.

---

# DIAPOSITIVA 31 — CONECTEMOS TODO

Esta diapositiva debe ser explicada lentamente.

## El proceso completo

### 1. Requisitos

¿Qué debe hacer el sistema?

↓

### 2. Análisis

¿Qué debemos validar?

↓

### 3. Diseño

¿Cómo lo vamos a probar?

↓

### 4. Ejecución

¿Funciona?

↓

### 5. Defectos

¿Qué problemas encontramos?

↓

### 6. API Testing

¿Las interfaces de comunicación funcionan?

↓

### 7. Usabilidad y accesibilidad

¿El sistema puede utilizarse de manera clara y accesible?

↓

### 8. Planificación

¿Cómo organizamos todo el proceso?

## Mensaje

> "QA no es una actividad aislada al final del desarrollo."

---

# DIAPOSITIVA 32 — ¿QUÉ APRENDIMOS?

Repasar los principales resultados.

El estudiante debería poder decir:

> "Puedo analizar requisitos."

> "Puedo diseñar casos de prueba."

> "Puedo ejecutar pruebas."

> "Puedo reportar defectos."

> "Puedo probar APIs."

> "Puedo evaluar usabilidad."

> "Puedo identificar problemas básicos de accesibilidad."

> "Puedo utilizar una herramienta como WAVE."

> "Puedo estructurar un Test Plan."

> "Comprendo para qué existe ISO/IEC/IEEE 29119."

## Cierre

Utilizar esta frase:

> **"QA no consiste solamente en encontrar errores. QA busca aportar calidad durante todo el proceso de desarrollo."**

---

# 4. GUÍA ESPECÍFICA PARA EL LABORATORIO WAVE

## Objetivo

Que el estudiante experimente una evaluación real de accesibilidad y comprenda la diferencia entre:

**herramienta automática**

y

**evaluación humana.**

## Preparación del docente

Antes de la clase:

1. Seleccionar una página pública.
2. Verificar que WAVE pueda analizarla.
3. Tener preparada una segunda página como alternativa.
4. Comprobar que los estudiantes puedan acceder a Internet.

No es necesario buscar una página "perfecta" o "mala".

Lo importante es que existan elementos que permitan discutir los resultados.

## Procedimiento

### Paso 1

Abrir WAVE.

### Paso 2

Introducir la URL.

### Paso 3

Analizar los resultados.

### Paso 4

Seleccionar un error.

### Paso 5

Leer la explicación.

### Paso 6

Preguntar:

> "¿Esto es realmente un problema para el usuario?"

### Paso 7

Buscar evidencia.

### Paso 8

Registrar el hallazgo.

---

# 5. GUÍA DE LA PRUEBA DE TECLADO

Pedir a los estudiantes:

> "Ahora no pueden utilizar el mouse."

Realizar una tarea sencilla.

Por ejemplo:

> Buscar información o completar un formulario.

## Deben observar

### Foco

¿Es visible?

### Orden

¿El recorrido tiene sentido?

### Accesibilidad

¿Todos los controles son alcanzables?

### Bloqueos

¿Algún elemento impide continuar?

### Formularios

¿Puedo introducir la información?

## Resultado

Cada estudiante debe indicar:

**PASÓ**

o

**SE ENCONTRÓ UN PROBLEMA**

y explicar por qué.

---

# 6. PREGUNTAS PARA GENERAR PARTICIPACIÓN

Durante la clase se pueden utilizar preguntas como:

### Usabilidad

> ¿Qué hace que una interfaz sea fácil de aprender?

> ¿Un sistema puede ser funcional pero difícil de utilizar?

> ¿Todo problema de usabilidad es un bug?

### Accesibilidad

> ¿Qué pasa si un usuario no puede utilizar el mouse?

> ¿Por qué no debemos depender únicamente del color?

> ¿Puede una herramienta automática detectar todos los problemas?

### Test Plan

> ¿Qué pasaría si comenzamos a probar sin saber el alcance?

> ¿Por qué necesitamos criterios de entrada?

> ¿Por qué necesitamos criterios de salida?

### QA

> ¿Cuál es la diferencia entre encontrar un problema y demostrar que existe?

Estas preguntas ayudan a desarrollar pensamiento crítico de QA.

---

# 7. ERRORES CONCEPTUALES QUE DEBEMOS EVITAR

## ❌ Error 1

"Usabilidad significa que la página se vea bonita."

### Corrección

Usabilidad está relacionada con la facilidad y efectividad para alcanzar objetivos.

---

## ❌ Error 2

"Accesibilidad significa solamente usar lectores de pantalla."

### Corrección

Los lectores de pantalla son una parte del tema. Accesibilidad incluye diferentes necesidades y formas de interacción.

---

## ❌ Error 3

"Si WAVE no muestra errores, la página es accesible."

### Corrección

Una herramienta automática tiene un alcance limitado.

Debe complementarse con evaluación humana.

---

## ❌ Error 4

"Todo resultado de WAVE es automáticamente un bug."

### Corrección

El QA debe analizar contexto, impacto y comportamiento esperado.

---

## ❌ Error 5

"Un Test Plan es solamente una lista de casos de prueba."

### Corrección

El Test Plan establece cómo se organizará y gestionará el esfuerzo de testing.

---

## ❌ Error 6

"ISO 29119 es una plantilla obligatoria que todas las empresas deben copiar."

### Corrección

Es una familia de estándares que proporciona conceptos, procesos y documentación relacionados con testing.

---

# 8. ACTIVIDAD FINAL RECOMENDADA

Como cierre del módulo, pedir al estudiante que complete:

## Mini Test Plan

### 1. Objetivo

---

### 2. Alcance

---

### 3. Fuera de alcance

---

### 4. Tipos de prueba

---

### 5. Ambiente

---

### 6. Datos de prueba

---

### 7. Riesgos

---

### 8. Criterios de entrada

---

### 9. Criterios de salida

---

### 10. Entregables

---

---

# 9. CRITERIOS DE EVALUACIÓN DE LA ACTIVIDAD

La actividad puede evaluarse de manera sencilla:

| Criterio                                | Logrado |
| --------------------------------------- | ------- |
| Identifica un problema de usabilidad    | ✅       |
| Identifica un problema de accesibilidad | ✅       |
| Presenta evidencia                      | ✅       |
| Explica el impacto                      | ✅       |
| Comprende POUR                          | ✅       |
| Define alcance                          | ✅       |
| Define estrategia/tipos de prueba       | ✅       |
| Identifica un riesgo                    | ✅       |
| Define criterio de entrada              | ✅       |
| Define criterio de salida               | ✅       |

No es necesario convertirlo en una evaluación pesada.

El objetivo es comprobar que **comprendieron los conceptos y pueden aplicarlos**.

---

# 10. MENSAJE FINAL DEL DOCENTE

Cerrar la clase con:

> "Durante este módulo hemos visto que el trabajo de QA no consiste solamente en ejecutar casos de prueba."
>
> "Un QA debe comprender los requisitos, identificar riesgos, diseñar pruebas, ejecutarlas, reportar problemas, verificar correcciones, evaluar diferentes aspectos de calidad y participar en la planificación."
>
> "La calidad no se agrega únicamente al final del desarrollo. Se construye y se verifica durante todo el proceso."

---

# 11. CONEXIÓN CON EL PERFIL PROFESIONAL

Es importante que el estudiante vea la utilidad laboral del contenido.

Un QA puede participar en actividades como:

* Análisis de requisitos.
* Diseño de casos.
* Testing funcional.
* Exploratory Testing.
* API Testing.
* Regression Testing.
* Accessibility Testing.
* Usability Testing.
* Defect Management.
* Test Planning.
* Test Reporting.
* Risk Analysis.

Por eso las dos últimas unidades amplían la visión del estudiante:

**U6 → Calidad desde la perspectiva del usuario**

**U7 → Calidad desde la perspectiva de la planificación y gestión**

---

# 12. RESUMEN DEL DOCENTE

### Antes de la clase

* Tener preparada una web para evaluar.
* Verificar acceso a WAVE.
* Tener una alternativa por si la primera web no puede analizarse.
* Preparar el escenario del sistema de compras.

### Durante la clase

**Explicar poco → demostrar → hacer practicar → discutir.**

Especialmente en:

* Usabilidad.
* WAVE.
* Prueba de teclado.
* Mini Test Plan.

### Evitar

* Explicaciones excesivamente teóricas de WCAG.
* Memorizar toda ISO/IEC/IEEE 29119.
* Convertir WAVE en un curso de la herramienta.
* Hacer una plantilla de Test Plan demasiado compleja.

### Priorizar

> **Pensamiento crítico de QA.**

El estudiante debe aprender a preguntar:

> **¿Qué problema existe?**

> **¿Cómo puedo demostrarlo?**

> **¿A quién afecta?**

> **¿Qué riesgo representa?**

> **¿Cómo debería probarlo?**

> **¿Cómo lo documentaría?**

---

# RESULTADO ESPERADO DE LA CLASE

Al terminar las dos horas, el estudiante debería haber pasado de:

> "Sé qué significa usabilidad y accesibilidad."

a:

> **"Puedo evaluar una aplicación, encontrar un problema, obtener evidencia, documentarlo y considerar esa actividad dentro de un plan de pruebas."**

Ese es el objetivo principal de esta Clase 6 y, al mismo tiempo, el cierre práctico del módulo.
