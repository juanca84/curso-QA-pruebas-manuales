# MÓDULO: ESTRATEGIAS DE ASEGURAMIENTO DE CALIDAD Y PRUEBAS MANUALES

# CLASE 1: INTRODUCCIÓN AL ASEGURAMIENTO DE CALIDAD Y PRUEBAS DE SOFTWARE

---

# 1. INFORMACIÓN GENERAL

## Objetivo de la clase

Al finalizar la clase, el estudiante será capaz de comprender los fundamentos de la calidad de software, el aseguramiento de calidad y las pruebas de software, identificando el rol del QA y desarrollando una primera aproximación a la mentalidad necesaria para analizar y probar una aplicación.

---

## Resultados esperados

Al finalizar la clase, el estudiante será capaz de:

- Comprender qué significa calidad en el contexto del software.
- Diferenciar los conceptos de QA, QC y Testing.
- Comprender el propósito de las pruebas de software.
- Identificar el rol del QA dentro de un equipo de desarrollo.
- Comprender que la calidad es responsabilidad de todo el equipo.
- Identificar conceptos básicos relacionados con requisitos, defectos y resultados de prueba.
- Desarrollar una primera aproximación a la mentalidad QA.
- Identificar situaciones y escenarios básicos que deberían probarse.
- Comprender la importancia del riesgo y la estrategia en las pruebas.

---

# 2. ESTRUCTURA DE LA CLASE

La primera clase está orientada principalmente a construir una base conceptual.

Todavía no trabajaremos en profundidad con:

- Casos de prueba formales.
- Reporte de defectos.
- Herramientas de gestión.
- Automatización.
- Técnicas avanzadas de diseño de pruebas.

Primero debemos responder una serie de preguntas fundamentales:

```text
¿Qué es calidad?
        ↓
¿Por qué necesitamos QA?
        ↓
¿Qué es Testing?
        ↓
¿Qué hace un QA?
        ↓
¿Cómo piensa un QA?
        ↓
¿Qué debemos probar?
```

---

# 3. ¿QUÉ ES CALIDAD DE SOFTWARE?

## Pregunta inicial

Comenzar la clase preguntando:

> **¿Cómo sabemos que un software tiene calidad?**

Permitir que los estudiantes respondan libremente.

Probablemente aparecerán respuestas como:

- No tiene errores.
- Funciona correctamente.
- Es rápido.
- Es fácil de utilizar.
- No se cae.
- Cumple lo que necesita el usuario.
- Es seguro.

Todas estas respuestas están relacionadas con la calidad.

Sin embargo, debemos comprender que:

> **La calidad no significa únicamente ausencia de errores.**

---

## Definición sencilla

Podemos entender la calidad de software como:

> **El grado en que un software cumple con los requisitos establecidos y satisface las necesidades de sus usuarios.**

Esta definición nos presenta dos elementos importantes:

1. Cumplir con los requisitos.
2. Satisfacer las necesidades del usuario o negocio.

---

## Ejemplo

Imaginemos una aplicación bancaria.

La aplicación:

- No presenta errores visibles.
- Los botones funcionan.
- Los datos se muestran.
- Las operaciones se completan.

Sin embargo:

- Tarda demasiado en mostrar información.
- Es difícil encontrar una transferencia.
- No funciona correctamente en dispositivos móviles.
- No protege adecuadamente la información.

Preguntar:

> **¿Podemos decir que la aplicación tiene buena calidad?**

No necesariamente.

Aunque técnicamente funcione, puede presentar problemas relacionados con:

- Rendimiento.
- Usabilidad.
- Seguridad.
- Compatibilidad.
- Experiencia del usuario.

---

## Características de un software de calidad

Un software puede evaluarse desde diferentes perspectivas.

### Funcionalidad

El sistema debe hacer lo que debe hacer.

Ejemplo:

Una tienda virtual debe permitir:

- Buscar productos.
- Agregar productos al carrito.
- Realizar una compra.

---

### Confiabilidad

El sistema debe funcionar correctamente de manera consistente.

No debería funcionar correctamente algunas veces y fallar otras veces bajo las mismas condiciones.

