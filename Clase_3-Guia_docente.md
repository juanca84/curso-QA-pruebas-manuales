# Guía del docente — Clase 3: Diseño de casos de prueba e introducción a la automatización

**Duración:** 2h15m
**Distribución:** 70% teoría y explicación / 25% ejemplo guiado / 5% práctica corta

---

## Propósito de la clase

El estudiante debe comprender que diseñar casos de prueba no consiste solamente en escribir pasos.

Debe poder responder:

> **¿Qué debo probar, bajo qué condiciones, con qué datos y cómo sé si el resultado es correcto?**

---

## Objetivos

Al finalizar la clase, el estudiante podrá:

* Explicar qué es un caso de prueba.
* Diferenciar un caso de prueba de una simple lista de pasos.
* Identificar los elementos de un caso de prueba.
* Transformar requisitos y reglas de negocio en escenarios.
* Diseñar casos positivos y negativos.
* Identificar datos relevantes para las pruebas.
* Identificar valores límite.
* Definir resultados esperados verificables.
* Revisar la calidad de un caso de prueba.
* Comprender conceptualmente qué es la automatización.
* Identificar qué tipos de pruebas pueden ser candidatas para automatización.

---

# Idea central de la clase

**REQUISITO → REGLAS → CONDICIONES → ESCENARIOS → CASOS DE PRUEBA → DATOS → EJECUCIÓN → RESULTADO**

Después podemos preguntarnos:

**¿Es repetitivo? ¿Es estable? ¿Es frecuente? ¿Es verificable?**

Si la respuesta es sí, puede ser un candidato para automatización.

---

# Ayudas memoria del docente

> Estas ayudas son para el docente y **no forman parte de las diapositivas**.

### QA

**PREVENIR → DETECTAR → MEJORAR**

### Requisito

Lo que el sistema debe cumplir.

### Regla de negocio

Una condición o restricción que el sistema debe respetar.

### Criterio de aceptación

Ayuda a determinar cuándo una funcionalidad puede considerarse aceptable.

### Escenario

Una situación o comportamiento que queremos validar.

### Escenario vs caso de prueba

El escenario responde:

> **¿Qué situación quiero probar?**

El caso de prueba responde:

> **¿Cómo voy a comprobarla?**

### Caso negativo ≠ prueba fallida

Una prueba negativa puede terminar en **PASS** si el sistema rechaza correctamente el dato inválido.

### Límites

Pensar en:

**Antes → En el límite → Después**

### Resultado esperado

Debe permitir determinar claramente:

**PASS / FAIL**

### Cobertura

Más casos no significa necesariamente mejor cobertura.

### Automatización

La automatización no decide qué probar.

Ayuda a ejecutar y verificar automáticamente determinados casos.

---

# 1. ¿Qué significa diseñar un caso de prueba?

**Tiempo: 10 minutos**

📽️ **Mostrar diapositivas 1–5**

Comenzar presentando el tema de la clase.

Explicar que hasta ahora hemos hablado de:

* requisitos,
* reglas,
* escenarios,
* riesgos.

Ahora debemos transformar ese análisis en algo que podamos ejecutar.

La pregunta principal es:

> **¿Cómo convertimos una condición que queremos validar en una prueba concreta?**

Explicar que diseñar un caso de prueba significa definir:

* qué queremos validar,
* bajo qué condiciones,
* qué datos utilizaremos,
* qué acciones realizaremos,
* qué resultado esperamos.

No se trata simplemente de escribir pasos.

---

# 2. Un caso de prueba no es solamente una lista de pasos

**Tiempo: 5 minutos**

📽️ **Mostrar diapositivas 6–7**

Utilizar el ejemplo de inicio de sesión.

Podemos escribir:

1. Abrir el sistema.
2. Escribir usuario.
3. Escribir contraseña.
4. Presionar iniciar sesión.

Pero preguntar:

> ¿Qué estamos validando?

