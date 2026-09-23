# GUÍA DEL DOCENTE

## Unidad 5 — API Testing con Postman

**Módulo:** Estrategia de Aseguramiento de la Calidad y Pruebas Manuales
**Unidad:** 5 — API Testing
**Duración:** 3 horas
**Herramienta principal:** Postman
**API utilizada para práctica:** JSONPlaceholder
**Nivel:** QA Manual / Introducción a automatización

---

# 1. Propósito de la unidad

Esta unidad introduce al estudiante en las pruebas de APIs desde la perspectiva de Quality Assurance.

El objetivo no es convertir al estudiante en desarrollador de APIs ni enseñarle programación avanzada.

El objetivo es que comprenda:

> **Cómo comunicarse con una API, cómo analizar una respuesta y cómo determinar si el comportamiento observado cumple con lo esperado.**

Además, se introduce brevemente la automatización mediante las funcionalidades de testing de Postman.

La progresión de aprendizaje será:

```text
Comprender API
      ↓
Comprender HTTP
      ↓
Analizar Request
      ↓
Analizar Response
      ↓
Ejecutar pruebas manuales
      ↓
Validar resultados
      ↓
Automatizar validaciones repetitivas
```

---

# 2. Objetivos de aprendizaje

Al finalizar la clase, el estudiante será capaz de:

1. Explicar qué es una API.
2. Diferenciar frontend, backend y API.
3. Explicar qué es una API REST.
4. Identificar recursos y endpoints.
5. Reconocer los principales métodos HTTP.
6. Diferenciar Request y Response.
7. Identificar URL, headers, parámetros y body.
8. Interpretar códigos de estado HTTP.
9. Comprender la estructura básica de JSON.
10. Ejecutar requests utilizando Postman.
11. Analizar respuestas de una API.
12. Realizar pruebas positivas y negativas.
13. Utilizar Collections y variables básicas.
14. Crear assertions sencillas en Postman.
15. Comprender la relación entre testing manual y automatización.

---

# 3. Distribución de la clase

| Bloque    | Tema                        |      Tiempo |
| --------- | --------------------------- | ----------: |
| 1         | Introducción a API Testing  |      20 min |
| 2         | REST y HTTP                 |      25 min |
| 3         | Request y Response          |      25 min |
| 4         | JSON y Status Codes         |      20 min |
| 5         | Práctica guiada con Postman |      35 min |
| 6         | Collections y Variables     |      20 min |
| 7         | Tests y Assertions          |      25 min |
| 8         | Ejercicio guiado            |      10 min |
| 9         | Práctica del estudiante     |      15 min |
| **Total** |                             | **180 min** |

---

# 4. Recomendación metodológica

La clase debe seguir una regla sencilla:

> **Primero explicar el concepto, después mostrarlo y finalmente permitir que el estudiante lo pruebe.**

No conviene comenzar directamente abriendo Postman.

El estudiante debe comprender primero:

```text
¿Qué estoy probando?
       ↓
¿Cómo se comunica?
       ↓
¿Qué envío?
       ↓
¿Qué recibo?
       ↓
¿Qué debería recibir?
```

Solamente después se introduce Postman.

---

# 5. Diapositiva 1 — Portada

## API Testing con Postman

### Qué debe explicar el docente

Introducir la idea de que una aplicación moderna está formada por diferentes componentes que necesitan comunicarse.

Explicar que durante esta clase el estudiante aprenderá a probar una parte fundamental de esas comunicaciones: las APIs.

### Mensaje importante

> "Hoy no vamos a aprender a desarrollar una API. Vamos a aprender a probarla."

---

# 6. Diapositiva 2 — Objetivos

Presentar brevemente los objetivos.

No es necesario leer cada punto.

Explicar que la clase seguirá una progresión:

```text
Conceptos
   ↓
HTTP
   ↓
Request / Response
   ↓
Postman
   ↓
Validaciones
   ↓
Automatización
```

