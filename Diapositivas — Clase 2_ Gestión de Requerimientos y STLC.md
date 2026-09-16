# CLASE 2

## Gestión de Requerimientos y STLC

**QA Manual – Pruebas de Software**

---

## Diapositiva 1 — Título

# Gestión de Requerimientos y STLC

### De los requerimientos a las pruebas

**QA Manual – Clase 2**

---

## Diapositiva 2 — Objetivos de la clase

Al finalizar la clase podrás:

- Comprender qué es un requerimiento.
- Diferenciar requerimientos funcionales y no funcionales.
- Identificar reglas de negocio.
- Comprender los criterios de aceptación.
- Detectar requerimientos ambiguos o incompletos.
- Analizar requerimientos desde la perspectiva de QA.
- Conocer las fases del **STLC**.
- Relacionar requerimientos con escenarios y casos de prueba.

---

# 1. Repaso de la Clase 1

## Diapositiva 3 — Recordemos

### ¿Qué vimos en la clase anterior?

- ¿Qué es QA?
- ¿Qué es Testing?
- ¿Qué es un requerimiento?
- ¿Qué es un error o defecto?
- ¿Qué es un escenario?
- Mentalidad de QA
- Riesgo y estrategia de pruebas

### Pregunta

> ¿Qué puede ocurrir si un requerimiento está mal definido?

---

## Diapositiva 4 — De un requerimiento a una prueba

```text
REQUERIMIENTO
      ↓
¿QUÉ DEBEMOS VALIDAR?
      ↓
ESCENARIOS
      ↓
CASOS DE PRUEBA
      ↓
EJECUCIÓN
      ↓
RESULTADO
```

### Idea clave

**La calidad de las pruebas depende en gran medida de qué tan bien entendemos el requerimiento.**

---

# 2. ¿Qué es un requerimiento?

## Diapositiva 5 — Definición

### ¿Qué es un requerimiento?

Un requerimiento describe una:

- Necesidad
- Condición
- Regla
- Funcionalidad
- Restricción

que el sistema debe cumplir.

### Ejemplo

> "El sistema debe permitir registrar nuevos usuarios."

---

## Diapositiva 6 — ¿Es suficiente?

> "El sistema debe permitir registrar nuevos usuarios."

### Preguntas de QA

- ¿Qué datos debe ingresar?
- ¿Qué campos son obligatorios?
- ¿Qué formatos son válidos?
- ¿Se pueden registrar datos duplicados?
- ¿Qué ocurre si falta información?
- ¿Qué reglas debe cumplir la contraseña?
- ¿Qué mensaje se muestra al finalizar?

### 💡 QA busca entender qué debe validarse.

---

# 3. ¿Por qué son importantes?

## Diapositiva 7 — Importancia de los requerimientos

Un requerimiento bien definido permite:

- Comprender el comportamiento esperado.
- Diseñar mejores pruebas.
- Reducir dudas durante el desarrollo.
- Detectar problemas antes de programar.
- Reducir retrabajo.
- Facilitar la comunicación entre equipos.

### Recuerda

> **Un problema en el requerimiento puede convertirse posteriormente en un problema del sistema.**

---

# 4. Tipos de requerimientos

## Diapositiva 8 — Requerimientos funcionales

### ¿Qué debe hacer el sistema?

Describen las **funcionalidades o comportamientos** del sistema.

### Ejemplos

- Registrar usuarios.
- Iniciar sesión.
- Crear productos.
- Generar reportes.
- Realizar una transferencia.
- Enviar una notificación.

### Pregunta

> ¿Qué acción debe realizar el sistema?

---

## Diapositiva 9 — Requerimientos no funcionales

### ¿Cómo debe funcionar el sistema?

Definen características, restricciones o condiciones.

### Ejemplos

- Rendimiento
- Seguridad
- Disponibilidad
- Usabilidad
- Compatibilidad

### Ejemplo

> "El sistema debe mostrar los resultados de búsqueda en menos de 3 segundos."

---