---

### Usabilidad

El sistema debe ser comprensible y fácil de utilizar.

Por ejemplo:

- Etiquetas claras.
- Mensajes comprensibles.
- Formularios fáciles de completar.
- Navegación sencilla.

---

### Seguridad

El sistema debe proteger:

- Usuarios.
- Datos.
- Operaciones.
- Información sensible.

---

### Rendimiento

El sistema debe responder en tiempos razonables.

---

### Compatibilidad

El sistema debe funcionar correctamente en los entornos esperados.

Por ejemplo:

- Navegadores.
- Dispositivos.
- Sistemas operativos.

---

## Idea principal

> **La calidad puede ser evaluada desde diferentes perspectivas. Un software que funciona no necesariamente es un software de calidad.**

---

# 4. ¿POR QUÉ NECESITAMOS QA?

Imaginemos una tienda virtual.

La aplicación permite:

- Registrarse.
- Iniciar sesión.
- Buscar productos.
- Agregar productos al carrito.
- Realizar pagos.

Sin actividades de calidad podrían aparecer problemas como:

- Permitir cantidades negativas.
- Calcular incorrectamente un total.
- Permitir compras sin pago.
- Mostrar información de otro usuario.
- Fallar en determinados navegadores.
- Dejar de responder ante muchos usuarios.

Estos problemas pueden afectar:

- Usuarios.
- Negocio.
- Información.
- Confianza.
- Costos.

Por esta razón necesitamos actividades que nos permitan:

- Prevenir problemas.
- Detectar problemas.
- Identificar riesgos.
- Verificar requisitos.
- Evaluar funcionalidades.
- Mejorar continuamente.

---

# 5. QA, QC Y TESTING

Estos conceptos están relacionados, pero no son exactamente lo mismo.

---

## QA — Quality Assurance

QA significa:

> **Quality Assurance**

En español:

> **Aseguramiento de la Calidad**

QA tiene un enfoque amplio y preventivo.

Busca ayudar a que el proceso y el producto tengan la calidad esperada.

Puede incluir actividades como:

- Revisar requisitos.
- Identificar riesgos.
- Realizar preguntas.
- Planificar pruebas.
- Definir estrategias.
- Promover buenas prácticas.
- Mejorar procesos.
- Evaluar el producto.

La idea principal es:

> **QA no solamente busca encontrar problemas. También busca prevenirlos.**

---

## QC — Quality Control

QC significa:

> **Quality Control**

En español:

> **Control de Calidad**

Su enfoque está más relacionado con evaluar e inspeccionar el producto.

Pregunta principal:

> **¿El producto cumple con lo esperado?**

---

## Testing

Testing consiste en realizar actividades para evaluar el software y comparar su comportamiento con lo esperado.

Pregunta principal:

> **¿El sistema funciona como esperamos?**

Ejemplo:

### Esperado

> El usuario puede iniciar sesión con credenciales correctas.

### Obtenido

> El sistema muestra un mensaje de error.

Existe una diferencia entre:

```text
Lo esperado
     ↓
Comparar
     ↓
Lo obtenido
```

Esta diferencia debe analizarse.

---

## Comparación

| Concepto | Enfoque principal |
|---|---|
| QA | Prevenir y asegurar la calidad |
| QC | Evaluar y controlar el producto |
| Testing | Probar y evaluar el comportamiento del software |

---

# 6. LA CALIDAD ES RESPONSABILIDAD DE TODO EL EQUIPO

Es importante eliminar una idea equivocada:

> **El QA es el único responsable de la calidad.**

Esto no es correcto.

La calidad debe ser una responsabilidad compartida.

---

## Responsables del negocio

Ayudan a:

- Definir necesidades.
- Establecer prioridades.
- Validar que el producto aporte valor.

---

## Analistas

Ayudan a:

- Comprender necesidades.
- Definir requisitos.
- Reducir ambigüedades.

---

## Desarrolladores

Deben:

- Implementar correctamente.
- Revisar su trabajo.
- Realizar pruebas necesarias.
- Corregir problemas.

---

## QA

Ayuda a:

- Analizar requisitos.
- Identificar riesgos.
- Preparar pruebas.
- Ejecutar pruebas.
- Detectar problemas.
- Comunicar información sobre la calidad.

---

## Otros miembros del equipo

También pueden contribuir a la calidad mediante:

- Diseño.
- Infraestructura.
- Seguridad.
- Despliegues.
- Validación con usuarios.

---

## Idea principal

> **QA no es el dueño absoluto de la calidad. QA ayuda al equipo a construir, verificar y mejorar la calidad del producto.**

---

# 7. EL ROL DEL QA DURANTE EL DESARROLLO

Un QA no debería participar únicamente cuando la aplicación está terminada.

La calidad debe considerarse durante diferentes etapas.

```text
Necesidad
    ↓
Análisis
    ↓
Diseño
    ↓
Desarrollo
    ↓
Pruebas
    ↓
Despliegue
    ↓
Mantenimiento
```

---

## Durante el análisis

Un QA puede:

- Revisar requisitos.
- Identificar dudas.
- Detectar ambigüedades.
- Hacer preguntas.
- Identificar riesgos.

---

## Durante el diseño

Puede:

- Analizar escenarios.
- Considerar comportamientos especiales.
- Identificar posibles problemas.

---

## Durante el desarrollo

Puede:

- Preparar pruebas.
- Preparar datos.
- Revisar funcionalidades disponibles.
- Resolver dudas con el equipo.

---

## Durante las pruebas

Puede:

- Ejecutar pruebas.
- Registrar resultados.
- Identificar problemas.
- Comunicar defectos.
- Verificar correcciones.

---

## Durante el despliegue y mantenimiento

Puede:

- Verificar funcionalidades importantes.
- Validar correcciones.
- Ejecutar pruebas de regresión.
- Analizar nuevos riesgos.

---

## Idea principal

> **La calidad es una actividad continua y no una etapa final del desarrollo.**

---

# 8. ¿POR QUÉ ES IMPORTANTE PROBAR TEMPRANO?

Encontrar un problema temprano normalmente reduce el impacto de corregirlo.

---

## Problema encontrado en requisitos

Puede requerir:

- Aclarar una necesidad.
- Modificar una definición.
- Resolver una ambigüedad.

---

## Problema encontrado durante desarrollo

Puede requerir:

- Modificar código.
- Revisar componentes.
- Realizar nuevas pruebas.

---

## Problema encontrado en producción

Puede requerir:

- Investigación urgente.
- Corrección.
- Nuevo despliegue.
- Comunicación con usuarios.
- Posibles pérdidas.

---

Podemos introducir brevemente el concepto:

# Shift Left Testing

Significa realizar actividades relacionadas con calidad y pruebas lo más temprano posible.

No profundizaremos todavía.

Lo importante es comprender:

> **QA no debería esperar al final para comenzar a pensar en las pruebas.**

---

# 9. REQUISITOS Y PRUEBAS

Las pruebas necesitan una referencia.

Necesitamos saber:

> **¿Qué debería hacer el sistema?**

Esa información normalmente proviene de los requisitos.

---

## ¿Qué es un requisito?

Un requisito representa una necesidad o condición que el sistema debe cumplir.

Ejemplo:

> El usuario debe poder recuperar su contraseña.

---

## Requisitos funcionales

Describen:

> **Qué debe hacer el sistema.**

Ejemplos:

- El usuario puede iniciar sesión.
- El usuario puede registrarse.
- El administrador puede eliminar usuarios.

---

## Requisitos no funcionales

Describen características o restricciones del sistema.

Ejemplos:

- El sistema debe responder en menos de tres segundos.
- La información debe estar protegida.
- El sistema debe funcionar en determinados navegadores.

---

## Ejemplo

### Funcional

> El usuario puede buscar productos.

### No funcional

> La búsqueda debe mostrar resultados en menos de dos segundos.

---

## Idea principal

> **Los requisitos nos ayudan a comprender qué debemos verificar y qué comportamiento esperamos del sistema.**

---

# 10. ERROR, DEFECTO Y FALLO

Debemos conocer algunos conceptos básicos.

---

## Error

Una equivocación humana.