> ¿Qué datos usamos?

> ¿Qué debería ocurrir?

> ¿Cómo sabemos si la prueba pasó?

Explicar que una lista de pasos puede indicar acciones, pero un caso de prueba debe tener un objetivo de validación y un resultado esperado.

---

# 3. Estructura de un caso de prueba

**Tiempo: 15 minutos**

📽️ **Mostrar diapositivas 8–14**

Presentar la estructura:

* ID
* Título
* Precondiciones
* Datos de prueba
* Pasos
* Resultado esperado

### ID y título

📽️ **Mostrar diapositiva 9**

Ejemplo:

**TC-LOGIN-001**

Título poco útil:

> Probar login

Título mejor:

> Iniciar sesión con credenciales válidas

Explicar que el título debe indicar claramente qué estamos validando.

### Precondiciones

📽️ **Mostrar diapositiva 10**

Ejemplo:

* Usuario registrado.
* Usuario activo.
* Sistema disponible.

Explicar que una precondición define qué debe cumplirse antes de comenzar la prueba.

### Datos de prueba

📽️ **Mostrar diapositiva 11**

Ejemplo:

```text
Usuario: user@test.com
Contraseña: Test1234
```

Explicar que los datos deben ser suficientes para ejecutar la prueba y reproducirla.

### Pasos

📽️ **Mostrar diapositiva 12**

Los pasos deben ser:

* claros,
* ordenados,
* reproducibles.

### Resultado esperado

📽️ **Mostrar diapositivas 13–14**

Evitar:

> El sistema funciona correctamente.

Preferir:

> El sistema permite el acceso y muestra la página principal.

Preguntar:

> ¿Con este resultado podemos determinar PASS o FAIL?

Explicar que el resultado esperado debe ser observable y verificable.

---

# 4. Del requisito al caso de prueba

**Tiempo: 20 minutos**

📽️ **Mostrar diapositivas 15–18**

Presentar el requisito:

> El sistema debe permitir registrar un usuario utilizando nombre, correo electrónico y contraseña. Todos los campos son obligatorios. El correo debe tener un formato válido y no debe estar registrado previamente.

Primero analizar el requisito.

No comenzar directamente escribiendo casos.

Preguntar:

> ¿Qué reglas encontramos?

---

## Reglas del ejemplo

📽️ **Mostrar diapositiva 16**

Identificar:

* R1: nombre obligatorio.
* R2: correo obligatorio.
* R3: contraseña obligatoria.
* R4: correo con formato válido.
* R5: correo no registrado previamente.

Explicar que estas reglas nos ayudan a descubrir qué debemos probar.

---

## Pensar en escenarios

📽️ **Mostrar diapositivas 17–18**

Construir los escenarios:

* Datos válidos.
* Nombre vacío.
* Correo vacío.
* Contraseña vacía.
* Correo inválido.
* Correo ya registrado.

Aquí hacer énfasis:

> **Primero pensamos qué situaciones debemos validar. Después diseñamos los casos de prueba.**

Tomar como ejemplo:

### Escenario

> Registrar usuario con correo inválido.

### Caso de prueba

Definimos:

* datos,
* pasos,
* resultado esperado.

Ejemplo:

```text
Datos:
juan@

Acción:
Intentar registrar el usuario.

Resultado esperado:
El sistema rechaza el registro y muestra una validación indicando que el correo no tiene un formato válido.
```

---

# 5. Casos positivos y negativos

**Tiempo: 15 minutos**

📽️ **Mostrar diapositivas 19–21**

Explicar:

### Caso positivo

Probamos datos válidos y esperamos el comportamiento correcto.

Ejemplo:

```text
Correo: juan@test.com
```

Esperamos:

> Registro exitoso.

### Caso negativo

Probamos una condición inválida y esperamos que el sistema la rechace correctamente.

Ejemplo:

```text
Correo: juan@
```

Esperamos:

> El sistema rechaza el registro y muestra una validación.

---

## Caso negativo ≠ prueba fallida

📽️ **Mostrar diapositiva 21**

Este punto es importante.

Ejemplo:

```text
Dato inválido
      ↓
Sistema rechaza correctamente
      ↓
PASS
```

Explicar:

> Una prueba negativa no significa que queremos que el sistema falle.

Significa que queremos comprobar cómo se comporta frente a una condición inválida.

---

# 6. Datos de prueba y valores límite

**Tiempo: 15 minutos**

📽️ **Mostrar diapositivas 22–23**

Presentar:

> La nueva contraseña debe tener entre 8 y 20 caracteres.

Preguntar:

> ¿Qué valores probarían?

No quedarse únicamente con:

* 10 caracteres.

Buscar límites:

* 7 → inválido.
* 8 → válido.
* 9 → válido.
* 19 → válido.
* 20 → válido.
* 21 → inválido.

Explicar la idea:

**Antes del límite → límite → después del límite**

Mostrar el esquema de la diapositiva:

```text
7     8                 20     21
│     │                  │      │
❌    ✓                  ✓      ❌
      └──── válido ──────┘
```

---

# 7. Resultado esperado

**Tiempo: 10 minutos**

📽️ **Mostrar diapositiva 13 y reforzar con diapositivas 21–23**

Volver a explicar que un buen caso debe permitir determinar claramente el resultado.

Comparar:

❌

> El sistema funciona correctamente.

vs.

✓

> El sistema rechaza la contraseña de 7 caracteres y muestra un mensaje indicando que debe contener al menos 8 caracteres.

Preguntar:

> ¿Podemos decidir PASS o FAIL?

Si la respuesta es sí, el resultado está suficientemente definido.

---

# 8. ¿Cuántos casos de prueba necesitamos?

**Tiempo: 10 minutos**

📽️ **Mostrar diapositivas 24–25**

Explicar que no existe una cantidad fija de casos para cualquier funcionalidad.

Depende de:

* requisitos,
* reglas,
* condiciones,
* riesgos,
* cobertura.

Evitar dos extremos:

### Muy pocos casos

Podemos dejar comportamientos sin validar.

### Demasiados casos redundantes

Aumentamos esfuerzo sin obtener una cobertura significativa adicional.

La idea es:

> **Casos suficientes y relevantes para cubrir el comportamiento que necesitamos validar.**

---

# 9. Calidad de un caso de prueba

**Tiempo: 10 minutos**

📽️ **Mostrar diapositiva 26**

Utilizar la siguiente lista de revisión:

* ¿Está relacionado con un requisito?
* ¿Tiene un objetivo claro?
* ¿Los datos son adecuados?
* ¿Los pasos son reproducibles?
* ¿El resultado esperado es verificable?
* ¿Permite determinar PASS o FAIL?
* ¿Aporta cobertura?

Explicar que escribir muchos casos no significa necesariamente diseñar buenos casos.

---

# 10. Ejemplo guiado completo

**Tiempo: 34 minutos**

📽️ **Mostrar diapositivas 27–35**

Este será el principal ejercicio guiado de la clase.

---

## Requisito

📽️ **Mostrar diapositiva 27**

Presentar:

> El sistema permite cambiar la contraseña. La nueva contraseña debe tener entre 8 y 20 caracteres. La nueva contraseña y su confirmación deben coincidir.

No comenzar todavía escribiendo casos.

Primero analizar.

---

## Analizar las reglas

📽️ **Mostrar diapositiva 28**

Identificar:

* mínimo 8 caracteres,
* máximo 20 caracteres,
* confirmación debe coincidir.

Preguntar:

> ¿Qué situaciones deberíamos probar?

---

## Construir escenarios

📽️ **Mostrar diapositiva 29**

Construir juntos:

| Escenario | Condición              |
| --------- | ---------------------- |
| E1        | Contraseña válida      |
| E2        | Menos de 8             |
| E3        | Exactamente 8          |
| E4        | Exactamente 20         |
| E5        | Más de 20              |
| E6        | Confirmación diferente |

Explicar que ahora tenemos escenarios.

Todavía no tenemos necesariamente todos los casos de prueba detallados.

---

## Caso TC-PASS-001

📽️ **Mostrar diapositivas 30–31**

### Datos

```text
Nueva contraseña: Password123
Confirmación: Password123
```

### Precondición

> Usuario autenticado.

### Resultado esperado

> El sistema permite cambiar la contraseña y muestra una confirmación de operación exitosa.

Explicar cómo pasamos del escenario al caso de prueba completo.

---

## Caso negativo TC-PASS-002

📽️ **Mostrar diapositiva 32**

Datos:

```text
Nueva contraseña: Test123
Confirmación: Test123
```

Tiene menos de 8 caracteres.

Esperamos:

> El sistema rechaza el cambio y muestra una validación indicando que la contraseña debe tener al menos 8 caracteres.

---

## Caso límite TC-PASS-003

📽️ **Mostrar diapositiva 33**

Datos:

```text
12345678
```

Tiene exactamente 8 caracteres.

Esperamos:

> El sistema permite el cambio.

Explicar que este caso valida el límite inferior.

---

## Caso límite TC-PASS-004

📽️ **Mostrar diapositiva 34**

Datos:

```text
12345678901234567890
```

Tiene exactamente 20 caracteres.

Esperamos:

> El sistema permite el cambio.

Explicar que este caso valida el límite superior.

---

## Preguntas de QA

📽️ **Mostrar diapositiva 35**

Utilizar las preguntas para reforzar el razonamiento:

> ¿Qué estamos validando?

> ¿Qué requisito estamos cubriendo?

> ¿Qué regla estamos validando?

> ¿Qué podría salir mal?

> ¿Qué datos necesitamos?

> ¿Cuál es el resultado esperado?

> ¿Cómo sabemos si la prueba pasó?

---

# 11. Práctica corta

**Tiempo: 6 minutos**

📽️ **Mostrar diapositivas 36–38**

Sistema: https://www.saucedemo.com/

Presentar:

> El sistema debe permitir continuar con el checkout cuando el usuario proporciona nombre, apellido y código postal. Estos datos son obligatorios.

Solicitar a los estudiantes:

> Crear 2 casos de prueba.

Uno positivo y uno negativo.

Esto nos permite hacer exactamente los dos casos que necesitamos:

Positivo

First Name: Juan
Last Name: Condori
Zip Code: 00000
Resultado: permite continuar al resumen del pedido.

Negativo

First Name: vacío
Last Name: Condori
Zip Code: 00000
Resultado: no permite continuar y muestra un mensaje indicando que el nombre es obligatorio.
Para la clase, elegiría este

Porque nos permite enseñar claramente:

Requisito → regla → escenario → caso de prueba
---
## Plantilla de caso de prueba
PLANTILLA DE CASO DE PRUEBA
CASO DE PRUEBA 1

ID:
Título:

Precondiciones:
Datos de prueba:

Pasos:
1.
2.
3.
4.

Resultado esperado:

CASO DE PRUEBA 2

ID:
Título:

Precondiciones:
Datos de prueba:

Pasos:
1.
2.
3.
4.

Resultado esperado:

REVISIÓN

Caso de prueba 1:

¿Qué condición estoy validando?
¿Qué regla del requisito estoy cubriendo?
¿Los datos de prueba son adecuados?
¿Los pasos permiten reproducir la prueba?
¿El resultado esperado es claro y verificable?
¿Cómo determinaría PASS o FAIL?

Caso de prueba 2:

¿Qué condición estoy validando?
¿Qué regla del requisito estoy cubriendo?
¿Los datos de prueba son adecuados?
¿Los pasos permiten reproducir la prueba?
¿El resultado esperado es claro y verificable?
¿Cómo determinaría PASS o FAIL?

