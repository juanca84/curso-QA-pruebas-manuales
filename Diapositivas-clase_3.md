# CLASE 3

## Diseño de casos de prueba

### e introducción a la automatización

**Duración:** 2 h 15 min

---

# DIAPOSITIVA 1 — PORTADA

# Diseño de casos de prueba

### e introducción a la automatización

**QA — Aseguramiento de la Calidad y Pruebas Manuales**

---

# DIAPOSITIVA 2 — ¿QUÉ VAMOS A APRENDER?

* Diseñar casos de prueba
* Transformar requisitos en pruebas
* Diseñar escenarios positivos y negativos
* Definir datos de prueba
* Validar límites
* Definir resultados esperados
* Revisar la calidad de un caso
* Introducción a la automatización

---

# DIAPOSITIVA 3 — LA PREGUNTA CENTRAL

# ¿Qué debemos probar?

No comenzar por los pasos.

Primero debemos entender:

```text
¿Qué comportamiento
quiero validar?
```

---

# DIAPOSITIVA 4 — DEL REQUISITO A LA PRUEBA

```text
REQUISITO
    ↓
REGLAS
    ↓
CONDICIONES
    ↓
ESCENARIOS
    ↓
CASOS DE PRUEBA
    ↓
DATOS
    ↓
EJECUCIÓN
    ↓
RESULTADO
```

---

# DIAPOSITIVA 5 — ¿QUÉ ES UN CASO DE PRUEBA?

> Un caso de prueba define cómo comprobar una condición específica del sistema.

Incluye:

```text
Qué validar
+
Con qué datos
+
Qué acciones realizar
+
Qué resultado esperar
```

---

# DIAPOSITIVA 6 — NO ES SOLO UNA LISTA DE PASOS

### ❌ Solo pasos

```text
1. Abrir login
2. Escribir correo
3. Escribir contraseña
4. Presionar botón
```

### ¿Qué falta?

* ¿Qué estamos validando?
* ¿Qué datos utilizamos?
* ¿Qué esperamos?
* ¿Cómo sabemos si pasó?

---

# DIAPOSITIVA 7 — UN CASO DE PRUEBA

```text
OBJETIVO
    +
CONDICIÓN
    +
DATOS
    +
ACCIONES
    +
RESULTADO ESPERADO
```

---

# DIAPOSITIVA 8 — ESTRUCTURA

## Caso de prueba

```text
ID

Título

Precondiciones

Datos de prueba

Pasos

Resultado esperado
```

---

# DIAPOSITIVA 9 — ID Y TÍTULO

### ID

Identifica el caso.

```text
TC-LOGIN-001
```

### Título

Describe qué se valida.

❌ Probar login

✅ Iniciar sesión con credenciales válidas

---

# DIAPOSITIVA 10 — PRECONDICIONES

Condiciones necesarias antes de ejecutar la prueba.

### Ejemplo

```text
- Usuario registrado
- Usuario activo
- Sistema disponible
```

---

# DIAPOSITIVA 11 — DATOS DE PRUEBA

Valores utilizados durante la prueba.

### Ejemplo

```text
Correo:
usuario@test.com

Contraseña:
Test1234
```

Los datos también forman parte del diseño de la prueba.

---

# DIAPOSITIVA 12 — PASOS

Los pasos describen las acciones necesarias.

Deben ser:

* Claros
* Ordenados
* Reproducibles

### Ejemplo

```text
1. Abrir la pantalla de login.
2. Ingresar el correo.
3. Ingresar la contraseña.
4. Presionar "Iniciar sesión".
```

---

# DIAPOSITIVA 13 — RESULTADO ESPERADO

Describe lo que debe ocurrir.

### ❌ Poco claro

```text
El sistema funciona correctamente.
```

### ✅ Verificable

```text
El sistema permite el acceso
y muestra la página principal.
```

---

# DIAPOSITIVA 14 — ¿PASS O FAIL?

El resultado esperado debe permitir determinar claramente:

```text
        EJECUCIÓN
            ↓
     ¿Qué ocurrió?
            ↓
¿Coincide con lo esperado?
       ↙          ↘
     SÍ            NO
     ↓              ↓
   PASS            FAIL
```

---

# DIAPOSITIVA 15 — DEL REQUISITO AL CASO

## Ejemplo

> El sistema debe permitir registrar un usuario utilizando nombre, correo electrónico y contraseña.

### Antes de crear casos:

**¿Qué debemos analizar?**

* Condiciones
* Reglas
* Situaciones posibles

---

# DIAPOSITIVA 16 — REGLAS DEL EJEMPLO

### Registro de usuario

```text
R1. Nombre obligatorio

R2. Correo obligatorio

R3. Contraseña obligatoria

R4. Correo con formato válido

R5. Correo no registrado previamente
```

---

# DIAPOSITIVA 17 — PENSAR EN ESCENARIOS

