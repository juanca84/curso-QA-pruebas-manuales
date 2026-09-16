# CLASE 2 — GESTIÓN DE REQUERIMIENTOS Y STLC

**Duración:** 2 horas  
**Modalidad:** Teórico-práctica

## Distribución

- Inicio + repaso: **7 min**
- Gestión de requerimientos: **66 min**
- Ejemplo guiado: **15 min**
- STLC: **20 min**
- Práctica: **15 min**
- Cierre: **4 min**

---

# 1. Objetivos de la clase

## Objetivo general

Comprender cómo QA analiza los requerimientos de un sistema y cómo participa dentro del ciclo de vida de las pruebas de software (STLC).

## Objetivos específicos

Al finalizar la clase, el estudiante podrá:

- Explicar qué es un requerimiento.
- Diferenciar requerimientos funcionales y no funcionales.
- Reconocer reglas de negocio.
- Comprender qué son los criterios de aceptación.
- Identificar requerimientos ambiguos o incompletos.
- Explicar qué hace QA durante el análisis de requerimientos.
- Conocer las fases principales del STLC.
- Relacionar requerimientos con escenarios y casos de prueba.

---

# 2. Inicio y repaso de la Clase 1

**Tiempo: 7 minutos**

## Presentación

### Qué decir

> "En la clase anterior vimos los fundamentos de QA: qué es QA, qué son las pruebas, qué es un defecto, qué es un escenario y cuál es la mentalidad que debe tener un QA."

> "Hoy vamos a dar un paso más. Vamos a estudiar algo fundamental: los requerimientos."

> "Antes de probar un sistema necesitamos saber qué debería hacer ese sistema. Y esa información normalmente viene de los requerimientos."

### Pregunta inicial

> "¿Qué creen que pasa si el requerimiento está mal definido?"

Escuchar algunas respuestas.

Cerrar:

> "Si no sabemos exactamente qué debe hacer el sistema, tampoco podemos determinar correctamente qué debemos probar."

## Repaso rápido

Preguntar:

- ¿Qué es QA?
- ¿Qué es una prueba?
- ¿Qué es un requerimiento?
- ¿Qué es un defecto?
- ¿Qué es un escenario?

No volver a explicar los conceptos salvo que exista una confusión importante.

### Mini ejercicio

Mostrar:

> "El campo correo electrónico es obligatorio."

Preguntar:

> "¿Qué podríamos probar?"

Esperar:

- Correo ingresado.
- Correo vacío.
- Correo inválido.
- Diferentes formatos.

Cerrar:

> "Perfecto. Ahora vamos a entender cómo llegamos desde un requerimiento hasta esas pruebas."

---

# 3. ¿Qué es un requerimiento?

**Tiempo: 8 minutos**

Decir:

> "Un requerimiento describe una necesidad, condición o comportamiento que el sistema debe cumplir."

### Ejemplo

> "El sistema debe permitir registrar nuevos usuarios."

Explicar:

> "Este requerimiento nos dice qué debe hacer el sistema, pero todavía no nos dice todos los detalles necesarios para probarlo."

Preguntar:

> "¿Qué información nos falta?"

Dejar que los estudiantes respondan.

Posibles respuestas:

- ¿Qué datos debe ingresar?
- ¿Qué campos son obligatorios?
- ¿Qué validaciones existen?
- ¿Puede existir el mismo usuario?
- ¿Qué pasa si ocurre un error?

Concluir:

> "Y precisamente aquí empieza una parte importante del trabajo de QA: analizar el requerimiento."

---

# 4. ¿Por qué son importantes los requerimientos?

**Tiempo: 7 minutos**

Mostrar:

```text
REQUERIMIENTO
      ↓
ANÁLISIS
      ↓
¿QUÉ DEBEMOS VALIDAR?
      ↓
ESCENARIOS
      ↓
CASOS DE PRUEBA
```

Explicar:

> "El requerimiento es una de las principales fuentes de información para determinar qué debemos probar."

### Ejemplo

Si tenemos:

> "El usuario debe poder registrarse."

QA debe preguntarse:

> "¿Qué significa registrarse correctamente?"