### Pregunta para iniciar

Preguntar:

> "Cuando una aplicación web necesita guardar información, ¿cómo creen que llega esa información al servidor?"

Escuchar respuestas antes de explicar.

---

# 7. Diapositiva 3 — ¿Qué es una API?

## Definición

**API (Application Programming Interface)** es un mecanismo que permite que diferentes aplicaciones o componentes de software se comuniquen mediante reglas definidas.

Una API establece cómo un consumidor puede solicitar información o realizar operaciones sobre un sistema.

### Explicación sencilla

Podemos utilizar la analogía de un restaurante:

```text
Cliente → Mesero → Cocina
```

El cliente no entra directamente a la cocina.

El mesero funciona como intermediario.

De manera similar:

```text
Aplicación → API → Backend
```

La aplicación no necesita conocer todos los detalles internos del backend.

### Concepto importante

Una API define:

* qué operaciones se pueden realizar;
* cómo solicitar esas operaciones;
* qué información se debe enviar;
* qué respuesta se puede esperar.

---

# 8. Diapositiva 4 — Ejemplo cotidiano

Utilizar el ejemplo de una aplicación de compras.

```text
Usuario
   ↓
Frontend
   ↓
API
   ↓
Backend
   ↓
Base de datos
```

Explicar:

El usuario hace clic en "Comprar".

El frontend puede enviar una solicitud al backend mediante una API.

La API recibe la solicitud y permite que el backend procese la operación.

### Aclaración importante

La API no es necesariamente una base 80> de datos.

Tampoco es necesariamente el frontend.

Es el mecanismo/interfaz que permite la comunicación entre componentes.

---

# 9. Diapositiva 5 — ¿Dónde está la API?

Explicar la arquitectura de manera conceptual.

```text
Frontend
   ↓
API
   ↓
Backend
   ↓
Database
```

### Pregunta

> "¿Podemos probar la API sin utilizar la interfaz gráfica?"

Respuesta:

**Sí.**

Esto es precisamente una de las ventajas del API Testing.

Podemos enviar requests directamente a la API.

### Valor para QA

Esto permite detectar problemas sin depender de la interfaz.

---

# 10. Diapositiva 6 — ¿Por qué probar APIs?

Explicar que la API puede contener errores aunque el frontend parezca funcionar.

Un QA puede validar:

* Datos.
* Reglas de negocio.
* Respuestas.
* Errores.
* Autenticación.
* Integraciones.
* Contratos.
* Rendimiento.

### Concepto clave

> Probar la interfaz no significa que todo el backend esté correctamente probado.

---

# 11. Diapositiva 7 — ¿Qué prueba un QA?

Aquí debemos cambiar la mentalidad del estudiante.

No queremos que piense:

> "Si recibí 200, está bien."

Queremos que piense:

> "¿La respuesta cumple con lo que establece el requisito?"

Por ejemplo:

```text
Esperado:
Usuario con ID 10

Actual:
Usuario con ID 15
```

Aunque la API devuelva:

```text
200 OK
```

existe un problema funcional.

### Frase para enfatizar

> **El código HTTP es una parte de la validación, no toda la validación.**

---

# 12. Diapositiva 8 — ¿Qué es REST?

## Definición

**REST (Representational State Transfer)** es un estilo arquitectónico utilizado para diseñar servicios web.

En la práctica, muchas APIs REST utilizan HTTP para trabajar con recursos.

### No profundizar demasiado

No entrar en teoría avanzada sobre REST.

Para este curso basta comprender:

```text
Recurso + URL + Método HTTP
```

Ejemplo:

```text
GET /users
```

---

# 13. Diapositiva 9 — Recursos

Explicar que una API normalmente expone recursos.

Ejemplos:

```text
/users
/products
/orders
/customers
```

Estos representan entidades del sistema.

### Pregunta

