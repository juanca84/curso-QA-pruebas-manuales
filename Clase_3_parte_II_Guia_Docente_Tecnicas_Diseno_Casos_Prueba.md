# Guía del Docente
## Clase extra — Técnicas de Diseño de Casos de Prueba

**Duración:** 1 hora  
**Módulo:** Estrategia de Aseguramiento de la Calidad y Pruebas Manuales  
**Tema:** Técnicas de diseño de casos de prueba  
**Modalidad:** Teórica + ejemplos guiados

---

## Objetivo general

Al finalizar la clase, el estudiante podrá:

- Comprender qué son las técnicas de diseño de casos de prueba.
- Aplicar **partición de equivalencia**.
- Aplicar **análisis de valores límite**.
- Comprender y construir **tablas de decisión**.
- Comprender y diseñar pruebas basadas en **transición de estados**.
- Seleccionar una técnica apropiada según el comportamiento del requisito.
- Entender que varias técnicas pueden combinarse.

---

## Distribución de la clase

| Diapositivas | Tema | Tiempo |
|---|---|---:|
| 1–3 | Introducción | 5 min |
| 4–6 | Partición de equivalencia | 15 min |
| 7–9 | Valores límite | 15 min |
| 10–12 | Tablas de decisión | 10 min |
| 13–15 | Transición de estados | 10 min |
| 16 | Integración | 3 min |
| 17 | Selección de técnica | 2 min |
| 18–20 | Resumen y cierre | 5 min |
| **Total** | | **60 min** |

---

# Diapositiva 1 — Portada

## TÉCNICAS DE DISEÑO DE CASOS DE PRUEBA

### Qué debe explicar el docente

Comenzar conectando esta clase con la clase anterior:

> "En la clase anterior aprendimos qué es un caso de prueba, cómo estructurarlo y cómo pasar de un requisito a escenarios y casos de prueba."

Ahora explicar:

> "Pero tenemos una pregunta importante: cuando tenemos un requisito, ¿cómo decidimos qué datos debemos probar?"

Aquí introducimos el concepto de **técnicas de diseño de pruebas**.

### Definición

> **Una técnica de diseño de casos de prueba es un método sistemático que ayuda al tester a seleccionar y construir casos de prueba a partir de los requisitos, reglas de negocio o comportamiento esperado del sistema.**

La palabra importante es **sistemático**.

No queremos que el tester simplemente diga:

> "Voy a probar algunos valores que se me ocurran."

Queremos que exista una razón detrás de la selección de cada prueba.

---

# Diapositiva 2 — ¿Por qué necesitamos técnicas?

### Qué explicar

Preguntar primero:

> "Si un campo acepta números entre 1 y 1.000.000, ¿tenemos que probar los 1.000.000 de valores?"

La respuesta es no.

Explicar:

> "El objetivo del testing no es probar absolutamente todas las posibilidades. En muchos casos eso sería imposible o demasiado costoso."

Las técnicas permiten **seleccionar un subconjunto representativo**.

### Concepto importante: cobertura

> **Cobertura** es qué parte de los requisitos, escenarios, condiciones o comportamientos estamos verificando mediante nuestras pruebas.

No significa necesariamente:

> "Tengo muchos casos, entonces tengo buena cobertura."

Podemos tener 100 casos mal diseñados y dejar escenarios importantes sin probar.

Por eso buscamos:

> **Casos relevantes + cobertura adecuada.**

### Frase clave

> **"No buscamos probar más; buscamos probar de manera inteligente."**

---

# Diapositiva 3 — Las 4 técnicas

Presentar las cuatro técnicas:

1. **Partición de equivalencia**
2. **Análisis de valores límite**
3. **Tablas de decisión**
4. **Transición de estados**

Aclarar:

> "No son las únicas técnicas existentes, pero son especialmente útiles para el testing funcional y manual que estamos estudiando."

También aclarar:

> "No siempre tenemos que utilizar las cuatro técnicas en un mismo requisito."

La elección depende del tipo de requisito.

---

# Diapositiva 4 — Partición de equivalencia

## Definición

> **La partición de equivalencia consiste en dividir un conjunto de valores de entrada en grupos o particiones cuyos elementos deberían producir un comportamiento equivalente del sistema.**