## Diapositiva 10 — Funcional vs. no funcional

| Funcional              | No funcional                     |
| ---------------------- | -------------------------------- |
| Qué hace               | Cómo debe funcionar              |
| Registrar usuario      | Responder en menos de 3 segundos |
| Generar reporte        | Estar disponible 99.9%           |
| Realizar transferencia | Proteger los datos               |

### Pregunta

> ¿Qué tipo de requerimiento es:\
> "El sistema debe permitir cambiar la contraseña"?

---

# 5. Requerimiento y regla de negocio

## Diapositiva 11 — ¿Qué es una regla de negocio?

Una **regla de negocio** define una condición que debe cumplirse de acuerdo con las reglas de la organización.

### Ejemplo

**Requerimiento**

> El sistema debe permitir registrar clientes.

**Regla de negocio**

> No se puede registrar un cliente si ya existe otro con el mismo número de documento.

---

## Diapositiva 12 — ¿Qué debe hacer QA?

QA debe identificar:

- Reglas que deben cumplirse.
- Condiciones permitidas.
- Condiciones no permitidas.
- Restricciones.
- Excepciones.

### Ejemplo

> "Un usuario no puede transferir un monto superior a su saldo disponible."

### Pregunta

**¿Cómo comprobaríamos esta regla?**

---

# 6. Criterios de aceptación

## Diapositiva 13 — ¿Qué son?

Los **criterios de aceptación** son condiciones que permiten determinar si una funcionalidad cumple con lo esperado.

### En otras palabras:

> ¿Qué debe cumplirse para considerar que la funcionalidad está correctamente implementada?

---

## Diapositiva 14 — Ejemplo: Registro de usuarios

### Funcionalidad

> Registrar un usuario.

### Criterios de aceptación

- El nombre es obligatorio.
- El correo es obligatorio.
- El correo debe tener un formato válido.
- El correo no debe estar registrado.
- La contraseña debe cumplir las reglas definidas.
- Debe mostrarse una confirmación al registrarse correctamente.

---

# 7. ¿Cómo debe ser un buen requerimiento?

## Diapositiva 15 — Características

Un buen requerimiento debe ser:

- **Claro**
- **Específico**
- **Completo**
- **Consistente**
- **Medible**
- **Verificable**

### Pregunta

> ¿Podemos diseñar una prueba para comprobarlo?

Si la respuesta es **no**, probablemente necesitamos más información.

---

## Diapositiva 16 — Requerimiento ambiguo

### ❌ Ejemplo

> "El sistema debe ser rápido y sencillo."

### Problemas

¿Qué significa:

- ¿Rápido?
- ¿Cuánto tiempo?
- ¿Sencillo para quién?
- ¿Qué operación?
- ¿En qué condiciones?

### QA debe pedir aclaraciones.

---

## Diapositiva 17 — De ambiguo a verificable

### ❌ Antes

> "El sistema debe ser rápido."

### ✅ Después

> "El sistema debe mostrar los resultados de búsqueda en menos de 3 segundos."

Ahora podemos preguntar:

> **¿Cómo lo verificamos?**

---

# 8. Requerimientos incompletos

## Diapositiva 18 — ¿Qué información falta?

### Requerimiento

> "El sistema debe permitir registrar usuarios de forma rápida y sencilla."

### QA debería preguntar:

- ¿Qué datos debe ingresar el usuario?
- ¿Cuáles son obligatorios?
- ¿Qué formatos son válidos?
- ¿Se permiten usuarios duplicados?
- ¿Qué reglas tiene la contraseña?
- ¿Qué ocurre si falta información?
- ¿Qué mensaje se muestra al finalizar?

### ⚠️ Importante

> **QA no debe inventar las respuestas.**

Debe solicitar aclaraciones.

---

# 9. Análisis de requerimientos desde QA

## Diapositiva 19 — ¿Qué hace QA con un requerimiento?

QA debe:

1. Comprender el requerimiento.
2. Identificar reglas de negocio.
3. Revisar criterios de aceptación.
4. Detectar ambigüedades.
5. Identificar información faltante.
6. Pensar en escenarios.
7. Identificar riesgos.
8. Solicitar aclaraciones.
9. Determinar qué debe validarse.

---

## Diapositiva 20 — La pregunta principal de QA

Al analizar un requerimiento, QA debe preguntarse:

> **¿Qué puede ocurrir y qué debemos comprobar?**

No buscamos solamente:

> "¿Funciona?"

También buscamos:

- ¿Qué pasa si los datos son incorrectos?
- ¿Qué pasa si falta información?
- ¿Qué pasa si se viola una regla?
- ¿Qué pasa en situaciones inesperadas?

---

# 10. Ejemplo guiado

## Diapositiva 21 — Registro de usuarios

### Requerimiento inicial

> "El sistema debe permitir registrar usuarios de forma rápida y sencilla."

### Pregunta

**¿Es suficiente para comenzar las pruebas?**

❌ No.

### ¿Por qué?

Falta información sobre:

- Datos
- Validaciones
- Reglas
- Restricciones
- Resultado esperado

---

## Diapositiva 22 — Requerimiento mejor definido

### Registro de usuario

> "El sistema debe permitir registrar un usuario proporcionando nombre, correo electrónico y contraseña."

### Reglas

1. Todos los campos son obligatorios.
2. El correo debe tener formato válido.
3. El correo no debe estar registrado.
4. La contraseña debe cumplir las reglas definidas.

---

## Diapositiva 23 — Criterios de aceptación

La funcionalidad debe:

- Permitir registrar datos válidos.
- Rechazar campos obligatorios vacíos.
- Rechazar correos inválidos.
- Rechazar correos ya registrados.
- Validar la contraseña.
- Mostrar confirmación cuando el registro sea exitoso.

---

## Diapositiva 24 — ¿Qué escenarios podemos identificar?

### Escenarios

1. Registro con datos válidos.
2. Nombre vacío.
3. Correo vacío.
4. Contraseña vacía.
5. Correo con formato inválido.
6. Correo ya registrado.
7. Contraseña inválida. 

### Importante

Hoy **identificamos escenarios**.

En la siguiente clase aprenderemos a convertirlos en **casos de prueba detallados**.

---

# 11. STLC

## Diapositiva 25 — ¿Qué es STLC?

# STLC

**Software Testing Life Cycle**

### Ciclo de Vida de las Pruebas de Software

Es un conjunto de fases que permiten organizar y ejecutar el proceso de pruebas.

---

## Diapositiva 26 — Fases del STLC

```text
1. Requirement Analysis
   Análisis de requisitos
            ↓
2. Test Planning
   Planificación de pruebas
            ↓
3. Test Case Development
   Diseño de casos de prueba
            ↓
4. Test Environment Setup
   Preparación del entorno
            ↓
5. Test Execution
   Ejecución de pruebas
            ↓
6. Test Closure
   Cierre de pruebas
```

---

## Diapositiva 27 — 1. Requirement Analysis

### Análisis de requisitos

QA:

- Revisa los requerimientos.
- Comprende la funcionalidad.
- Identifica reglas de negocio.
- Revisa criterios de aceptación.
- Detecta ambigüedades.
- Identifica riesgos.
- Determina qué debe probarse.

### Aquí comienza el trabajo de QA.

---

## Diapositiva 28 — 2. Test Planning

### Planificación de pruebas

Se define:

- Alcance.
- Tipos de pruebas.
- Recursos.
- Responsabilidades.
- Entorno.
- Datos de prueba.
- Riesgos.
- Cronograma.

### Pregunta

> ¿Qué necesitamos para poder probar?

---

## Diapositiva 29 — 3. Test Case Development

### Diseño / desarrollo de casos de prueba

A partir de los escenarios se construyen los casos de prueba.

```text
ESCENARIO
   ↓
CASO DE PRUEBA
   ↓
Precondiciones
Datos
Pasos
Resultado esperado
```

