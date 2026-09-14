# MÓDULO 3 - DFSQA-03
# Estrategia de Aseguramiento de la Calidad y Pruebas Manuales

**Duración total:** 12 horas  
**Número de clases:** 6  
**Duración por clase:** 2 horas  
**Modalidad:** Teórico-práctica  

---

# 1. Objetivo General

Desarrollar en los participantes los conocimientos fundamentales para analizar requerimientos, diseñar y ejecutar pruebas de software, gestionar defectos, realizar pruebas de APIs, evaluar aspectos básicos de usabilidad y accesibilidad, y comprender la planificación de pruebas dentro de una estrategia de aseguramiento de calidad.

La automatización será incorporada de manera **introductoria y transversal**, mostrando su relación con las pruebas manuales y la estrategia de QA, sin profundizar en herramientas o frameworks específicos.

---

# 2. Metodología

El módulo tendrá un enfoque principalmente teórico, complementado con ejemplos guiados y pequeñas actividades de aplicación.

| Actividad | Porcentaje | Tiempo aproximado |
|---|---:|---:|
| Teoría y explicación | **70%** | **84 min** |
| Ejemplos guiados | **25%** | **30 min** |
| Práctica corta | **5%** | **6 min** |

## Dinámica general

```text
CONCEPTO
   ↓
EXPLICACIÓN
   ↓
EJEMPLO
   ↓
EJEMPLO GUIADO
   ↓
PRÁCTICA CORTA
   ↓
CONCLUSIÓN
```

Las prácticas tendrán como objetivo reforzar y comprobar la comprensión de los contenidos, evitando convertir cada sesión en un taller extenso.

---

# 3. Plan General de Clases

| Clase | Unidad | Tema principal |
|---|---|---|
| 1 | Unidad 1 | Fundamentos del QA y mentalidad del tester |
| 2 | Unidad 2 | Gestión de requerimientos y STLC |
| 3 | Unidad 3 | Diseño de casos de prueba e introducción a automatización |
| 4 | Unidad 4 | Bug Tracking, Reporting y pruebas de regresión |
| 5 | Unidad 5 | API Testing con Postman y ejemplo de automatización |
| 6 | Unidad 6 + 7 | Usabilidad, accesibilidad y Test Plan Management |

---

# CLASE 1
# Fundamentos del QA y Mentalidad del Tester

## Unidad 1: Fundamentos Epistemológicos del QA

### Objetivo de la clase

Comprender los fundamentos del aseguramiento de la calidad, el rol del QA y desarrollar una mentalidad orientada a la identificación de riesgos y defectos.

---

## Contenido Teórico y Explicación

### 1. Calidad de Software

- ¿Qué es calidad?
- Calidad desde la perspectiva del usuario.
- Calidad desde la perspectiva del negocio.
- Calidad y cumplimiento de requisitos.
- Calidad y expectativas del usuario.
- ¿Software sin bugs significa software de calidad?

---

### 2. QA, QC y Testing

- Quality Assurance.
- Quality Control.
- Software Testing.
- Diferencias entre QA, QC y Testing.
- Prevención de defectos.
- Detección de defectos.

```text
QA
↓
Prevención

QC
↓
Control

Testing
↓
Detección
```

---

### 3. Rol del QA

- Responsabilidades principales.
- Participación durante el ciclo de desarrollo.
- Comunicación con Developers.
- Comunicación con Product Owner.
- QA como parte del equipo.
- QA más allá de encontrar bugs.

---

### 4. Psicología del Testing

- Mentalidad del tester.
- Pensamiento crítico.
- Curiosidad.
- Observación.
- Cuestionamiento de supuestos.
- Pensamiento orientado al riesgo.

### Sesgos comunes

- Confirmation Bias.
- Suposiciones incorrectas.
- Probar solamente caminos felices.
- Confiar demasiado en resultados previos.

---

### 5. Principios Fundamentales del Testing

Introducción a los principios:

1. El testing demuestra la presencia de defectos.
2. El testing exhaustivo es imposible.
3. Testing temprano.
4. Agrupación de defectos.
5. Paradoja del pesticida.
6. Testing depende del contexto.
7. Ausencia de errores no significa producto útil.