Puede incluir:

- Nombre.
- Correo.
- Contraseña.
- Validaciones.
- Confirmaciones.
- Restricciones.

### Idea clave

> "Mientras mejor definido esté el requerimiento, más fácil será diseñar pruebas adecuadas."

---

# 5. Tipos de requerimientos

**Tiempo: 10 minutos**

## 5.1 Requerimientos funcionales

Decir:

> "Los requerimientos funcionales describen qué debe hacer el sistema."

Ejemplos:

- Registrar usuarios.
- Iniciar sesión.
- Crear productos.
- Generar reportes.
- Procesar pagos.

### Ejemplo

> "El sistema debe permitir al usuario registrar una cuenta."

Preguntar:

> "¿Qué estamos describiendo?"

Respuesta:

> "Una funcionalidad."

---

## 5.2 Requerimientos no funcionales

Decir:

> "Los requerimientos no funcionales describen características, restricciones o condiciones bajo las cuales debe funcionar el sistema."

Ejemplos:

- Rendimiento.
- Seguridad.
- Disponibilidad.
- Usabilidad.
- Compatibilidad.

### Ejemplo

> "El sistema debe responder en menos de 3 segundos."

Preguntar:

> "¿Qué estamos definiendo?"

Respuesta:

> "Una condición de rendimiento."

### Otro ejemplo

> "El sistema debe soportar 500 usuarios concurrentes."

Aclarar:

> "No estamos describiendo una funcionalidad concreta, sino una condición que debe cumplir el sistema."

No profundizar todavía en pruebas de rendimiento o seguridad.

---

# 6. Requerimiento y regla de negocio

**Tiempo: 8 minutos**

Explicar:

> "Un requerimiento puede decir qué debe hacer el sistema, mientras que una regla de negocio establece condiciones que deben cumplirse."

### Ejemplo

**Requerimiento:**

> "El sistema debe permitir registrar clientes."

**Regla de negocio:**

> "No se puede registrar un cliente si ya existe otro con el mismo número de documento."

Preguntar:

> "¿Debería QA probar esta regla?"

Sí.

Explicar:

> "Las reglas de negocio son muy importantes porque muchas veces contienen condiciones que debemos validar."

### Segundo ejemplo

**Requerimiento:**

> "El sistema debe permitir realizar una transferencia."

**Regla:**

> "El usuario no puede transferir un monto superior a su saldo disponible."

Preguntar:

> "¿Qué pasaría si QA solamente prueba una transferencia válida?"

Concluir:

> "No estaríamos validando completamente la regla de negocio."

---

# 7. Criterios de aceptación

**Tiempo: 10 minutos**

Introducir:

> "Otro elemento que ayuda mucho a QA son los criterios de aceptación."

Definición:

> "Son condiciones que deben cumplirse para considerar que una funcionalidad está correctamente implementada."

### Ejemplo

**Requerimiento:**

> "El sistema debe permitir registrar usuarios."

### Criterios de aceptación

- El nombre es obligatorio.
- El correo es obligatorio.
- El correo debe tener un formato válido.
- El correo no puede estar registrado previamente.
- La contraseña debe cumplir las reglas definidas.
- El sistema debe mostrar una confirmación cuando el registro sea exitoso.

Mostrar:

```text
REQUERIMIENTO
      ↓
CRITERIOS DE ACEPTACIÓN
      ↓
¿QUÉ DEBEMOS VALIDAR?
```

### Aclaración

> "Los criterios de aceptación pueden variar dependiendo de la metodología y de cómo trabaja cada equipo. Son especialmente comunes en equipos ágiles."

No profundizar todavía en historias de usuario.

---

# 8. Características de un buen requerimiento

**Tiempo: 8 minutos**

Presentar:

- Claro.
- Específico.
- Completo.
- Consistente.
- Medible.
- Verificable.

No buscar que memoricen la lista. Lo importante es comprenderla.

### Ejemplo

❌

> "El sistema debe ser rápido."

Preguntar:

> "¿Cómo podemos probar esto?"

Problema:

> "Rápido" no está definido.

Mejor:

> "El sistema debe mostrar los resultados de búsqueda en menos de 3 segundos."

Explicar:

> "Ahora QA tiene un criterio concreto que puede verificar."

### Segundo ejemplo

> "El usuario puede administrar productos."

Preguntar:

> "¿Qué significa administrar?"

Puede significar:

- Crear.
- Editar.
- Eliminar.
- Consultar.

Conclusión:

> "Necesitamos mayor precisión."

---

# 9. Requerimientos ambiguos o incompletos

**Tiempo: 8 minutos**

Mostrar:

> "El sistema debe permitir registrar usuarios de manera rápida y sencilla."

Preguntar:

> "¿Aceptaríamos este requerimiento?"

Dejar que los estudiantes encuentren los problemas.

### Posibles preguntas

- ¿Qué significa "rápida"?
- ¿Cuánto tiempo debe tomar?
- ¿Qué significa "sencilla"?
- ¿Qué campos son obligatorios?
- ¿Qué formato debe tener el correo?
- ¿Puede registrarse un correo existente?
- ¿Qué requisitos tiene la contraseña?
- ¿Qué mensaje se muestra después del registro?

### Mensaje importante

> "QA no debe inventar las respuestas."

> "Si el requerimiento no está claro, debemos solicitar una aclaración a la persona responsable."

---

# 10. Análisis de requerimientos desde la perspectiva de QA

**Tiempo: 10 minutos**

Aclarar:

> "Esta sección nos enseña el proceso general. Las técnicas específicas para diseñar pruebas las veremos en clases posteriores."

Cuando QA recibe un requerimiento:

```text
1. Comprender el requerimiento
              ↓
2. Identificar reglas de negocio
              ↓
3. Revisar criterios de aceptación
              ↓
4. Detectar ambigüedades
              ↓
5. Identificar información faltante
              ↓
6. Pensar en escenarios
              ↓
7. Identificar riesgos
              ↓
8. Solicitar aclaraciones
              ↓
9. Determinar qué debe validarse
```

### Explicación breve

**Comprender**

> "¿Qué debe hacer el sistema?"

**Reglas de negocio**

> "¿Qué condiciones deben cumplirse?"

**Criterios de aceptación**

> "¿Cómo sabemos que la funcionalidad está correcta?"

**Ambigüedades**

> "¿Existe algo que pueda interpretarse de diferentes maneras?"

**Información faltante**

> "¿Hay algo que necesitamos conocer antes de probar?"

**Escenarios**

> "¿Qué situaciones deberíamos validar?"

**Riesgos**

> "¿Qué podría salir mal o tener mayor impacto?"

**Aclaraciones**

> "¿Qué debemos preguntar al responsable del requerimiento?"

### Idea clave

> "El objetivo de esta etapa no es encontrar defectos en el software. Es encontrar problemas o dudas antes de que lleguen al software."

---

# 11. Ejemplo guiado — Registro de usuarios

**Tiempo: 15 minutos**

Este será el ejemplo central de la clase.

## Paso 1 — Requerimiento inicial

Mostrar:

> "El sistema debe permitir registrar usuarios de forma rápida y sencilla."

Preguntar:

> "¿Aceptaríamos este requerimiento tal como está?"

Respuesta esperada:

> No.

---

## Paso 2 — Analizar

Preguntar al grupo:

> "¿Qué necesitamos saber?"

Construir las respuestas:

- Datos necesarios.
- Campos obligatorios.
- Validaciones.
- Reglas.
- Restricciones.
- Resultado esperado.

---

## Paso 3 — Mejorar el requerimiento

Mostrar:

> "El sistema debe permitir registrar un usuario proporcionando nombre, correo electrónico y contraseña."

Preguntar:

> "¿Está más claro?"

Sí, pero todavía podemos agregar condiciones.

---

## Paso 4 — Reglas de negocio

Agregar:

1. Todos los campos son obligatorios.
2. El correo debe tener un formato válido.
3. El correo no puede estar registrado previamente.
4. La contraseña debe cumplir las reglas establecidas.

Explicar:

> "Ahora sabemos que no solamente debemos probar que el registro funciona. También debemos validar estas condiciones."