### Explicación sencilla

> "Si tenemos muchos valores que deberían comportarse de la misma manera, podemos seleccionar algunos representantes en lugar de probarlos todos."

### Ejemplo: edad

Requisito:

> "El sistema permite registrar usuarios con edades entre 18 y 65 años."

Preguntar:

> "¿Todas las edades entre 18 y 65 deberían producir el mismo resultado respecto a esta regla?"

Sí.

Entonces podemos formar:

```text
0 ───────── 17 | 18 ───────── 65 | 66 ─────────→
   inválido          válido            inválido
```

Tenemos **tres particiones**.

---

# Diapositiva 5 — Ejemplo de particiones

Explicar cada partición.

### Partición 1

**0–17**

Todos los valores pertenecen al grupo:

> "Edad menor al mínimo permitido."

Resultado esperado:

**Inválido.**

### Partición 2

**18–65**

Grupo:

> "Edad dentro del rango permitido."

Resultado:

**Válido.**

### Partición 3

**66 en adelante**

Grupo:

> "Edad mayor al máximo permitido."

Resultado:

**Inválido.**

### ¿Por qué 17, 30 y 66?

Porque queremos seleccionar **representantes**.

```text
17 → representa menores de 18
30 → representa edades permitidas
66 → representa mayores de 65
```

### Punto pedagógico importante

Aclarar:

> "No significa que probar un único valor garantice que todos los valores de la partición funcionen. Es una estrategia para reducir el número de pruebas basándonos en el comportamiento esperado."

---

# Diapositiva 6 — ¿Qué debemos recordar?

### Partición de equivalencia responde:

> **¿Qué grupos de entradas deberían comportarse de manera equivalente?**

El proceso mental es:

```text
Requisito
   ↓
Identificar regla
   ↓
Identificar grupos
   ↓
Seleccionar representantes
   ↓
Crear casos de prueba
```

### Ejemplo adicional

Requisito:

> "Un código debe tener entre 6 y 10 caracteres."

Podemos identificar:

- Menos de 6 → inválido
- 6–10 → válido
- Más de 10 → inválido

Representantes:

```text
5 → inválido
8 → válido
11 → inválido
```

---

# Diapositiva 7 — Análisis de valores límite

## Definición

> **El análisis de valores límite es una técnica que concentra las pruebas en los valores situados en los límites de los rangos o condiciones definidos por el requisito.**

### Motivo

> "Los límites son puntos donde cambia el comportamiento esperado."

Por ejemplo:

```text
17 → inválido
18 → válido
```

El comportamiento cambia justamente entre 17 y 18.

---

# Diapositiva 8 — Probando los límites

Volvemos al ejemplo:

> Edad permitida: 18–65.

Mostrar:

```text
17   18   19
```

Y:

```text
64   65   66
```

### Explicar cada uno

- **17:** justo antes del límite inferior.
- **18:** límite inferior.
- **19:** justo después del límite.
- **64:** antes del límite superior.
- **65:** límite superior.
- **66:** justo después del límite.

### ¿Por qué probar los límites?

> "Muchos errores aparecen porque el desarrollador implementó incorrectamente una condición."

Por ejemplo, el requisito dice:

```text
18 ≤ edad ≤ 65
```

Pero el código podría terminar implementando accidentalmente:

```text
18 < edad < 65
```

En ese caso:

- 18 fallaría.
- 65 fallaría.

Aunque ambos deberían ser válidos.

### Punto importante

El QA debe comprobar **el comportamiento real**, no asumir que la implementación respeta el requisito.

---

# Diapositiva 9 — Equivalencia + límites

Explicar:

> "No debemos pensar que tenemos que escoger entre partición de equivalencia o valores límite. Podemos utilizar ambas."

### Ejemplo

Partición:

```text
<18 | 18–65 | >65
```

Después identificamos los límites:

```text
17 | 18 | 19
64 | 65 | 66
```

### Diferencia fundamental

**Partición de equivalencia:**

> ¿Qué grupos existen?

**Valores límite:**

> ¿Qué pasa en los extremos de esos grupos?

### Regla práctica

Cuando tenemos un requisito basado en rangos:

> **Primero identifica las particiones y después revisa sus límites.**

---

# Diapositiva 10 — Tablas de decisión