Ejemplo:

El requisito indica:

> Los usuarios con 18 años pueden registrarse.

Una persona interpreta:

> Solo los usuarios mayores a 18 años pueden registrarse.

---

## Defecto

El problema queda incorporado en el producto.

Ejemplo:

```text
edad > 18
```

Cuando debería ser:

```text
edad >= 18
```

---

## Fallo

El defecto produce un comportamiento incorrecto durante la ejecución.

Ejemplo:

Usuario:

```text
Edad: 18
```

Resultado:

```text
Registro rechazado
```

Cuando debería permitirse.

---

## Relación

```text
Error humano
      ↓
Defecto
      ↓
Fallo durante la ejecución
```

---

## Bug

En el entorno laboral también es común escuchar:

- Bug.
- Issue.
- Problema.
- Incidencia.

Para este curso podemos utilizar inicialmente:

> **Bug o defecto: comportamiento que no cumple con lo esperado.**

---

## Importante

No todos los problemas provienen del código.

También pueden originarse en:

- Requisitos ambiguos.
- Diseño.
- Configuración.
- Datos.
- Infraestructura.
- Integraciones.

---

# 11. ¿QUÉ SON LAS PRUEBAS DE SOFTWARE?

Las pruebas de software son actividades realizadas para evaluar el sistema y verificar su comportamiento.

Nos ayudan a responder preguntas como:

- ¿Funciona correctamente?
- ¿Cumple los requisitos?
- ¿Qué ocurre con datos inválidos?
- ¿Qué ocurre en situaciones especiales?
- ¿El comportamiento es el esperado?

---

## Prueba positiva

Verifica el sistema utilizando condiciones válidas.

Ejemplo:

```text
Usuario válido
Contraseña válida
```

Resultado esperado:

> El usuario puede iniciar sesión.

---

## Prueba negativa

Verifica cómo responde el sistema ante condiciones inválidas.

Ejemplo:

```text
Usuario inválido
```

Resultado esperado:

> El sistema rechaza el acceso y muestra un mensaje adecuado.

---

## Idea principal

> **No solamente debemos verificar lo que debería funcionar. También debemos analizar situaciones donde el sistema debería rechazar, validar o manejar correctamente una condición.**

---

# 12. RESULTADO ESPERADO Y RESULTADO OBTENIDO

Este concepto es fundamental.

---

## Resultado esperado

Representa lo que debería ocurrir.

Ejemplo:

> El usuario debe acceder al sistema utilizando credenciales válidas.

---

## Resultado obtenido

Representa lo que realmente ocurrió.

Ejemplo:

> El sistema muestra una pantalla en blanco.

---

## Comparación

```text
Acción
   ↓
Resultado esperado
   ↓
Ejecutar
   ↓
Resultado obtenido
   ↓
Comparar
```

Si existe una diferencia, debemos investigarla.

---

# 13. DATOS Y AMBIENTE DE PRUEBA

Para realizar pruebas necesitamos condiciones adecuadas.

---

## Datos de prueba

Son los datos que utilizamos para realizar una prueba.

Ejemplos:

### Datos válidos

```text
usuario@email.com
Password123
```

### Datos inválidos

```text
correo_incorrecto
contraseña vacía
usuario inexistente
```

---

## Ambiente de prueba

El sistema puede comportarse de manera diferente dependiendo del ambiente.

Ejemplos:

- Desarrollo.
- Testing.
- QA.
- Staging.
- Producción.

Por ahora solamente debemos comprender:

> **Las condiciones donde realizamos una prueba pueden afectar el resultado.**

---

# 14. LA MENTALIDAD QA

Esta es una de las partes más importantes de la clase.

Utilizar una aplicación:

> **No es lo mismo que probar una aplicación.**

---

## Un usuario piensa

> ¿Cómo utilizo esta funcionalidad?

---

## Un desarrollador puede pensar

> ¿Cómo hago que esto funcione?

---

## Un QA debe pensar

> ¿Cómo debería funcionar?

> ¿Qué puede salir mal?

> ¿Qué no está claro?

> ¿Qué escenarios no estamos considerando?