---

### 6. Niveles de Prueba

- Unit Testing.
- Integration Testing.
- System Testing.
- Acceptance Testing.

```text
Unit
  ↓
Integration
  ↓
System
  ↓
Acceptance
```

Se explicará principalmente:

- Objetivo.
- Alcance.
- Participantes.
- Tipo de problemas identificados.

---

### 7. Agile y Calidad

- Calidad en metodologías tradicionales.
- Calidad en Agile.
- Manifiesto Ágil y calidad.
- QA en equipos Agile.
- Scrum y QA.
- Participación temprana.
- Shift-Left Testing.

---

## Ejemplo Guiado

### Caso: Formulario de Login

```text
Email

Password

[ Iniciar Sesión ]
```

Analizar junto con los estudiantes:

- Escenarios positivos.
- Escenarios negativos.
- Datos inválidos.
- Casos inesperados.
- Riesgos.

Preguntas:

- ¿Qué esperamos que funcione?
- ¿Qué podría fallar?
- ¿Qué no estamos considerando?
- ¿Cómo intentaría fallar este formulario?

---

## Práctica Corta

Identificar:

> **3 escenarios de prueba para un formulario de Login.**

---

# CLASE 2
# Gestión de Requerimientos y STLC

## Unidad 2: Gestión de Requerimientos y STLC

### Objetivo de la clase

Analizar requerimientos desde la perspectiva de QA y comprender el ciclo de vida de las pruebas.

---

## Contenido Teórico y Explicación

### 1. Requerimientos de Software

- ¿Qué es un requerimiento?
- Importancia de los requerimientos.
- Requerimientos funcionales.
- Requerimientos no funcionales.

Ejemplo:

```text
Funcional

El usuario puede crear una tarea.
```

```text
No Funcional

El sistema debe responder
en menos de 2 segundos.
```

---

### 2. Características de un Buen Requerimiento

- Claro.
- Completo.
- Consistente.
- Verificable.
- Medible.
- Sin ambigüedades.

---

### 3. Historias de Usuario

Estructura:

```text
Como [usuario]

Quiero [acción]

Para [beneficio]
```

Componentes:

- Actor.
- Acción.
- Objetivo.
- Valor.

---

### 4. Criterios de Aceptación

- ¿Qué son?
- ¿Por qué son importantes?
- Criterios verificables.
- Casos positivos.
- Casos negativos.
- Reglas de negocio.

Introducción a:

```text
Given

When

Then
```

---

### 5. Análisis de Requerimientos desde QA

El QA debe identificar:

- Ambigüedades.
- Información faltante.
- Dependencias.
- Reglas de negocio.
- Casos excepcionales.
- Riesgos.
- Restricciones.

---

### 6. QA en Agile

Participación en:

- Refinement.
- Sprint Planning.
- Desarrollo.
- Testing.
- Sprint Review.
- Feedback.

---

### 7. STLC

## Software Testing Life Cycle

```text
Requirement Analysis
        ↓
Test Planning
        ↓
Test Design
        ↓
Test Environment
        ↓
Test Execution
        ↓
Test Closure
```

Explicar cada etapa:

### Requirement Analysis

¿Qué debemos probar?

### Test Planning

¿Cómo organizaremos las pruebas?

### Test Design

¿Qué pruebas realizaremos?

### Test Environment

¿Dónde realizaremos las pruebas?

### Test Execution

Ejecutar y registrar resultados.

### Test Closure

Analizar resultados y cerrar el ciclo.

---

## Ejemplo Guiado

### Historia de Usuario

> Como usuario, quiero crear una tarea para organizar mis actividades.

Analizar:

- ¿Qué información falta?
- ¿Qué reglas de negocio existen?
- ¿Qué preguntas debería realizar QA?
- ¿Qué criterios de aceptación necesitamos?

---

## Práctica Corta

Crear:

> **1 criterio de aceptación para una historia de usuario.**

---

# CLASE 3
# Diseño Técnico de Casos de Prueba e Introducción a la Automatización

## Unidad 3