> "Si estamos desarrollando un sistema hospitalario, ¿qué recursos podríamos encontrar?"

Posibles respuestas:

* patients
* doctors
* appointments
* medical-records

Esto permite relacionar el concepto con sistemas reales.

---

# 14. Diapositiva 10 — Endpoint

## Definición

Un **endpoint** es una dirección específica de una API que permite acceder a una funcionalidad o recurso.

Ejemplo:

```text
GET /users
```

Otro:

```text
GET /users/15
```

### Explicación

No debemos confundir:

**Recurso:**

```text
/users
```

**Endpoint:**

```text
GET /users
```

El método HTTP forma parte de la operación que queremos realizar sobre el recurso.

---

# 15. Diapositiva 11 — Métodos HTTP

Explicar:

| Método | Uso                     |
| ------ | ----------------------- |
| GET    | Obtener información     |
| POST   | Crear                   |
| PUT    | Actualizar un recurso   |
| PATCH  | Actualizar parcialmente |
| DELETE | Eliminar                |

### Ejemplos

```text
GET /users
POST /users
PUT /users/10
PATCH /users/10
DELETE /users/10
```

### Pregunta

> "¿Qué método usaríamos para consultar un usuario?"

GET.

> "¿Para crear uno?"

POST.

---

# 16. Diapositiva 12 — CRUD + HTTP

Relacionar:

```text
CREATE → POST
READ   → GET
UPDATE → PUT / PATCH
DELETE → DELETE
```

### Aclaración

PUT y PATCH no son exactamente iguales.

**PUT:** normalmente representa una actualización completa o reemplazo.

**PATCH:** actualización parcial.

No es necesario entrar en detalles de implementación.

---

# 17. Diapositiva 13 — Request

## Definición

Un **Request** es la solicitud que el cliente envía al servidor.

Puede contener:

* Método.
* URL.
* Headers.
* Parámetros.
* Body.

### Ejemplo

```http
POST /users
Content-Type: application/json
```

```json
{
  "name": "Juan",
  "email": "juan@example.com"
}
```

---

# 18. Diapositiva 14 — Anatomía del Request

Explicar cada componente.

### Método

Indica la operación.

### URL

Indica dónde realizar la operación.

### Headers

Información adicional de la solicitud.

### Parámetros

Información enviada como parte de la URL o ruta.

### Body

Información enviada al servidor.

### Pregunta

> "¿Todos los requests tienen body?"

No.

Por ejemplo, un GET normalmente no necesita body.

---

# 19. Diapositiva 15 — URL

Ejemplo:

```text
https://api.example.com/users/15
```

Explicar:

```text
https
 ↓
protocolo

api.example.com
 ↓
servidor

/users
 ↓
recurso

/15
 ↓
identificador
```

No es necesario enseñar DNS ni infraestructura.

El objetivo es que el QA pueda leer una URL.

---

# 20. Diapositiva 16 — Parámetros

Existen diferentes formas de enviar parámetros.

### Path Parameter

```text
/users/15
```

Aquí `15` identifica un recurso.

### Query Parameter

```text
/users?page=2
```

Aquí `page=2` es un parámetro de consulta.

### Pregunta

> "¿Cuál es la diferencia?"

Path:

> Identifica normalmente un recurso.

Query:

> Modifica o filtra una consulta.

---

# 21. Diapositiva 17 — Headers

## Definición

Los headers contienen información adicional relacionada con la petición o respuesta HTTP.

Ejemplo:

```text
Content-Type: application/json
```

Puede indicar el formato del contenido.

Otro ejemplo:

```text
Authorization: Bearer TOKEN
```

Puede transportar información de autenticación.

### Para QA

Debemos comprobar que:

* los headers requeridos estén presentes;
* tengan valores correctos;
* la API responda apropiadamente cuando faltan.

---

# 22. Diapositiva 18 — Body

El body contiene datos enviados al servidor.