### ¿Qué podría ocurrir?

```text
✓ Datos válidos

✕ Nombre vacío

✕ Correo vacío

✕ Contraseña vacía

✕ Correo inválido

✕ Correo ya registrado
```

---

# DIAPOSITIVA 18 — ESCENARIO → CASO

### Escenario

```text
Registrar usuario con correo inválido
```

### Caso de prueba

```text
Datos:
correo = juan@

Acción:
Intentar registrar

Resultado esperado:
El sistema rechaza el correo
y muestra un mensaje de validación.
```

---

# DIAPOSITIVA 19 — CASOS POSITIVOS

Validan condiciones válidas.

### Ejemplo

```text
Nombre     → válido
Correo     → válido
Contraseña → válida

             ↓

      Registro exitoso
```

---

# DIAPOSITIVA 20 — CASOS NEGATIVOS

Validan condiciones inválidas o no permitidas.

### Ejemplo

```text
Correo inválido
       ↓
Intentar registrar
       ↓
Sistema rechaza
       ↓
Mensaje de validación
```

---

# DIAPOSITIVA 21 — CASO NEGATIVO ≠ PRUEBA FALLIDA

### Una prueba negativa puede terminar en:

# PASS

si el sistema responde correctamente ante una condición inválida.

```text
Dato inválido
      ↓
Sistema rechaza correctamente
      ↓
PASS
```

---

# DIAPOSITIVA 22 — DATOS DE PRUEBA

Los datos determinan qué condición estamos validando.

### Ejemplo

> La contraseña debe tener entre 8 y 20 caracteres.

```text
7       ❌
8       ✓
9       ✓
...
19      ✓
20      ✓
21      ❌
```

---

# DIAPOSITIVA 23 — PRUEBAS DE LÍMITE

```text
          VÁLIDO
     ┌──────────────┐
     8              20
     ●──────────────●
    7                21
    ❌                ❌
```

Los límites ayudan a validar restricciones.

---

# DIAPOSITIVA 24 — ¿CUÁNTOS CASOS NECESITAMOS?

No se trata de crear la mayor cantidad posible.

Debemos buscar:

```text
REQUISITOS
    +
REGLAS
    +
RIESGO
    +
COBERTURA
```

---

# DIAPOSITIVA 25 — EVITAR DOS EXTREMOS

### Muy pocos casos

```text
Poca cobertura
```

### Demasiados casos redundantes

```text
Mayor esfuerzo
sin aportar nueva cobertura
```

### Objetivo

```text
Casos relevantes
y suficientes
```

---

# DIAPOSITIVA 26 — CALIDAD DEL CASO DE PRUEBA

Antes de ejecutar:

```text
¿Está relacionado con un requisito?

¿Tiene un objetivo claro?

¿Tiene datos definidos?

¿Los pasos son reproducibles?

¿El resultado es verificable?

¿Aporta cobertura?
```

---

# DIAPOSITIVA 27 — EJEMPLO GUIADO

# Cambio de contraseña

> El sistema permite cambiar la contraseña.

> La nueva contraseña debe tener entre 8 y 20 caracteres.

> La nueva contraseña y su confirmación deben coincidir.

---

# DIAPOSITIVA 28 — ANALIZAR ANTES DE PROBAR

### Reglas

```text
Mínimo: 8 caracteres

Máximo: 20 caracteres

Confirmación:
debe coincidir
```

### ¿Qué debemos probar?

---

# DIAPOSITIVA 29 — ESCENARIOS

```text
E1. Contraseña válida

E2. Menos de 8 caracteres

E3. Exactamente 8 caracteres

E4. Exactamente 20 caracteres

E5. Más de 20 caracteres

E6. Confirmación diferente
```

---

# DIAPOSITIVA 30 — CASO DE PRUEBA

## TC-PASS-001

### Cambiar contraseña con datos válidos

**Precondición**

```text
Usuario autenticado
```

**Datos**

```text
Nueva contraseña: Password123
Confirmación: Password123
```

---

# DIAPOSITIVA 31 — CASO DE PRUEBA

## TC-PASS-001

### Pasos

```text
1. Abrir cambio de contraseña.
2. Ingresar nueva contraseña.
3. Ingresar confirmación.
4. Guardar cambios.
```

### Resultado esperado

```text
El sistema permite cambiar la contraseña
y muestra un mensaje de confirmación.
```

---

# DIAPOSITIVA 32 — CASO NEGATIVO

## TC-PASS-002

### Menos de 8 caracteres

**Datos**

```text
Nueva contraseña: Test123
Confirmación: Test123
```

### Resultado esperado

```text
El sistema no permite cambiar la contraseña
y muestra un mensaje de validación.
```

---

# DIAPOSITIVA 33 — CASO DE LÍMITE

## TC-PASS-003

### Exactamente 8 caracteres

```text
12345678
```