---

## Paso 5 — Criterios de aceptación

Podemos establecer:

- El usuario puede registrarse con datos válidos.
- El sistema rechaza campos obligatorios vacíos.
- El sistema rechaza correos inválidos.
- El sistema rechaza correos ya registrados.
- El sistema valida la contraseña.
- El sistema muestra confirmación cuando el registro es exitoso.

---

## Paso 6 — Escenarios

Preguntar:

> "Ahora que tenemos más información, ¿qué deberíamos probar?"

Construir:

1. Registro con datos válidos.
2. Nombre vacío.
3. Correo vacío.
4. Contraseña vacía.
5. Correo con formato inválido.
6. Correo ya registrado.
7. Contraseña inválida.

Aclarar:

> "En esta clase solamente estamos identificando escenarios. En la próxima clase aprenderemos a convertir estos escenarios en casos de prueba detallados."

---

# 12. Introducción al STLC

**Tiempo: 20 minutos**

Decir:

> "Hasta ahora hemos visto qué necesita saber QA antes de probar. Ahora vamos a ver cómo se organiza el proceso completo de pruebas."

## Definición

**STLC — Software Testing Life Cycle**

**Ciclo de Vida de las Pruebas de Software**

Aclarar:

> "En el ámbito profesional es habitual utilizar los términos en inglés, por eso aprenderemos ambos."

---

## Las seis fases

```text
Requirement Analysis
Análisis de requisitos
          ↓
Test Planning
Planificación de pruebas
          ↓
Test Case Development
Diseño / desarrollo de casos de prueba
          ↓
Test Environment Setup
Preparación del entorno de pruebas
          ↓
Test Execution
Ejecución de pruebas
          ↓
Test Closure
Cierre de pruebas
```

---

## 12.1 Requirement Analysis — Análisis de requisitos

QA:

- Lee los requisitos.
- Comprende la funcionalidad.
- Identifica reglas de negocio.
- Revisa criterios de aceptación.
- Detecta ambigüedades.
- Identifica riesgos.
- Determina qué debe probarse.

### Pregunta

> "¿Qué hicimos con el ejemplo de registro?"

Respuesta:

> "Analizamos el requerimiento."

---

## 12.2 Test Planning — Planificación de pruebas

Aquí definimos:

- Alcance.
- Tipos de pruebas.
- Recursos.
- Responsables.
- Ambiente.
- Datos.
- Riesgos.
- Cronograma.

Ejemplo:

> "¿Qué necesitamos para probar el registro?"

- Ambiente QA.
- Base de datos.
- Usuarios.
- Datos.
- Navegadores.
- Tiempo.

---

## 12.3 Test Case Development — Diseño / desarrollo de casos de prueba

Explicar:

> "Aquí transformamos los escenarios identificados en casos de prueba que puedan ejecutarse."

```text
Escenario
    ↓
Caso de prueba
    ↓
Precondiciones
    ↓
Datos
    ↓
Pasos
    ↓
Resultado esperado
```

Aclarar:

> "La próxima clase estará dedicada a esto."

---

## 12.4 Test Environment Setup — Preparación del entorno

Explicar:

> "Antes de ejecutar necesitamos tener disponible un ambiente adecuado."

Puede incluir:

- Aplicación.
- Base de datos.
- Configuración.
- Usuarios.
- Datos de prueba.
- Navegadores.
- Dispositivos.

Pregunta:

> "¿Qué pasa si el ambiente no está disponible?"

Respuesta:

> "No podemos ejecutar correctamente las pruebas."

---

## 12.5 Test Execution — Ejecución de pruebas

Mostrar:

```text
Caso de prueba
      ↓
Ejecutar
      ↓
Resultado real
      ↓
Comparar con esperado
      ↓
PASS / FAIL
```

Explicar:

> "Aquí ejecutamos los casos y comparamos el resultado real con el resultado esperado."

Si no coincide:

> "Tenemos un posible defecto que deberá ser registrado y gestionado."

---

## 12.6 Test Closure — Cierre de pruebas

Explicar:

> "Cuando termina el ciclo de pruebas, revisamos qué ocurrió."