Ejemplo:

```json
{
  "name": "Juan",
  "email": "juan@example.com"
}
```

Es habitual encontrar body en:

* POST
* PUT
* PATCH

### Desde QA

Debemos comprobar:

* campos obligatorios;
* tipos;
* valores;
* formatos;
* reglas de negocio.

---

# 23. Diapositiva 19 — Response

## Definición

Un **Response** es la respuesta enviada por el servidor después de procesar un request.

Puede contener:

* Status Code.
* Headers.
* Body.

Ejemplo:

```text
201 Created
```

```json
{
  "id": 25,
  "name": "Juan"
}
```

---

# 24. Diapositiva 20 — Analizando un Response

Explicar que el QA debe analizar tres aspectos:

### 1. Status

¿La operación tuvo el resultado esperado?

### 2. Headers

¿La respuesta tiene la información esperada?

### 3. Body

¿Los datos son correctos?

---

# 25. Diapositiva 21 — Status Codes

Explicar las categorías:

```text
2xx → Éxito
3xx → Redirección
4xx → Error relacionado con la solicitud
5xx → Error del servidor
```

No memorizar todos los códigos.

---

# 26. Diapositiva 22 — Códigos importantes

### 200 — OK

La solicitud fue procesada correctamente.

### 201 — Created

Se creó un recurso.

### 400 — Bad Request

La solicitud no es válida.

### 401 — Unauthorized

Falta autenticación válida.

### 403 — Forbidden

El servidor entiende la solicitud, pero no permite realizar la operación.

### 404 — Not Found

El recurso no fue encontrado.

### 500 — Internal Server Error

Error interno del servidor.

---

# 27. Diapositiva 23 — ¿200 significa que todo está bien?

Este concepto merece énfasis.

Ejemplo:

```text
GET /users/1
```

Respuesta:

```text
200 OK
```

Pero:

```json
{
  "id": 5,
  "name": "Pedro"
}
```

El requisito esperaba:

```text
id = 1
```

Tenemos:

```text
Status → Correcto
Datos → Incorrectos
```

Por lo tanto:

> **La prueba puede fallar aunque el status sea 200.**

---

# 28. Diapositiva 24 — JSON

## Definición

**JSON (JavaScript Object Notation)** es un formato utilizado frecuentemente para representar e intercambiar datos.

Ejemplo:

```json
{
  "id": 10,
  "name": "Laptop",
  "price": 5000,
  "available": true
}
```

---

# 29. Diapositiva 25 — Elementos de JSON

Explicar:

### String

```json
"name": "Laptop"
```

### Número

```json
"price": 5000
```

### Boolean

```json
"available": true
```

### Array

```json
"tags": ["computer", "office"]
```

### Objeto

```json
"address": {
  "city": "La Paz"
}
```

No profundizar en sintaxis de programación.

---

# 30. Diapositiva 26 — ¿Qué valida QA en JSON?

El QA puede validar:

### Existencia

¿Está el campo?

### Tipo

¿Es string, número, boolean, array?

### Valor

¿Tiene el valor esperado?

### Estructura

¿La respuesta tiene la estructura correcta?

### Reglas

¿Se cumplen las reglas de negocio?

---

# 31. Diapositiva 27 — Postman

## Definición

**Postman** es una herramienta utilizada para desarrollar, probar y trabajar con APIs.

En esta clase la utilizaremos para:

* Crear requests.
* Ejecutarlos.
* Analizar responses.
* Crear Collections.
* Utilizar variables.
* Crear tests.

### Importante

Postman es una herramienta.

**API Testing es la disciplina/práctica de testing.**

---

# 32. Diapositiva 28 — Primera práctica

Utilizar JSONPlaceholder como API de demostración.

Endpoint:

```text
GET https://jsonplaceholder.typicode.com/users
```

Pedir a los estudiantes que observen:

* Método.
* URL.
* Status.
* Tiempo.
* Body.