> ¿Qué ocurre en situaciones especiales?

---

# 15. EJEMPLO DE MENTALIDAD QA

Tenemos un formulario:

```text
Nombre

Correo

Contraseña

[ Registrarse ]
```

Un usuario podría simplemente completar:

- Nombre válido.
- Correo válido.
- Contraseña válida.

Y registrarse.

---

Un QA comienza a realizar preguntas.

---

## Nombre

- ¿Es obligatorio?
- ¿Tiene longitud máxima?
- ¿Acepta números?
- ¿Acepta caracteres especiales?

---

## Correo

- ¿Debe ser único?
- ¿Valida formato?
- ¿Acepta espacios?
- ¿Acepta mayúsculas?

---

## Contraseña

- ¿Tiene longitud mínima?
- ¿Tiene restricciones?
- ¿Puede estar vacía?
- ¿Se muestra protegida?

---

## Botón

- ¿Se puede presionar varias veces?
- ¿Qué ocurre mientras procesa?
- ¿Existe un mensaje de éxito?

---

## Idea principal

> **Un QA no debe asumir. Debe analizar, preguntar y verificar.**

---

# 16. ESCENARIOS Y CASOS DE PRUEBA

En esta clase solamente introduciremos estos conceptos.

---

## Escenario de prueba

Representa una situación general que queremos verificar.

Ejemplo:

> Verificar el inicio de sesión.

---

## Caso de prueba

Describe de manera más específica:

- Qué se prueba.
- Datos.
- Pasos.
- Resultado esperado.
- Resultado obtenido.

Ejemplo:

| Campo | Información |
|---|---|
| ID | TC-001 |
| Nombre | Inicio de sesión exitoso |
| Datos | Usuario válido |
| Resultado esperado | Acceso al sistema |

No profundizaremos todavía.

Este tema será desarrollado en clases posteriores.

---

# 17. NO PODEMOS PROBAR TODO

Este es uno de los principios más importantes del testing.

Pregunta:

> Si un campo acepta números del 1 al 1.000.000, ¿debemos probar todos los números?

No.

Existen demasiadas:

- Combinaciones.
- Entradas.
- Situaciones.
- Dispositivos.
- Configuraciones.

Por eso debemos seleccionar pruebas de manera inteligente.

---

# 18. RIESGO Y ESTRATEGIA

Las pruebas requieren decisiones.

Debemos pensar:

- ¿Qué probar?
- ¿Cómo probar?
- ¿Qué es más importante?
- ¿Dónde existe mayor riesgo?

---

## Ejemplo

En una tienda virtual:

| Funcionalidad | Riesgo aproximado |
|---|---|
| Cambiar color de botón | Bajo |
| Editar perfil | Medio |
| Inicio de sesión | Alto |
| Pago | Muy alto |

---

Pregunta:

> ¿Dónde deberíamos invertir mayor esfuerzo?

Normalmente en las funcionalidades con mayor riesgo.

---

## Idea principal

> **No todas las funcionalidades requieren el mismo nivel de esfuerzo de prueba.**

---

# 19. PRINCIPIOS FUNDAMENTALES DE TESTING

Introducción general.

---

## Las pruebas muestran la presencia de defectos

Las pruebas pueden encontrar problemas.

Pero no pueden demostrar que el sistema no tiene ninguno.

Ejemplo:

```text
100 pruebas exitosas
```

No significa:

```text
El sistema no tiene defectos
```

Significa:

> No encontramos problemas durante las pruebas realizadas.

---

## No podemos probar todo

Debemos seleccionar pruebas estratégicamente.

---

## Probar temprano ayuda

Encontrar problemas temprano puede reducir el impacto de corregirlos.

---

## Los defectos pueden concentrarse

Algunas áreas pueden presentar más problemas que otras.

---

## Repetir siempre las mismas pruebas puede ser insuficiente

Debemos:

- Explorar.
- Cambiar datos.
- Considerar nuevos escenarios.

---

## Las pruebas dependen del contexto

No se prueba igual:

- Una aplicación bancaria.
- Un videojuego.
- Un sistema médico.
- Una tienda virtual.

---