## Definición

> **Una tabla de decisión es una técnica que representa diferentes combinaciones de condiciones y las acciones o resultados correspondientes.**

Es especialmente útil cuando existen **reglas de negocio con múltiples condiciones**.

### Ejemplo

> "El usuario puede descargar un documento si está autenticado y tiene permiso."

Tenemos dos condiciones:

```text
Autenticado
Tiene permiso
```

Cada una puede ser:

```text
Sí / No
```

Por lo tanto tenemos diferentes combinaciones.

---

# Diapositiva 11 — Ejemplo

Explicar la tabla columna por columna.

### Caso 1

```text
Autenticado = Sí
Permiso = Sí
```

Resultado:

**Permitir descarga.**

### Caso 2

```text
Autenticado = Sí
Permiso = No
```

Resultado:

**Denegar.**

### Caso 3

```text
Autenticado = No
Permiso = Sí
```

Resultado:

**Denegar.**

### Caso 4

```text
Autenticado = No
Permiso = No
```

Resultado:

**Denegar.**

### Concepto importante

Cada columna representa una **regla o combinación de condiciones**.

Y esa combinación puede convertirse en:

> **Un escenario o caso de prueba.**

---

# Diapositiva 12 — ¿Qué nos aporta?

Las tablas de decisión son especialmente útiles para evitar:

> **Olvidar combinaciones de condiciones.**

Ejemplo:

> "Si el cliente es premium y la compra supera Bs 500 y paga con tarjeta, recibe descuento."

Tenemos varias condiciones.

Si diseñamos las pruebas solamente "a ojo", podríamos olvidar combinaciones.

La tabla obliga al QA a analizar las condiciones de forma estructurada.

### Frase clave

> **"Cuando el resultado depende de varias condiciones, piensa en una tabla de decisión."**

---

# Diapositiva 13 — Transición de estados

## Definición

> **La técnica de transición de estados permite diseñar pruebas verificando cómo cambia el estado de un sistema cuando ocurre un evento o acción.**

### Tres conceptos importantes

#### Estado

Una situación en la que puede encontrarse el sistema.

Ejemplo:

**Activa**

#### Evento

Algo que ocurre y puede provocar un cambio.

Ejemplo:

**Tres intentos fallidos.**

#### Transición

El cambio de un estado a otro.

```text
Activa → Bloqueada
```

---

# Diapositiva 14 — Estados y eventos

Analizar la tabla.

### Caso

**Activa + 3 intentos incorrectos**

Resultado:

**Bloqueada**

Después:

**Bloqueada + administrador desbloquea**

Resultado:

**Activa**

### Caso interesante

> "¿Qué ocurre si una cuenta bloqueada intenta iniciar sesión?"

De acuerdo con la regla:

**Debe permanecer bloqueada.**

Esto muestra por qué debemos probar las transiciones y no solamente verificar que existen los estados.

### Punto clave

> "En transición de estados nos interesa comprobar que el sistema pasa al estado correcto cuando ocurre un evento válido y que no permite transiciones que no deberían existir."

---

# Diapositiva 15 — ¿Cuándo utilizarla?

Ejemplos:

### Cuenta

```text
Activa → Bloqueada
```

### Pedido

```text
Pendiente → Enviado → Entregado
```

### Documento

```text
Borrador → En revisión → Aprobado
```

### Pago

```text
Pendiente → Procesado
Pendiente → Rechazado
```

### Ticket

```text
Abierto → En progreso → Resuelto → Cerrado
```

### Pregunta para los estudiantes

> "¿Qué podría pasar si intentamos realizar una transición que el negocio no permite?"

Por ejemplo:

```text
Entregado → Pendiente
```

Si esa transición no está definida por el negocio, debería investigarse o considerarse un comportamiento inválido.

---

# Diapositiva 16 — Una técnica no excluye a otra

Enseñar:

> **Las técnicas no son mutuamente excluyentes.**

Un mismo requisito puede necesitar varias.

Ejemplo: transferencia entre Bs 10 y Bs 5.000.

### Partición

Nos ayuda con:

> Los valores permitidos.

### Valores límite

Nos ayuda con:

> Los extremos del monto.

### Tabla de decisión

Nos ayuda con:

> Autenticación + saldo suficiente.

### Transición de estados

Nos ayuda con:

> Pendiente → Procesada / Rechazada.

### Mensaje importante

> "La técnica se selecciona según el aspecto del requisito que queremos cubrir."

---

# Diapositiva 17 — ¿Qué técnica utilizarías?

El objetivo es **reconocer la técnica adecuada**, no diseñar nuevamente los casos.

Presentar cada situación y preguntar antes de discutir la respuesta.

### A

> Formulario permite ingresar edad entre 18 y 65.

**Respuesta:** Partición de equivalencia + valores límite.

### B

> Descuento depende de tipo de cliente, monto y forma de pago.

**Respuesta:** Tabla de decisión.

### C

> Pedido: Pendiente, Enviado, Entregado, Cancelado.

**Respuesta:** Transición de estados.

### D

> Código acepta entre 6 y 10 caracteres.

**Respuesta:** Partición de equivalencia + valores límite.

### Pregunta adicional

> "¿Por qué no usaríamos transición de estados para el ejemplo A?"

La respuesta esperada:

> "Porque el requisito presenta un rango de valores, no una secuencia de estados que cambian mediante eventos."

---

# Diapositiva 18 — Resumen

Pedir a los estudiantes que expliquen cada técnica con sus propias palabras.

| Técnica | Pregunta |
|---|---|
| **Partición de equivalencia** | ¿Qué grupos existen? |
| **Valores límite** | ¿Qué ocurre en los extremos? |
| **Tabla de decisión** | ¿Qué combinaciones de condiciones existen? |
| **Transición de estados** | ¿Cómo cambia el sistema? |

---

# Diapositiva 19 — Idea final

Explicar:

> "Un buen diseño de pruebas no consiste simplemente en escribir muchos casos de prueba."

Un QA debe comenzar preguntándose:

```text
¿Qué dice el requisito?
        ↓
¿Qué comportamiento debo cubrir?
        ↓
¿Qué técnica me ayuda?
        ↓
¿Qué casos debo diseñar?
```

### Concepto importante

Las técnicas ayudan a que el diseño sea:

- **Sistemático**
- **Justificable**
- **Eficiente**
- **Orientado al riesgo**

---

# Diapositiva 20 — Cierre

Terminar con:

> **"La técnica correcta depende del tipo de requisito que estamos probando."**

Recordatorio:

```text
Rangos
 ↓
Partición + Límites

Condiciones
 ↓
Tabla de decisión

Estados
 ↓
Transición de estados
```

### Pregunta final

> **"Si mañana reciben un requisito nuevo, ¿qué es lo primero que deberían hacer antes de comenzar a escribir casos de prueba?"**

Respuesta esperada:

> **"Analizar el requisito y determinar qué técnica o técnicas de diseño son adecuadas."**

---

# Conceptos que el docente debe asegurarse de que aprendan

Al terminar la clase, comprueba que los estudiantes puedan explicar con sus propias palabras:

### 1. Partición de equivalencia

> Divide las entradas en grupos que deberían tener un comportamiento equivalente y permite seleccionar representantes de esos grupos.

### 2. Valores límite

> Se enfoca en los valores situados en los extremos de los rangos y en los valores inmediatamente alrededor de ellos.

### 3. Tabla de decisión

> Representa combinaciones de condiciones y sus resultados o acciones correspondientes.

### 4. Transición de estados

> Permite diseñar pruebas sobre los cambios entre estados provocados por determinados eventos.

### Concepto transversal

> **Las técnicas de diseño no sustituyen al análisis del requisito. Son herramientas para convertir ese análisis en una selección sistemática de casos de prueba.**

---

## Mensaje pedagógico final

El objetivo de esta clase no es que el estudiante memorice cuatro nombres. Debe aprender a **reconocer el tipo de problema que presenta un requisito** y seleccionar una técnica adecuada.

La secuencia mental que queremos desarrollar es:

```text
REQUISITO
   ↓
ANÁLISIS
   ↓
¿QUÉ TIPO DE COMPORTAMIENTO TENGO?
   ↓
SELECCIONAR TÉCNICA
   ↓
DISEÑAR CASOS DE PRUEBA
   ↓
EJECUTAR Y VALIDAR
```