### Objetivo de la clase

Comprender cómo diseñar casos de prueba mediante técnicas básicas y conocer qué tipo de pruebas pueden ser candidatas para automatización.

---

# Contenido Teórico y Explicación

## 1. Test Scenario

- ¿Qué es?
- Nivel general.
- Representa qué queremos probar.

Ejemplo:

```text
Verificar creación de usuario.
```

---

## 2. Test Case

- ¿Qué es?
- Nivel detallado.
- Pasos específicos.
- Datos.
- Resultado esperado.

---

## 3. Diferencia

```text
Test Scenario
      ↓
¿Qué probar?
```

```text
Test Case
      ↓
¿Cómo probar?
```

---

## 4. Estructura de un Test Case

- ID.
- Título.
- Precondiciones.
- Datos de prueba.
- Pasos.
- Resultado esperado.
- Resultado actual.
- Estado.

---

## 5. Técnicas de Caja Negra

Introducción a:

- Partición de equivalencia.
- Valores límite.
- Tablas de decisión.
- Transición de estados.

Se dará mayor énfasis a:

### Partición de Equivalencia

### Valores Límite

---

## 6. Partición de Equivalencia

Ejemplo:

```text
Edad permitida:

18 - 65
```

Particiones:

```text
Menor a 18
→ Inválido

18 - 65
→ Válido

Mayor a 65
→ Inválido
```

---

## 7. Valores Límite

```text
17
18
19

64
65
66
```

Explicar por qué los límites son importantes.

---

## 8. Tabla de Decisión

Introducción mediante reglas de negocio.

Ejemplo:

```text
Usuario activo
+
Contraseña correcta
=
Acceso permitido
```

---

## 9. Transición de Estados

Ejemplo:

```text
Pendiente
   ↓
En Progreso
   ↓
Completado
```

---

## 10. Introducción a Caja Blanca

Conceptualmente:

- Statement Coverage.
- Branch Coverage.

Sin profundizar en programación.

---

# 11. Introducción a la Automatización

### ¿Qué es automatización de pruebas?

Concepto general.

### Manual Testing

```text
Tester
↓
Ejecuta pasos
↓
Verifica resultado
```

### Automated Testing

```text
Script
↓
Ejecuta pasos
↓
Valida resultado
```

---

## 12. ¿Qué pruebas conviene automatizar?

Características:

- Repetitivas.
- Estables.
- Frecuentes.
- Basadas en reglas.
- Importantes para regresión.

---

## 13. ¿Qué pruebas no siempre conviene automatizar?

- Exploratorias.
- Usabilidad.
- Evaluaciones subjetivas.
- Casos que cambian constantemente.

---

## 14. Automatización como complemento

```text
Testing Manual

+

Testing Automatizado

=

Mejor estrategia de QA
```

Mención introductoria:

- Selenium.
- Cypress.
- Playwright.

**Sin profundizar en herramientas.**

---

## Ejemplo Guiado

### Caso

Edad permitida:

```text
18 - 65 años
```

Realizar:

- Partición de equivalencia.
- Valores límite.
- Algunos casos de prueba.

Después analizar:

> ¿Cuáles de estos casos serían buenos candidatos para automatización?

---

## Práctica Corta

Para una contraseña:

```text
Mínimo: 8 caracteres

Máximo: 20 caracteres
```

Identificar:

> **Valores límite principales.**

---

# CLASE 4
# Bug Tracking, Reporting y Pruebas de Regresión

## Unidad 4: Bug Tracking & Reporting

### Objetivo de la clase

Comprender el ciclo de vida de los defectos, documentarlos correctamente y conocer su relación con las pruebas de regresión.

---

# Contenido Teórico y Explicación

## 1. Conceptos

- Error.
- Defecto.
- Bug.
- Failure.

---

## 2. Expected vs Actual

```text
Expected Result

≠

Actual Result
```

Puede existir un defecto.

---

## 3. Identificación de Defectos

- Reproducibilidad.
- Evidencia.
- Información del ambiente.
- Pasos claros.
- Datos utilizados.

---

## 4. Bug Life Cycle

