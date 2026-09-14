# Clase 1 — Introducción al Aseguramiento de Calidad y Pruebas Manuales

---

## DIAPOSITIVA 1 — PORTADA

### Texto en pantalla

**ESTRATEGIAS DE ASEGURAMIENTO DE CALIDAD**

### Clase 1

**Introducción al aseguramiento de calidad y pruebas manuales**

### Diseño visual

Fondo claro con un panel lateral azul oscuro.

En la parte derecha, un flujo visual sencillo:

**Requisito → Prueba → Calidad**

No utilizar fotografías genéricas. El elemento visual debe representar directamente el tema de QA.

### Notas del docente

Dar la bienvenida y presentar el propósito general del módulo.

Explicar que durante el curso no solamente se aprenderá a ejecutar pruebas, sino a **pensar como QA**.

Comentar que inicialmente se trabajará con conceptos fundamentales y pruebas manuales. Las herramientas de automatización se introducirán posteriormente, cuando ya exista una base sólida de testing.

### Mensaje clave

> Antes de aprender herramientas, necesitamos aprender a pensar en calidad.

---

# DIAPOSITIVA 2 — PREGUNTA DE APERTURA

## ¿Cómo sabemos que un software tiene calidad?

### Texto principal

> **¿Que una aplicación funcione significa que tiene calidad?**

### Diseño visual

Una pregunta grande en el centro.

Debajo, tres tarjetas:

| FUNCIONA | ES USABLE | ES CONFIABLE |
|---|---|---|
| ¿Hace lo que debe? | ¿El usuario puede utilizarlo fácilmente? | ¿Se comporta correctamente? |

### Notas del docente

No responder inmediatamente.

Preguntar a los estudiantes:

- ¿Qué significa para ustedes que un software tenga calidad?
- ¿Alguna vez utilizaron una aplicación que funcionaba pero era mala?
- ¿Qué problemas recuerdan?

Buscar respuestas como:

- era lenta;
- se cerraba;
- tenía errores;
- era difícil de utilizar;
- mostraba mensajes confusos;
- perdía información.

Después introducir la idea:

**“Funcionar” es solamente una parte de la calidad.**

### Interacción

Dejar que algunos estudiantes respondan antes de continuar.

### Mensaje clave

> La calidad de software tiene más dimensiones que simplemente funcionar.

---

# DIAPOSITIVA 3 — OBJETIVO DE LA CLASE

## ¿Qué vamos a aprender?

### Elemento central

**PENSAR COMO QA**

### Cuatro objetivos visuales

**01 — ENTENDER**  
Qué significa calidad de software.

**02 — DIFERENCIAR**  
QA, QC y Testing.

**03 — ANALIZAR**  
Riesgos, requisitos y escenarios.

**04 — APLICAR**  
Una mirada QA sobre un sistema real.

### Diseño visual

Colocar **PENSAR COMO QA** en el centro.

Los cuatro objetivos alrededor como tarjetas conectadas.

### Notas del docente

Explicar que el objetivo de esta primera clase no es convertir al estudiante en experto en herramientas.

Primero necesitamos construir una forma de pensar.

Un QA debe preguntarse:

- ¿Qué podría salir mal?
- ¿Qué debería ocurrir?
- ¿Qué pasa si el usuario hace algo diferente?
- ¿Qué información necesitamos para probar?
- ¿Qué riesgos existen?

### Mensaje clave

> QA comienza con preguntas, no con herramientas.

---

# DIAPOSITIVA 4 — RUTA DE LA CLASE

## ¿Cómo avanzaremos?

### Diseño visual

Roadmap horizontal:

**01 Calidad**  
↓  
**02 QA / QC / Testing**  
↓  
**03 Rol del QA**  
↓  
**04 Requisitos y defectos**  
↓  
**05 Mentalidad y riesgo**  
↓  
**06 Pruebas manuales**  
↓  
**07 Ejemplo guiado**  
↓  
**08 Actividad**

### Notas del docente

Presentar brevemente el recorrido.

Explicar que primero construiremos la base conceptual.

Después veremos cómo piensa un QA.

Finalmente aplicaremos los conceptos en una aplicación real mediante un ejemplo guiado.

No explicar todavía cada punto en profundidad.

### Mensaje clave