## Ausencia de defectos no significa éxito

Un sistema puede funcionar técnicamente.

Pero no satisfacer la necesidad del usuario.

---

# 20. HABILIDADES IMPORTANTES PARA UN QA

---

## Atención al detalle

Observar:

- Mensajes.
- Datos.
- Comportamientos.
- Cambios.

---

## Pensamiento crítico

Preguntar:

> ¿Qué ocurre si...?

---

## Curiosidad

Explorar situaciones diferentes.

---

## Comunicación

Explicar claramente:

- Qué ocurrió.
- Cómo ocurrió.
- Qué se esperaba.

---

## Organización

Mantener información sobre:

- Pruebas.
- Resultados.
- Evidencias.
- Problemas.

---

## Comprensión del negocio

Entender:

> ¿Para qué existe esta funcionalidad?

---

# 21. COMUNICACIÓN Y ACTITUD DEL QA

Un QA no debe buscar culpables.

El objetivo es mejorar el producto.

---

## Comunicación deficiente

> El Login está mal.

No sabemos:

- Qué ocurrió.
- Cómo ocurrió.
- Qué datos se utilizaron.
- Qué se esperaba.

---

## Mejor comunicación

> Al intentar iniciar sesión con credenciales incorrectas, el sistema muestra una pantalla en blanco en lugar de un mensaje indicando que las credenciales son inválidas.

---

## Actitud profesional

En lugar de decir:

> El desarrollador hizo mal esto.

Podemos comunicar:

> La funcionalidad presenta un comportamiento diferente al esperado.

---

## Idea principal

> **QA trabaja con el equipo para mejorar el producto, no para encontrar culpables.**

---

# 22. PRUEBAS MANUALES

Las pruebas manuales son realizadas principalmente por una persona que interactúa con el sistema y evalúa su comportamiento.

Ejemplo:

```text
1. Abrir aplicación.
2. Ingresar usuario.
3. Ingresar contraseña.
4. Presionar Login.
5. Verificar resultado.
```

---

## Pruebas manuales no significa simplemente hacer clic

Requieren:

- Análisis.
- Observación.
- Pensamiento crítico.
- Curiosidad.
- Comprensión del negocio.
- Identificación de riesgos.
- Comunicación.

---

# 23. QA MANUAL Y AUTOMATION

Introducción breve.

---

## QA Manual

Una persona ejecuta y analiza las pruebas.

Puede ser especialmente útil para:

- Exploración.
- Usabilidad.
- Situaciones nuevas.
- Evaluación humana.

---

## Automation

Utiliza herramientas y código para ejecutar determinadas pruebas automáticamente.

---

## Idea principal

> **La automatización no reemplaza completamente las pruebas manuales.**

Y:

> **No todo debe automatizarse.**

Este tema será desarrollado posteriormente.

---

# 24. VERIFICACIÓN Y VALIDACIÓN

Introducción básica.

---

## Verificación

Pregunta:

> ¿Estamos construyendo correctamente el producto?

---

## Validación

Pregunta:

> ¿Estamos construyendo el producto correcto?

---

## Ejemplo

Podemos construir correctamente una funcionalidad.

Pero:

> El requisito inicial puede no resolver la necesidad real.

Por eso debemos considerar tanto:

- Construir correctamente.
- Construir lo correcto.

---

# 25. EJEMPLO GUIADO: PENSANDO COMO UN QA

## Objetivo

El objetivo no es crear todavía casos de prueba formales.

El objetivo es demostrar cómo cambia nuestra forma de pensar.

```text
Usuario
   ↓
Utiliza

QA
   ↓
Analiza
   ↓
Pregunta
   ↓
Prueba
```

---

# 26. APLICACIÓN DE PRUEBA

Utilizaremos:

**SauceDemo**

Para esta primera clase utilizaremos únicamente:

# LOGIN

---

## Credenciales

```text
Usuario: standard_user
Contraseña: secret_sauce
```

---

# 27. ETAPA 1: PENSAR COMO USUARIO

Mostrar la pantalla.

Preguntar:

> ¿Qué harían como usuarios?

Probablemente:

1. Ingresar usuario.
2. Ingresar contraseña.
3. Presionar Login.

Realizar el Login.

---

## Pregunta

> ¿Funcionó?

Sí.

---

## Pregunta clave

> ¿Eso significa que terminamos de probar el Login?

No.

---

# 28. ETAPA 2: PENSAR COMO QA

Preguntar:

> **¿Qué más podríamos probar?**

Permitir que los estudiantes propongan ideas.

Después guiarlos.

---

## Escenario 1: Login correcto

```text
Usuario válido
Contraseña válida
```

Resultado esperado:

> Acceso al sistema.

---

## Escenario 2: Usuario incorrecto

```text
Usuario incorrecto
Contraseña válida
```

Pregunta:

> ¿Qué debería ocurrir?

Resultado esperado:

> El acceso debe ser rechazado.

---

## Escenario 3: Contraseña incorrecta

```text
Usuario válido
Contraseña incorrecta
```

Resultado esperado:

> El acceso debe ser rechazado.

---

## Escenario 4: Campos vacíos

No ingresar información.

Presionar Login.

Resultado esperado:

> El sistema debe validar los campos.

---

## Escenario 5: Solo usuario

Ingresar usuario.

No ingresar contraseña.

Resultado esperado:

> El sistema debe validar la información.

---

## Escenario 6: Solo contraseña

No ingresar usuario.

Ingresar contraseña.

Resultado esperado:

> El sistema debe validar la información.

---

## Escenario 7: Usuario bloqueado

```text
Usuario: locked_out_user
Contraseña: secret_sauce
```

Pregunta:

> ¿Qué debería ocurrir?

Resultado esperado:

> El usuario no debería poder ingresar y debería recibir un mensaje adecuado.

---

# 29. RESULTADO ESPERADO VS RESULTADO OBTENIDO

Seleccionar un escenario.

Antes de ejecutar preguntar:

> ¿Qué esperamos que ocurra?

Definir:

# Resultado esperado

Ejecutar.

Observar:

# Resultado obtenido

Comparar:

```text
Esperado
   ↓
Ejecutar
   ↓
Obtenido
   ↓
Comparar
```

---

# 30. CONTINUAR EXPLORANDO

Preguntar:

> ¿Qué más podríamos verificar?

---

## Interfaz

- ¿Los campos son claros?
- ¿El botón es visible?
- ¿Los mensajes se entienden?

---

## Validaciones

- ¿Se validan campos vacíos?
- ¿Los mensajes son adecuados?

---

## Comportamiento

- ¿Qué ocurre si presionamos varias veces?
- ¿Qué ocurre con diferentes usuarios?

---

## Seguridad

Introducir superficialmente:

- ¿La contraseña se muestra?
- ¿El sistema protege el campo?

---

# 31. REFLEXIÓN DEL EJEMPLO

Preguntar:

> ¿Todas las pruebas tenían como objetivo ingresar al sistema?

No.

Algunas verificaban que:

- El sistema permita.
- El sistema rechace.
- El sistema valide.
- El sistema informe.

---

## Idea importante

> **Una prueba puede ser exitosa aunque el usuario no pueda completar una acción.**

Ejemplo:

Un usuario bloqueado no debe ingresar.

Si el sistema rechaza correctamente el acceso:

> La prueba es exitosa.

---

# 32. PROCESO MENTAL DEL QA

Mostrar:

```text
Observar
   ↓
Comprender
   ↓
Preguntar
   ↓
Identificar escenarios
   ↓
Definir expectativas
   ↓
Ejecutar
   ↓
Comparar
   ↓
Comunicar
```

---

# 33. ACTIVIDAD CORTA

Presentar:

```text
REGISTRO DE USUARIO


Nombre

Correo electrónico

Contraseña

Confirmar contraseña


[ Registrarse ]
```

---

## Instrucción

Individualmente o en parejas:

> Identifique al menos cinco situaciones que deberían probarse.

---

## Posibles respuestas

- Campos vacíos.
- Correo inválido.
- Contraseñas diferentes.
- Usuario existente.
- Nombre demasiado largo.
- Contraseña demasiado corta.
- Espacios.
- Caracteres especiales.