```text
NEW
 ↓
ASSIGNED
 ↓
IN PROGRESS
 ↓
FIXED
 ↓
RETEST
 ↓
CLOSED
```

Otros estados:

- Reopened.
- Rejected.
- Duplicate.
- Deferred.

---

## 5. Bug Report

Componentes:

- ID.
- Title.
- Environment.
- Preconditions.
- Steps to Reproduce.
- Test Data.
- Expected Result.
- Actual Result.
- Evidence.

---

## 6. Severity

Impacto técnico.

- Critical.
- High.
- Medium.
- Low.

---

## 7. Priority

Urgencia de solución.

- High.
- Medium.
- Low.

---

## 8. Severity vs Priority

Analizar diferentes casos.

---

# 9. Buenas Prácticas

- Título claro.
- Pasos reproducibles.
- Evidencia.
- Información objetiva.
- Un problema por reporte.
- Evitar opiniones.

---

# 10. Pruebas de Regresión

### ¿Qué es Regression Testing?

Verificar que los cambios no hayan afectado funcionalidades existentes.

---

### Retest vs Regression

#### Retest

```text
Bug corregido
↓
Volver a probar el mismo bug
```

#### Regression

```text
Cambio realizado
↓
Verificar otras funcionalidades
```

---

## 11. Relación con Automatización

Las pruebas de regresión suelen ser buenas candidatas para automatización porque son:

- Repetitivas.
- Frecuentes.
- Importantes.
- Ejecutadas después de cambios.

---

## Ejemplo Guiado

Caso:

> El sistema permite crear una tarea sin título.

Crear:

- Title.
- Steps.
- Expected Result.
- Actual Result.
- Severity.
- Priority.

Después preguntar:

> ¿Esta prueba debería formar parte de una suite de regresión?

---

## Práctica Corta

Definir:

> Expected Result y Actual Result.

Para un escenario con un defecto.

---

# CLASE 5
# API Testing con Postman y Ejemplo de Automatización

## Unidad 5: API Testing con Postman

### Objetivo de la clase

Comprender los fundamentos de las APIs, realizar validaciones básicas con Postman y observar ejemplos simples de automatización.

---

# Contenido Teórico y Explicación

## 1. ¿Qué es una API?

- Comunicación entre aplicaciones.
- Cliente.
- Servidor.
- Backend.
- API REST.

---

## 2. Endpoints

Ejemplo:

```text
/api/users
```

---

## 3. Métodos HTTP

### GET

Obtener información.

### POST

Crear información.

### PUT

Actualizar completamente.

### PATCH

Actualizar parcialmente.

### DELETE

Eliminar información.

---

## 4. Request

Componentes:

- URL.
- Method.
- Headers.
- Parameters.
- Body.

---

## 5. Response

- Status Code.
- Headers.
- Body.
- JSON.

---

## 6. HTTP Status Codes

Principales:

```text
200 OK

201 Created

400 Bad Request

401 Unauthorized

403 Forbidden

404 Not Found

500 Internal Server Error
```

---

# 7. Introducción a Postman

- Interface.
- Requests.
- Collections.
- Environments.
- Variables.

---

# 8. Validaciones de API

Validar:

- Status Code.
- Response Body.
- Campos.
- Tipos de datos.
- Datos esperados.
- Errores.

---

# 9. Scripts Básicos

Introducción a JavaScript en Postman.

Ejemplo:

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

Conceptos:

- `pm.test`.
- `pm.response`.
- Assertions.

---

# 10. Automatización Básica

Explicar el flujo:

```text
Prueba Manual

↓

Validación

↓

Script

↓

Ejecución Repetible
```

La automatización se presenta como concepto.

No se profundiza en:

- Frameworks.
- Arquitectura.
- Patrones.
- Programación avanzada.

---

# 11. Ejemplo Breve con Selenium

Mostrar conceptualmente una prueba automatizada:

```text
1. Abrir navegador

2. Ir a Login

3. Buscar campo Email

4. Ingresar datos

5. Presionar botón

6. Verificar resultado
```

Se puede mostrar un código muy corto únicamente como demostración.

Objetivo:

> Que el estudiante vea cómo un caso manual puede convertirse en una prueba automatizada.

### No se desarrollará:

- Framework.
- Page Object Model.
- Configuración avanzada.
- Suite completa.
- Selenium en profundidad.

---

## Ejemplo Guiado

Realizar:

```text
GET /users
```

Analizar:

- Request.
- Response.
- Status Code.
- JSON.
- Datos.

Agregar una validación simple.

Después mostrar rápidamente:

> Un caso de Login manual y su equivalente conceptual en Selenium.

---

## Práctica Corta

Identificar en una respuesta:

- Status Code.
- Campo principal.
- Resultado esperado.

---

# CLASE 6
# Usabilidad, Accesibilidad y Test Plan Management

---

# Unidad 6
# Pruebas de Usabilidad y Accesibilidad

## Objetivo

Comprender aspectos básicos de experiencia de usuario y accesibilidad como parte de la calidad del software.

---

# Contenido Teórico y Explicación

## 1. UX

- ¿Qué es UX?
- Experiencia del usuario.
- Funcionalidad vs experiencia.

---

## 2. Usabilidad

Características:

- Facilidad de aprendizaje.
- Eficiencia.
- Consistencia.
- Prevención de errores.
- Feedback.
- Navegación.

---

## 3. QA y Perspectiva del Usuario

Preguntas:

- ¿Se entiende?
- ¿Es fácil de utilizar?
- ¿El usuario sabe qué hacer?
- ¿Existen mensajes claros?
- ¿Se previenen errores?

---

# 4. Accesibilidad

- ¿Qué es?
- Importancia.
- Accesibilidad como parte de la calidad.

---

# 5. WCAG

Introducción.

## Principios POUR

### Perceivable

La información debe poder percibirse.

### Operable

La interfaz debe poder utilizarse.

### Understandable

Debe ser comprensible.

### Robust

Debe funcionar correctamente con diferentes tecnologías.

---

# 6. Aspectos Básicos

- Contraste.
- Navegación por teclado.
- Labels.
- Texto alternativo.
- Mensajes de error.
- Tamaño y claridad.
- Estructura.

---

## Ejemplo Guiado

Evaluar una interfaz considerando:

- Claridad.
- Navegación.
- Feedback.
- Mensajes.
- Contraste.
- Accesibilidad.

---

## Práctica Corta

Identificar:

> **1 problema de accesibilidad o usabilidad.**

---

# Unidad 7
# Test Plan Management

## Objetivo

Comprender la importancia de la planificación y los principales elementos de un Test Plan.

---

# Contenido Teórico y Explicación

## 1. ¿Qué es un Test Plan?

- Propósito.
- Importancia.
- Organización de las pruebas.

---

## 2. ISO/IEC/IEEE 29119

Introducción:

- ¿Qué es?
- ¿Por qué existen estándares?
- Relación con Testing.

No se estudiará el estándar completo.

---

## 3. Master Test Plan

Componentes principales:

### Introduction

Descripción general.

### Objectives

¿Qué queremos validar?

### Scope

¿Qué está incluido?

### Out of Scope

¿Qué no está incluido?

### Test Strategy

¿Cómo se realizarán las pruebas?

### Resources

¿Quién participa?

### Test Environment

¿Dónde se prueba?

### Risks

¿Qué puede afectar las pruebas?

### Entry Criteria

¿Cuándo pueden comenzar?

### Exit Criteria

¿Cuándo pueden finalizar?

---

# 4. Estrategia de Pruebas

Definir:

- Tipos de prueba.
- Alcance.
- Recursos.
- Ambiente.
- Riesgos.

---

# 5. Riesgos

Ejemplos:

- Cambios de requerimientos.
- Ambiente no disponible.
- Datos incompletos.
- Falta de tiempo.
- Dependencias externas.

---

# 6. Entry y Exit Criteria

### Entry Criteria

Condiciones para iniciar pruebas.

### Exit Criteria

Condiciones para finalizar pruebas.

---

## Ejemplo Guiado

Crear un Mini Test Plan.