## Formato

📽️ **Mostrar diapositiva 37**

```text
ID:

Título:

Precondiciones:

Datos de prueba:

Pasos:

Resultado esperado:
```

Dar aproximadamente 6 minutos.

No profundizar todavía en técnicas avanzadas de diseño.

---

## Revisión

📽️ **Mostrar diapositiva 38**

Revisar rápidamente:

* ¿Qué valida?
* ¿Qué regla cubre?
* ¿Los datos son adecuados?
* ¿Los pasos son claros?
* ¿El resultado esperado es verificable?
* ¿Podemos determinar PASS o FAIL?

La práctica debe ser corta.

El objetivo es comprobar si entendieron el proceso de diseño.

---

# 12. Introducción a la automatización

**Tiempo: 10 minutos**

📽️ **Mostrar diapositivas 39–46**

Aquí hacer solamente una introducción conceptual.

**No realizar práctica de automatización.**

Plantear una situación:

> Tenemos que ejecutar el mismo caso de prueba 100 veces.

Preguntar:

> ¿Tiene sentido que una persona repita exactamente las mismas acciones 100 veces?

Explicar que aquí aparece la automatización.

---

## Prueba manual

📽️ **Mostrar diapositiva 39**

```text
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

## Prueba automatizada

📽️ **Mostrar diapositiva 40**

```text
Script
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

## ¿Qué significa automatizar?

📽️ **Mostrar diapositiva 41**

Explicar:

> Automatizar significa utilizar herramientas o scripts para ejecutar determinadas pruebas y comprobar automáticamente sus resultados.

Aclarar:

> **No significa automatizar todo.**

---

## Candidatos para automatización

📽️ **Mostrar diapositiva 42**

Algunas características:

* repetitivos,
* estables,
* frecuentes,
* verificables,
* alto volumen,
* regresión.

---

## Ejemplo

📽️ **Mostrar diapositiva 43**

Ejemplo:

> Ejecutar login con muchos usuarios y diferentes escenarios.

Si necesitamos repetirlo constantemente, puede ser un buen candidato para automatización.

---

## ¿Todo se automatiza?

📽️ **Mostrar diapositiva 44**

No.

Algunas actividades requieren intervención humana:

* pruebas exploratorias,
* usabilidad,
* experiencia de usuario,
* evaluación visual,
* comportamientos todavía no definidos.

Explicar que la automatización complementa las pruebas manuales.

---

## Herramientas

📽️ **Mostrar diapositiva 45**

Mencionar brevemente:

* Selenium
* Playwright
* Cypress

No entrar en instalación, configuración ni código.

El objetivo de esta clase es solamente que conozcan el concepto.

---

## Primero diseñar, después automatizar

📽️ **Mostrar diapositiva 46**

Reforzar:

```text
¿Qué probar?
      ↓
Caso de prueba
      ↓
¿Es repetitivo?
      ↓
¿Es estable?
      ↓
¿Es verificable?
      ↓
Automatización
```

La automatización viene después del diseño de la prueba.

---

# 13. Cierre de la clase

**Tiempo: 5 minutos**

📽️ **Mostrar diapositivas 47–50**

Repasar:

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

## Idea final

📽️ **Mostrar diapositiva 48**

> **Primero sabemos qué probar.
> Después diseñamos cómo probarlo.
> Finalmente decidimos cómo ejecutarlo.**

---

## Próxima clase

📽️ **Mostrar diapositiva 49**

Introducir brevemente:

* particiones de equivalencia,
* valores límite,
* tablas de decisión,
* transición de estados.

Explicar que en la siguiente clase veremos técnicas para determinar de forma más sistemática **qué casos de prueba necesitamos**.

---

## Cierre

📽️ **Mostrar diapositiva 50**

Preguntar:

> **¿Qué preguntas tienen?**

Finalizar la clase.