---

## Objetivo

No crear casos de prueba formales.

El objetivo es desarrollar:

# MENTALIDAD QA

---

# 34. ACTIVIDAD DE CIERRE

Presentar:

> El usuario puede eliminar su cuenta.

Preguntar:

> **¿Qué probarían?**

Posibles respuestas:

- Confirmación.
- Cancelación.
- Eliminación correcta.
- Usuario inexistente.
- Sesión activa.
- Mensajes.
- Datos relacionados.

---

# 35. RESUMEN DE LA CLASE

Durante esta clase aprendimos:

---

## Calidad

No significa solamente ausencia de errores.

---

## QA

Ayuda a prevenir problemas y promover la calidad.

---

## Testing

Evalúa el comportamiento del software.

---

## La calidad es responsabilidad compartida

Todo el equipo participa.

---

## QA participa durante diferentes etapas

No solamente al final.

---

## Los requisitos son fundamentales

Nos ayudan a saber qué debemos verificar.

---

## Un QA debe analizar y preguntar

No debe asumir.

---

## No podemos probar todo

Necesitamos estrategia y priorización.

---

## El riesgo importa

No todas las funcionalidades tienen la misma importancia.

---

## Las pruebas manuales requieren pensamiento

No consisten únicamente en hacer clic.

---

# 36. CONCEPTOS CLAVE

Al finalizar la clase, los estudiantes deben reconocer:

- Calidad de software.
- QA.
- QC.
- Testing.
- Pruebas manuales.
- Requisitos.
- Requisitos funcionales.
- Requisitos no funcionales.
- Error.
- Defecto.
- Fallo.
- Bug.
- Resultado esperado.
- Resultado obtenido.
- Datos de prueba.
- Ambiente de prueba.
- Riesgo.
- Escenario de prueba.
- Caso de prueba.
- Prueba positiva.
- Prueba negativa.
- Verificación.
- Validación.

---

# 37. MENSAJES PRINCIPALES PARA RECORDAR

> **Calidad no significa solamente ausencia de errores.**

> **QA no solamente busca bugs.**

> **La calidad es responsabilidad de todo el equipo.**

> **Las pruebas comienzan con el análisis.**

> **Un QA debe hacer preguntas.**

> **No podemos probar todo.**

> **Debemos pensar en riesgos y prioridades.**

> **Un resultado diferente al esperado debe analizarse.**

> **La calidad es un proceso continuo.**

---

# 38. MENSAJE FINAL DE LA CLASE

Podemos finalizar con el siguiente mensaje:

> **Un QA no comienza haciendo clic.**

> **Un QA comienza observando, analizando y haciendo preguntas.**

La idea central de esta primera clase es:

# UN QA NO SOLAMENTE PRUEBA SOFTWARE.

# UN QA ANALIZA, PREGUNTA, PREVIENE, VERIFICA Y COMUNICA.

---

# 39. TRANSICIÓN A LA SIGUIENTE CLASE

En esta primera clase aprendimos:

- Qué es calidad.
- Qué es QA.
- Qué es Testing.
- Qué hace un QA.
- Cómo comienza a pensar un QA.

La siguiente etapa será aprender:

> **¿Cómo transformamos una funcionalidad en escenarios y pruebas concretas?**

Posteriormente profundizaremos en:

- Escenarios de prueba.
- Casos de prueba.
- Datos de prueba.
- Resultados esperados.
- Pruebas positivas.
- Pruebas negativas.
- Diseño de pruebas.
- Estrategias de prueba.

---

# 40. NOTAS PARA EL DOCENTE

Durante esta primera clase es recomendable evitar profundizar demasiado en:

- Herramientas.
- Jira.
- Reporte formal de defectos.
- Severidad y prioridad.
- Casos de prueba avanzados.
- Automatización.
- Selenium.
- Playwright.
- Técnicas avanzadas de diseño.

El objetivo es construir una base sólida.

Durante toda la clase reforzar tres ideas:

> **QA no significa solamente buscar errores.**

> **Las pruebas comienzan con preguntas.**

> **Un QA debe pensar antes de probar.**