### Preguntas

> ¿Qué status recibimos?

> ¿Qué formato tiene la respuesta?

> ¿Qué contiene cada usuario?

---

# 33. Diapositiva 29 — Analizando Response

Aquí el docente debe demostrar que una prueba no consiste simplemente en "hacer clic en Send".

Analizar:

```text
Status
Response time
Headers
Body
```

Después preguntar:

> "¿Qué podríamos comprobar como QA?"

Esperar respuestas de los estudiantes.

---

# 34. Diapositiva 30 — GET por ID

Ejecutar:

```text
GET https://jsonplaceholder.typicode.com/users/1
```

Analizar:

```json
{
  "id": 1,
  ...
}
```

### Pregunta

> "¿Qué condición podemos validar?"

Respuesta:

```text
El ID recibido debe ser 1.
```

Aquí comienza a introducirse el concepto de **assertion**.

---

# 35. Diapositiva 31 — Negative Testing

Ejecutar:

```text
GET https://jsonplaceholder.typicode.com/users/9999
```

### Explicar

No solamente debemos comprobar:

> "¿Funciona con datos correctos?"

También:

> "¿Qué ocurre cuando la entrada no es válida o el recurso no existe?"

### Tipos de escenarios negativos

* ID inexistente.
* Parámetro inválido.
* Campo obligatorio faltante.
* Formato incorrecto.
* Usuario no autenticado.

---

# 36. Diapositiva 32 — Collections

## Definición

Una Collection permite agrupar requests relacionadas.

Ejemplo:

```text
Users API
├── Get Users
├── Get User
├── Create User
├── Update User
└── Delete User
```

### Beneficios

* Organización.
* Reutilización.
* Mantenimiento.
* Ejecución conjunta.

---

# 37. Diapositiva 33 — Variables

Mostrar:

```text
{{base_url}}/users
```

En lugar de:

```text
https://jsonplaceholder.typicode.com/users
```

Variable:

```text
base_url =
https://jsonplaceholder.typicode.com
```

### Explicación

Las variables permiten reutilizar información y cambiar configuraciones sin modificar cada request.

---

# 38. Diapositiva 34 — Ambientes

Explicar el concepto:

```text
DEV
QA
STAGING
PRODUCTION
```

Podríamos tener:

```text
{{base_url}}
```

con diferentes valores.

### Mensaje importante

> El request puede ser el mismo; el ambiente puede cambiar.

Esto es especialmente importante en proyectos profesionales.

---

# 39. Diapositiva 35 — Automatización

Introducir el problema.

Preguntar:

> "Si tenemos que comprobar el mismo endpoint 100 veces, ¿queremos revisar manualmente el status y los datos cada vez?"

Aquí introducir:

> **Automatización de pruebas.**

La automatización permite ejecutar validaciones repetitivas de manera consistente.

---

# 40. Diapositiva 36 — Primera assertion

Mostrar:

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

Explicar solamente lo necesario.

### `pm.test`

Define una prueba.

### `pm.response`

Permite acceder a la respuesta.

### `to.have.status(200)`

Comprueba que el status sea 200.

---

# 41. Diapositiva 37 — Validar un dato

Mostrar:

```javascript
pm.test("User ID is 1", function () {
    const data = pm.response.json();
    pm.expect(data.id).to.eql(1);
});
```

Explicar conceptualmente:

```text
Response
   ↓
Convertimos a JSON
   ↓
Obtenemos id
   ↓
Comparamos con 1
```

### No enseñar

* Funciones avanzadas.
* Loops.
* Variables complejas.
* Programación avanzada.

El objetivo es comprender la idea.

---

# 42. Diapositiva 38 — ¿Qué estamos automatizando?

Esta diapositiva es importante pedagógicamente.

Explicar:

> No estamos automatizando el pensamiento del QA.

Estamos automatizando una validación que ya sabemos definir.