### 📌 Se profundizará en la siguiente clase.

---

## Diapositiva 30 — 4. Test Environment Setup

### Preparación del entorno

Se prepara lo necesario para ejecutar las pruebas:

- Aplicación.
- Base de datos.
- Configuración.
- Usuarios.
- Datos de prueba.
- Navegadores.
- Dispositivos.

### Objetivo

> Tener un entorno adecuado para ejecutar las pruebas.

---

## Diapositiva 31 — 5. Test Execution

### Ejecución de pruebas

```text
Caso de prueba
      ↓
Ejecutar
      ↓
Resultado actual
      ↓
Comparar
      ↓
PASS / FAIL
```

Si el resultado actual no coincide con el esperado:

> **Puede existir un defecto.**

---

## Diapositiva 32 — 6. Test Closure

### Cierre de pruebas

Se revisan:

- Casos ejecutados.
- Casos aprobados.
- Casos fallidos.
- Defectos encontrados.
- Defectos pendientes.
- Riesgos.
- Resultados de las pruebas.

### Objetivo

Documentar y comunicar el resultado del ciclo de pruebas.

---

# 12. Requerimientos + STLC

## Diapositiva 33 — ¿Cómo se relacionan?

```text
REQUERIMIENTO
      ↓
ANÁLISIS DE QA
      ↓
REGLAS / CRITERIOS
      ↓
ESCENARIOS
      ↓
CASOS DE PRUEBA
      ↓
EJECUCIÓN
      ↓
RESULTADOS
      ↓
DEFECTOS
```

### Idea clave

> **QA no empieza cuando ejecuta una prueba.**

QA comienza desde el análisis del requerimiento.

---

# 13. Práctica

## Diapositiva 34 — Ejercicio

### Sistema: Registro de usuarios

**Requerimiento:**

> "El sistema debe permitir registrar un usuario proporcionando nombre, correo electrónico y contraseña."

### Reglas

- Todos los campos son obligatorios.
- El correo debe tener formato válido.
- El correo no debe estar registrado.
- La contraseña debe cumplir las reglas definidas.

---

## Diapositiva 35 — Actividad 1

### Analizar el requerimiento

Identifica:

**2 preguntas**

¿Qué información adicional necesitamos?

**2 riesgos**

¿Qué podría salir mal?

---

## Diapositiva 36 — Actividad 2

### Identificar escenarios

Crea **5 escenarios de prueba** para el registro de usuarios.

Ejemplo:

> Registro con datos válidos.

Ahora identifica otros cuatro.

---

## Diapositiva 37 — Actividad 3

### Crear un caso de prueba

Selecciona uno de tus escenarios.

Define:

- ID
- Título
- Precondiciones
- Datos de prueba
- Pasos
- Resultado esperado

### No buscamos perfección.

Buscamos entender:

**Requerimiento → Escenario → Caso de prueba**

---

# 14. Cierre

## Diapositiva 38 — ¿Qué aprendimos?

Hoy aprendimos:

- Qué es un requerimiento.
- Tipos de requerimientos.
- Reglas de negocio.
- Criterios de aceptación.
- Requerimientos ambiguos e incompletos.
- Análisis de requerimientos desde QA.
- STLC y sus fases.
- Relación entre requerimientos y pruebas.

---

## Diapositiva 39 — Concepto clave

# QA empieza antes de probar

Primero debemos:

**Entender → Analizar → Preguntar → Identificar riesgos → Diseñar → Ejecutar**

---

## Diapositiva 40 — Próxima clase

# Clase 3

## Escenarios y Casos de Prueba

Aprenderemos:

- ¿Qué es un escenario?
- ¿Qué es un caso de prueba?
- Diferencias entre ambos.
- Estructura de un caso de prueba.
- Precondiciones.
- Datos de prueba.
- Pasos.
- Resultado esperado.
- Pruebas positivas y negativas.
- Ejercicios prácticos.

### De los requerimientos a casos de prueba detallados.