```text
Sistema:
TaskFlow

Objetivo:
Validar funcionalidades principales.

Alcance:
Login y gestión de tareas.

Tipos:
Functional Testing
API Testing
Usability Testing

Riesgo:
Cambios de requerimientos.

Criterio de salida:
No existen defectos críticos abiertos.
```

---

## Práctica Corta

Identificar:

> **1 riesgo del proyecto y una posible acción de mitigación.**

---

# 4. Integración de Automatización en el Módulo

La automatización se integrará de manera progresiva.

| Unidad | Contenido relacionado |
|---|---|
| Unidad 3 | Qué es automatización y qué pruebas automatizar |
| Unidad 4 | Regresión y pruebas candidatas para automatización |
| Unidad 5 | Validaciones automatizadas de API y ejemplo breve con Selenium |

---

# Progresión

```text
UNIDAD 3

¿Qué es automatización?

↓

¿Qué pruebas automatizar?

↓

UNIDAD 4

¿Qué pruebas repetimos?

↓

¿Qué es regresión?

↓

UNIDAD 5

¿Cómo se ve una prueba automatizada?

↓

Postman + Validación

+

Ejemplo breve Selenium
```

---

# 5. Resumen de Contenidos

| Unidad | Contenido |
|---|---|
| Unidad 1 | Calidad, QA, QC, Testing, psicología, principios, niveles y Agile |
| Unidad 2 | Requerimientos, historias de usuario, criterios de aceptación y STLC |
| Unidad 3 | Test Cases, caja negra, caja blanca, equivalencia, valores límite y automatización |
| Unidad 4 | Bugs, ciclo de vida, reportes, severidad, prioridad y regresión |
| Unidad 5 | APIs, HTTP, Postman, validaciones, scripts y ejemplo de automatización |
| Unidad 6 | UX, usabilidad, accesibilidad y WCAG |
| Unidad 7 | Test Plan, estrategia, riesgos y criterios de entrada/salida |

---

# 6. Alcance de la Automatización

La automatización tendrá un enfoque introductorio.

## Se abordará

- Concepto de automatización.
- Pruebas manuales vs automatizadas.
- Criterios para automatizar.
- Regresión.
- Automatización de validaciones simples.
- Ejemplo breve con Selenium.
- Mención de Cypress y Playwright.

---

## No se abordará en profundidad

- Framework de automatización.
- Arquitectura de pruebas.
- Page Object Model.
- Programación avanzada.
- Selenium avanzado.
- Cypress avanzado.
- Playwright avanzado.
- Integración CI/CD.
- Desarrollo de una suite completa.

---

# 7. Secuencia General del Módulo

```text
FUNDAMENTOS QA
       ↓
REQUERIMIENTOS
       ↓
DISEÑO DE PRUEBAS
       ↓
AUTOMATIZACIÓN
       ↓
DEFECTOS
       ↓
REGRESIÓN
       ↓
API TESTING
       ↓
EJEMPLO DE AUTOMATIZACIÓN
       ↓
USABILIDAD
       ↓
ACCESIBILIDAD
       ↓
TEST PLAN
```

---

# 8. Resultado Esperado

Al finalizar el módulo, el estudiante será capaz de:

1. Comprender el rol del QA dentro de un proyecto de software.
2. Diferenciar QA, QC y Testing.
3. Aplicar principios fundamentales de testing.
4. Analizar requerimientos e historias de usuario.
5. Identificar criterios de aceptación.
6. Comprender el ciclo STLC.
7. Diseñar escenarios y casos de prueba.
8. Aplicar partición de equivalencia y valores límite.
9. Comprender cuándo una prueba puede ser candidata para automatización.
10. Identificar y reportar defectos correctamente.
11. Diferenciar severidad y prioridad.
12. Comprender las pruebas de regresión.
13. Realizar validaciones básicas de APIs.
14. Comprender el uso de Postman para pruebas.
15. Observar ejemplos básicos de automatización.
16. Identificar problemas de usabilidad.
17. Comprender fundamentos de accesibilidad y WCAG.
18. Comprender la estructura de un Test Plan.
19. Identificar riesgos y criterios de entrada y salida.