Proceso:

```text
Requisito
   ↓
QA analiza
   ↓
Define resultado esperado
   ↓
Diseña prueba
   ↓
Automatiza validación
```

### Frase clave

> **Primero sabemos qué probar; después decidimos qué automatizar.**

---

# 43. Diapositiva 39 — Actividad práctica

Los estudiantes crearán:

```text
Collection:
QA - Users API
```

### Request 1

```text
GET /users
```

### Request 2

```text
GET /users/1
```

### Request 3

```text
GET /users/9999
```

### Request 4

Crear una assertion.

Por ejemplo:

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

---

# 44. Diapositiva 40 — Piensa como QA

Mostrar:

```text
RESULTADO ESPERADO
        ↓
     COMPARAR
        ↑
RESULTADO ACTUAL
```

### Pregunta final

> "¿Qué ocurre si el resultado actual no coincide con el esperado?"

Respuesta:

> Tenemos una prueba fallida y debemos investigar si existe un defecto.

Esto conecta con las unidades anteriores.

---

# 45. Diapositiva 41 — Postman no es API Testing

Explicar:

**Postman = herramienta**

**API Testing = actividad de QA**

Existen otras herramientas:

* Postman.
* Insomnia.
* SoapUI.
* K6.
* Rest Assured.
* Playwright.
* Cypress.

No profundizar en ellas.

El estudiante debe entender que los conocimientos aprendidos son transferibles.

---

# 46. Diapositiva 42 — Resumen

Repasar:

```text
API
 ↓
REST
 ↓
HTTP
 ↓
Request
 ↓
Response
 ↓
JSON
 ↓
Postman
 ↓
Assertions
 ↓
Automatización
```

Preguntar a los estudiantes:

> ¿Qué concepto les parece más importante de la clase?

Utilizar sus respuestas para detectar posibles dificultades.

---

# 47. Diapositiva 43 — Idea final

Presentar:

> **Una API no se prueba solamente para saber si responde.**

> **Se prueba para saber si responde correctamente según los requisitos.**

Y:

> **Primero pensamos como QA. Después utilizamos la herramienta. Finalmente automatizamos lo repetitivo.**

---

# 48. Conceptos fundamentales que el estudiante debe dominar

Al finalizar la clase, comprobar que puedan definir:

### API

Mecanismo que permite la comunicación entre aplicaciones o componentes.

### REST

Estilo arquitectónico utilizado para diseñar servicios web.

### Endpoint

Dirección específica de una API para acceder a un recurso u operación.

### Request

Petición enviada al servidor.

### Response

Respuesta enviada por el servidor.

### HTTP Method

Indica la operación que se desea realizar.

### Header

Información adicional asociada a una petición o respuesta HTTP.

### Parameter

Dato utilizado para modificar o identificar una solicitud.

### Body

Contenido enviado dentro de una petición HTTP.

### Status Code

Código que comunica el resultado de una petición HTTP.

### JSON

Formato utilizado para representar e intercambiar datos.

### Assertion

Validación que comprueba una condición esperada.

### API Testing

Proceso de verificar que una API funciona correctamente de acuerdo con los requisitos y condiciones esperadas.

### Automatización

Uso de herramientas o scripts para ejecutar y validar pruebas de forma automática, especialmente cuando las verificaciones son repetitivas.

---

# 49. Errores frecuentes que debe evitar el docente

## Error 1 — Convertir la clase en programación

No dedicar demasiado tiempo a JavaScript.

El código de Postman es solamente un medio para explicar assertions.

---

## Error 2 — Enseñar demasiados códigos HTTP

No es necesario memorizar decenas de códigos.

Concentrarse en los más utilizados.

---

## Error 3 — Confundir API con Postman

Postman no es una API.

Postman es una herramienta para trabajar con APIs.

---

## Error 4 — Pensar que HTTP 200 significa éxito funcional