> Primero entendemos los conceptos; después los aplicamos.

---

# DIAPOSITIVA 5 — ¿QUÉ ES CALIDAD?

## ¿Qué significa calidad de software?

### Texto principal

> **La calidad no se reduce a “que funcione”.**

### Diseño visual

Colocar un bloque central:

**SOFTWARE**

Alrededor:

**FUNCIONALIDAD**  
Hace lo que debe hacer.

**USABILIDAD**  
Es comprensible y fácil de utilizar.

**CONFIABILIDAD**  
Se comporta correctamente y de forma estable.

**RENDIMIENTO**  
Responde dentro de tiempos aceptables.

Visual:

```text
                  FUNCIONALIDAD
                       │
                       ▼
                 ┌───────────┐
                 │ SOFTWARE  │
                 └───────────┘
                  ▲    ▲    ▲
                  │    │    │
             USABILIDAD │ CONFIABILIDAD
                        │
                   RENDIMIENTO
```

### Notas del docente

Explicar que diferentes personas pueden evaluar la calidad desde perspectivas diferentes.

Para un usuario:

> “La aplicación es fácil de utilizar.”

Para negocio:

> “Cumple lo que necesitamos.”

Para desarrollo:

> “El sistema funciona correctamente y puede mantenerse.”

Para QA:

> “Necesitamos comprobar diferentes condiciones y riesgos.”

Aclarar que las dimensiones mostradas son ejemplos y que la calidad puede involucrar otros atributos.

### Pregunta

> Si una aplicación funciona perfectamente pero tarda 30 segundos en responder, ¿tiene calidad?

Usar las respuestas para introducir rendimiento.

### Mensaje clave

> Calidad significa cumplir las necesidades y expectativas relevantes, no solamente ejecutar correctamente.

---

# DIAPOSITIVA 6 — ¿FUNCIONAR SIGNIFICA TENER CALIDAD?

## Un sistema puede funcionar… y aun así tener problemas.

### Diseño visual

Dividir la pantalla en dos.

### 🟢 FUNCIONA

- El botón responde.
- El registro se guarda.
- La pantalla carga.

### 🔴 PERO…

- Es demasiado lento.
- El mensaje es confuso.
- Permite datos incorrectos.
- No funciona correctamente en otro entorno.

En la parte inferior:

> **Funcionar ≠ tener calidad**

### Notas del docente

Utilizar un ejemplo cotidiano.

Supongamos una aplicación bancaria.

El botón **“Transferir”** funciona.

La transferencia se realiza.

Pero imaginemos que:

- tarda demasiado;
- permite ingresar un monto negativo;
- no informa claramente el resultado;
- funciona en Chrome pero falla en otro navegador.

La funcionalidad principal existe, pero todavía tenemos problemas de calidad.

### Pregunta

> ¿Cuál de estos problemas debería detectar un QA?

Respuesta esperada:

**Todos pueden ser relevantes**, dependiendo del requisito y del riesgo.

### Mensaje clave

> Una prueba exitosa de una funcionalidad no significa que todo el sistema tenga calidad.

---

# DIAPOSITIVA 7 — DIFERENTES PERSPECTIVAS

## ¿Quién decide si algo tiene calidad?

### Diseño visual

Mostrar cuatro perspectivas:

```text
                 CALIDAD
                    │
       ┌────────────┼────────────┐
       │            │            │
     USUARIO      NEGOCIO     DESARROLLO
       │            │            │
    Facilidad    Requisitos    Correcto
    de uso       cumplidos     y mantenible

                    +
                   
                    QA
                    │
              Riesgos y
              evidencias
```

### Notas del docente

Explicar que calidad no pertenece exclusivamente al QA.

Cada participante puede observar diferentes aspectos.

**Usuario:**  
¿Puedo realizar mi tarea?

**Negocio:**  
¿El sistema cumple el objetivo?

**Desarrollo:**  
¿El software funciona y puede mantenerse?

**QA:**  
¿Qué riesgos existen y qué evidencia tenemos de que el sistema cumple lo esperado?

Aclarar que el QA no “es dueño” de la calidad.

### Mensaje clave

> QA ayuda al equipo a obtener información sobre la calidad.

---

# DIAPOSITIVA 8 — UNA IDEA IMPORTANTE