### Resultado esperado

```text
El sistema acepta la contraseña
porque cumple con la longitud mínima.
```

---

# DIAPOSITIVA 34 — OTRO CASO DE LÍMITE

## TC-PASS-004

### Exactamente 20 caracteres

```text
12345678901234567890
```

### Resultado esperado

```text
El sistema acepta la contraseña
porque cumple con la longitud máxima.
```

---

# DIAPOSITIVA 35 — PREGUNTAS DE QA

Durante el diseño de un caso:

```text
¿Qué estoy validando?

¿Qué requisito estoy cubriendo?

¿Qué regla estoy validando?

¿Qué puede salir mal?

¿Qué datos necesito?

¿Qué debería ocurrir?

¿Cómo sé si pasó?
```

---

# DIAPOSITIVA 36 — PRÁCTICA

## Diseñar 2 casos de prueba

### Requisito

> El sistema permite registrar un usuario. El nombre y correo son obligatorios. El correo debe tener un formato válido.

### Crear:

```text
1 caso positivo

1 caso negativo
```

---

# DIAPOSITIVA 37 — FORMATO

```text
ID:

Título:

Precondiciones:

Datos de prueba:

Pasos:

Resultado esperado:
```

---

# DIAPOSITIVA 38 — REVISIÓN

Para revisar nuestro caso:

```text
¿Qué estamos validando?

¿Qué regla cubre?

¿Los datos son adecuados?

¿Los pasos son claros?

¿El resultado es verificable?

¿Podemos determinar PASS / FAIL?
```

---

# DIAPOSITIVA 39 — DE LAS PRUEBAS MANUALES A LA AUTOMATIZACIÓN

## Una pregunta:

> ¿Qué ocurre si necesitamos ejecutar la misma prueba 100 veces?

```text
PRUEBA MANUAL

Tester
  ↓
Acciones
  ↓
Sistema
  ↓
Observación
  ↓
Resultado
```

---

# DIAPOSITIVA 40 — PRUEBA AUTOMATIZADA

```text
SCRIPT
  ↓
Acciones
  ↓
Sistema
  ↓
Validación automática
  ↓
PASS / FAIL
```

---

# DIAPOSITIVA 41 — ¿QUÉ ES AUTOMATIZAR?

> Utilizar herramientas y scripts para ejecutar determinadas pruebas y comprobar sus resultados de forma automática.

### No significa:

> Automatizar todo.

---

# DIAPOSITIVA 42 — ¿QUÉ PRUEBAS PUEDEN SER CANDIDATAS?

```text
REPETITIVAS
ESTABLES
FRECUENTES
VERIFICABLES
ALTO VOLUMEN
REGRESIÓN
```

---

# DIAPOSITIVA 43 — EJEMPLO

### Login

Si necesitamos ejecutar:

```text
100 usuarios
×
varios escenarios
×
varias ejecuciones
```

La automatización puede ayudar a reducir el trabajo repetitivo.

---

# DIAPOSITIVA 44 — ¿TODO SE AUTOMATIZA?

No necesariamente.

Algunas pruebas requieren mayor intervención humana:

```text
Exploración

Usabilidad

Experiencia de usuario

Evaluación visual

Comportamientos no totalmente definidos
```

---

# DIAPOSITIVA 45 — HERRAMIENTAS

### Algunas herramientas de automatización

```text
Selenium

Playwright

Cypress
```

También existen herramientas orientadas a:

```text
APIs
Mobile
Performance
```

---

# DIAPOSITIVA 46 — PRIMERO DISEÑAR, DESPUÉS AUTOMATIZAR

```text
¿QUÉ DEBO PROBAR?
        ↓
CASO DE PRUEBA
        ↓
¿ES REPETITIVO?
        ↓
¿ES ESTABLE?
        ↓
¿ES VERIFICABLE?
        ↓
AUTOMATIZACIÓN
```

---

# DIAPOSITIVA 47 — RESUMEN

```text
REQUISITO
    ↓
REGLAS
    ↓
ESCENARIOS
    ↓
CASOS DE PRUEBA
    ↓
DATOS
    ↓
EJECUCIÓN
    ↓
RESULTADOS
```

---

# DIAPOSITIVA 48 — IDEA FINAL

# Primero sabemos qué probar.

# Después diseñamos cómo probarlo.

# Finalmente decidimos cómo ejecutarlo.

---

# DIAPOSITIVA 49 — PRÓXIMA CLASE

## ¿Cómo determinar sistemáticamente

qué casos de prueba necesitamos?

### Próximos conceptos

```text
Partición de equivalencia

Valores límite

Tablas de decisión

Transición de estados
```

---

# DIAPOSITIVA 50 — CIERRE

# ¿Qué preguntas tienen?

### Diseño de casos de prueba

**QA — Aseguramiento de la Calidad y Pruebas Manuales**