Un `200 OK` solamente indica que la petición HTTP fue procesada con éxito según el protocolo.

Los datos todavía deben validarse.

---

## Error 5 — Probar únicamente casos positivos

Recordar:

> **Un buen QA también pregunta qué sucede cuando las cosas salen mal.**

---

## Error 6 — Inventar resultados esperados

El resultado esperado debe surgir de:

* Requerimientos.
* Criterios de aceptación.
* Documentación.
* Contrato de API.
* Reglas de negocio.

No de suposiciones del tester.

---

# 50. Preguntas para evaluar comprensión durante la clase

### Pregunta 1

¿Qué diferencia existe entre frontend y API?

### Pregunta 2

¿Qué diferencia existe entre request y response?

### Pregunta 3

¿Qué método utilizarías para crear un usuario?

### Pregunta 4

¿Qué significa 404?

### Pregunta 5

¿Un 200 garantiza que la información recibida sea correcta?

### Pregunta 6

¿Qué diferencia existe entre un path parameter y un query parameter?

### Pregunta 7

¿Por qué utilizamos variables en Postman?

### Pregunta 8

¿Qué es una assertion?

### Pregunta 9

¿Qué parte de una prueba automatizamos?

### Pregunta 10

¿Quién decide qué debe validar una prueba?

Respuesta esperada:

> El QA, basándose en los requisitos, criterios de aceptación, reglas de negocio y comportamiento esperado del sistema.

---

# 51. Actividad práctica — Instrucciones para el docente

## Objetivo

Que el estudiante pueda realizar una prueba básica de API desde cero.

### Paso 1

Abrir Postman.

### Paso 2

Crear una Collection:

```text
QA - Users API
```

### Paso 3

Crear:

```text
GET /users
```

### Paso 4

Analizar la respuesta.

### Paso 5

Crear:

```text
GET /users/1
```

### Paso 6

Comprobar:

```text
Status = 200
id = 1
```

### Paso 7

Crear:

```text
GET /users/9999
```

### Paso 8

Analizar qué sucede.

### Paso 9

Crear una assertion.

### Paso 10

Ejecutar nuevamente y observar:

```text
PASS
FAIL
```

---

# 52. Cierre de la actividad

Preguntar:

> "¿Qué hicimos primero: automatizar o analizar?"

Respuesta:

**Analizar.**

Después:

> "¿Por qué?"

Porque primero necesitamos saber cuál es el comportamiento esperado.

Finalmente:

> "¿Qué automatizamos?"

Las validaciones que queremos repetir de forma consistente.

---

# 53. Relación con las unidades anteriores

Esta unidad debe conectarse con lo aprendido anteriormente.

El estudiante ya aprendió:

```text
Requerimientos
       ↓
Diseño de casos
       ↓
Resultados esperados
       ↓
Defectos
```

Ahora aplicamos esos conocimientos a APIs:

```text
Requerimiento
       ↓
Caso de prueba
       ↓
Request
       ↓
Response
       ↓
Comparación
       ↓
PASS / FAIL
       ↓
Defecto si corresponde
```

Esto permite que el estudiante entienda que **API Testing no es un tema aislado**, sino otra forma de aplicar los fundamentos de testing.

---

# 54. Mensaje pedagógico final para el docente

El estudiante debe terminar la clase comprendiendo tres ideas:

### 1. Una API también debe probarse

No debemos limitar las pruebas a la interfaz gráfica.

### 2. El QA compara comportamiento esperado vs. comportamiento actual

La herramienta ayuda, pero el análisis sigue siendo responsabilidad del QA.

### 3. La automatización viene después del análisis

```text
ENTENDER
   ↓
ANALIZAR
   ↓
DISEÑAR
   ↓
PROBAR
   ↓
VALIDAR
   ↓
AUTOMATIZAR
```

La herramienta puede cambiar.

**La mentalidad de QA permanece.**