## QA no significa solamente buscar bugs

### Diseño visual

Colocar un gran contraste:

```text
          ❌ IDEA REDUCIDA

       QA = BUSCAR BUGS


          ✅ IDEA CORRECTA

       QA = PREVENIR
       + ANALIZAR
       + PROBAR
       + COMUNICAR
       + EVALUAR RIESGOS
```

### Notas del docente

Esta es una idea importante para establecer desde el inicio.

Explicar que encontrar defectos es una parte del trabajo, pero QA también participa en:

- análisis de requisitos;
- identificación de riesgos;
- definición de escenarios;
- preparación de datos;
- planificación de pruebas;
- ejecución;
- documentación;
- comunicación de resultados.

Un QA puede aportar valor **antes de que exista código**.

### Ejemplo

Si un requisito dice:

> “El usuario debe poder registrarse.”

Un QA puede preguntar:

- ¿Qué datos son obligatorios?
- ¿Qué ocurre si el correo ya existe?
- ¿Qué formato debe tener el correo?
- ¿Qué contraseña se acepta?
- ¿Qué mensaje verá el usuario?

### Mensaje clave

> Un buen QA intenta descubrir problemas antes de que lleguen al usuario.

---

# DIAPOSITIVA 9 — ¿POR QUÉ NECESITAMOS QA?

## Porque el software puede fallar de muchas formas.

### Diseño visual

Mostrar diferentes puntos de riesgo alrededor de una aplicación:

```text
                 REQUISITOS
                     ↓
                 DESARROLLO
                     ↓
        ┌─────────────────────────┐
        │       APLICACIÓN        │
        └─────────────────────────┘
          ↓       ↓       ↓
       DATOS    USUARIO  ENTORNO
          ↓       ↓       ↓
       ERRORES  CONFUSIÓN  FALLAS
```

Al lado:

**¿Qué puede salir mal?**

- Requisitos incorrectos.
- Datos inesperados.
- Errores de implementación.
- Problemas de integración.
- Problemas de rendimiento.
- Problemas de usabilidad.

### Notas del docente

Explicar que el software es un sistema complejo.

No todos los problemas son evidentes.

Un sistema puede funcionar correctamente en el escenario que desarrolló el programador y fallar cuando:

- el usuario introduce otro dato;
- utiliza otra secuencia;
- trabaja con muchos registros;
- utiliza otro navegador;
- realiza una acción inesperada.

Aquí introducir el concepto de **variabilidad**.

### Pregunta

> ¿Podemos asumir que los usuarios siempre harán lo que nosotros esperamos?

La respuesta esperada es:

**No.**

### Mensaje clave

> El QA ayuda a descubrir comportamientos inesperados antes de que se conviertan en problemas para el usuario.

---

# DIAPOSITIVA 10 — ¿QUÉ APORTA QA?

## QA aporta información para tomar mejores decisiones.

### Diseño visual

Flujo:

```text
REQUISITOS
     ↓
 ANALIZAR
     ↓
 IDENTIFICAR RIESGOS
     ↓
 DISEÑAR PRUEBAS
     ↓
 EJECUTAR
     ↓
 OBTENER EVIDENCIA
     ↓
 COMUNICAR
     ↓
 MEJORAR LA CALIDAD
```

### Elemento destacado

> **QA transforma preguntas en evidencia.**

### Notas del docente

Explicar cada paso de forma sencilla.

**Analizar:**  
Entender qué debe hacer el sistema.

**Identificar riesgos:**  
Preguntarnos qué podría fallar y qué sería importante para el usuario o negocio.

**Diseñar pruebas:**  
Definir cómo vamos a comprobar el comportamiento.

**Ejecutar:**  
Realizar las pruebas.

**Obtener evidencia:**  
Registrar resultados, datos, capturas o información relevante.

**Comunicar:**  
Informar hallazgos de forma clara.

**Mejorar:**  
El equipo utiliza esa información para tomar decisiones.

### Transición

Concluir:

> Ahora que entendemos por qué necesitamos QA, debemos diferenciar tres conceptos que suelen confundirse: **QA, QC y Testing**.

Esto introduce directamente la siguiente sección del Markdown.

### Mensaje clave

> El valor del QA no está solamente en encontrar errores, sino en generar información útil sobre la calidad.