Podemos analizar:

- Casos ejecutados.
- Casos aprobados.
- Casos fallidos.
- Defectos.
- Defectos pendientes.
- Riesgos.
- Resultados.

Idea:

> "No se trata solamente de ejecutar pruebas; también debemos comunicar los resultados."

---

# 13. Relacionar todo

Mostrar:

```text
REQUERIMIENTO
      ↓
REQUIREMENT ANALYSIS
Análisis de requisitos
      ↓
TEST PLANNING
Planificación
      ↓
TEST CASE DEVELOPMENT
Diseño de casos
      ↓
TEST ENVIRONMENT SETUP
Preparación del entorno
      ↓
TEST EXECUTION
Ejecución
      ↓
TEST CLOSURE
Cierre
```

Preguntar:

> "¿Dónde comienza a participar QA?"

Respuesta:

> "Desde el análisis de requisitos."

Reforzar:

> "Por eso QA no es solamente ejecutar casos de prueba."

---

# 14. Práctica

**Tiempo: 15 minutos**

## Sistema: Registro de usuarios

### Requerimiento

> El sistema debe permitir registrar un usuario proporcionando nombre, correo electrónico y contraseña.

### Reglas de negocio

- Todos los campos son obligatorios.
- El correo debe tener un formato válido.
- El correo no puede estar registrado previamente.
- La contraseña debe cumplir las reglas establecidas.

---

## Actividad 1 — Análisis

Identificar:

### 2 preguntas

Por ejemplo:

- ¿Cuál es la longitud mínima de la contraseña?
- ¿Qué mensaje debe mostrarse cuando el correo ya existe?

### 2 riesgos

Por ejemplo:

- Permitir registrar usuarios duplicados.
- Permitir contraseñas que no cumplen las reglas de seguridad.

---

## Actividad 2 — Escenarios

Crear **5 escenarios de prueba**.

---

## Actividad 3 — Caso de prueba

Elegir uno de los escenarios y elaborar:

- ID.
- Título.
- Precondición.
- Datos.
- Pasos.
- Resultado esperado.

### Importante

No exigir todavía perfección en la estructura del caso de prueba.

La finalidad de esta práctica es comprobar que el estudiante entiende:

> **Requerimiento → análisis → escenarios → caso de prueba.**

---

# 15. Revisión rápida de la práctica

**Tiempo incluido dentro de los 15 minutos de práctica**

Seleccionar 1 o 2 respuestas.

Preguntar:

> "¿Qué escenario eligieron?"

> "¿Cuál es el resultado esperado?"

> "¿Qué dato utilizarían?"

> "¿Qué pasaría si el resultado real es diferente?"

Conectar:

> "Si el resultado real no coincide con el esperado, podemos tener un defecto."

---

# 16. Cierre

**Tiempo: 4 minutos**

Realizar preguntas rápidas:

1. ¿Qué es un requerimiento?
2. ¿Cuál es la diferencia entre funcional y no funcional?
3. ¿Qué es una regla de negocio?
4. ¿Qué son los criterios de aceptación?
5. ¿Qué significa STLC?
6. ¿Cuál es la primera fase del STLC?

## Mensaje final

> "Hoy vimos que el trabajo de QA comienza mucho antes de ejecutar una prueba."

> "Primero necesitamos entender qué debe hacer el sistema, identificar las condiciones que debe cumplir y detectar cualquier duda o ambigüedad."

> "A partir de ahí podemos diseñar nuestras pruebas y posteriormente ejecutarlas."

### Concepto para recordar

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

---

# 17. Conexión con la Clase 3

Cerrar diciendo:

> "Hoy identificamos qué debemos probar."

> "En la siguiente clase vamos a aprender cómo convertir esos escenarios en casos de prueba bien definidos."

## Clase 3 — Escenarios y casos de prueba

Trabajaremos:

- Qué es un escenario.
- Qué es un caso de prueba.
- Estructura de un caso de prueba.
- Precondiciones.
- Datos de prueba.
- Pasos.
- Resultado esperado.
- Casos positivos y negativos.
- Ejercicios prácticos.