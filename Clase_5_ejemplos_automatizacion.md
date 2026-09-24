# Automatización de API con Postman y JSONPlaceholder

## 1. Objetivo

Practicar la automatización de pruebas de API utilizando **Postman** y **JSONPlaceholder**.

Durante la práctica se aprenderá a:

* Crear y organizar una Collection.
* Utilizar variables.
* Ejecutar requests HTTP.
* Crear pruebas automatizadas con JavaScript.
* Validar códigos de estado HTTP.
* Validar datos de las respuestas.
* Reutilizar información entre requests.
* Ejecutar varias pruebas mediante Collection Runner.

---

# 2. Configuración inicial

## URL base

Utilizaremos:

```text
https://jsonplaceholder.typicode.com
```

Crear un Environment en Postman con la siguiente variable:

| Variable   | Value                                  |
| ---------- | -------------------------------------- |
| `base_url` | `https://jsonplaceholder.typicode.com` |

Las requests utilizarán:

```text
{{base_url}}
```

Por ejemplo:

```http
GET {{base_url}}/users
```

---

# 3. Automatización de GET - Obtener usuarios

## Request

```http
GET {{base_url}}/users
```

## Objetivo

Verificar que:

* La API responda correctamente.
* El código HTTP sea `200`.
* La respuesta sea un arreglo.
* Existan usuarios.

## Tests

En **Scripts → Post-response**:

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Response is an array", function () {
    pm.expect(pm.response.json()).to.be.an("array");
});

pm.test("There are users", function () {
    const users = pm.response.json();

    pm.expect(users.length).to.be.greaterThan(0);
});
```

## Resultado esperado

Todas las pruebas deben aparecer como:

```text
PASS
```

---

# 4. Automatización de GET - Obtener un usuario

## Request

```http
GET {{base_url}}/users/1
```

## Objetivo

Verificar los datos de un usuario específico.

## Tests

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

const user = pm.response.json();

pm.test("User has an id", function () {
    pm.expect(user).to.have.property("id");
});

pm.test("User ID is 1", function () {
    pm.expect(user.id).to.eql(1);
});

pm.test("User has a name", function () {
    pm.expect(user.name).to.be.a("string");
});

pm.test("User has an email", function () {
    pm.expect(user.email).to.be.a("string");
});
```

## ¿Qué estamos automatizando?

Estamos verificando:

```text
Código HTTP
     ↓
Estructura
     ↓
ID
     ↓
Nombre
     ↓
Correo electrónico
```

---

# 5. Automatización de POST - Crear un usuario

## Request

```http
POST {{base_url}}/users
```

## Body

Seleccionar:

```text
Body → raw → JSON
```

Enviar:

```json
{
    "name": "Juan Carlos",
    "username": "jcondori",
    "email": "juan@example.com"
}
```

## Tests

```javascript
pm.test("Status code is 201", function () {
    pm.response.to.have.status(201);
});

const response = pm.response.json();

pm.test("Response contains an ID", function () {
    pm.expect(response).to.have.property("id");
});

pm.test("Name was created correctly", function () {
    pm.expect(response.name).to.eql("Juan Carlos");
});

pm.test("Email was created correctly", function () {
    pm.expect(response.email).to.eql("juan@example.com");
});
```

## ¿Qué estamos validando?

```text
Request
   ↓
POST
   ↓
API
   ↓
Response
   ↓
Status 201
   ↓
Validación de datos
```

---

# 6. POST utilizando variables

Las variables permiten evitar datos escritos directamente en las requests.

## Variables

En el Environment:

| Variable     | Value              |
| ------------ | ------------------ |
| `user_name`  | `Juan Carlos`      |
| `user_email` | `juan@example.com` |

## Body

```json
{
    "name": "{{user_name}}",
    "username": "jcondori",
    "email": "{{user_email}}"
}
```

## Tests

```javascript
const response = pm.response.json();

pm.test("User was created", function () {
    pm.expect(pm.response.code).to.eql(201);
});

pm.test("Name is correct", function () {
    pm.expect(response.name).to.eql(
        pm.environment.get("user_name")
    );
});

pm.test("Email is correct", function () {
    pm.expect(response.email).to.eql(
        pm.environment.get("user_email")
    );
});
```

Esto permite reutilizar los mismos tests aunque cambiemos los datos.

---

# 7. Automatización de PUT - Actualizar un usuario

## Request

```http
PUT {{base_url}}/users/1
```

## Body

```json
{
    "name": "Juan Carlos Actualizado",
    "username": "jcondori",
    "email": "actualizado@example.com"
}
```

## Tests

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

const response = pm.response.json();

pm.test("Name was updated", function () {
    pm.expect(response.name).to.eql(
        "Juan Carlos Actualizado"
    );
});

pm.test("Email was updated", function () {
    pm.expect(response.email).to.eql(
        "actualizado@example.com"
    );
});
```

---

# 8. Automatización de DELETE

## Request

```http
DELETE {{base_url}}/users/1
```

## Test

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

## Importante

JSONPlaceholder es una API de prueba.

Las operaciones como `POST`, `PUT`, `PATCH` y `DELETE` simulan el comportamiento de una API real, pero los cambios no se almacenan de forma permanente.

---

# 9. Reutilizar información entre requests

Podemos guardar información de una respuesta en una variable y utilizarla posteriormente.

## Primera request

```http
GET {{base_url}}/users/1
```

## Test

```javascript
const user = pm.response.json();

pm.environment.set("user_id", user.id);

pm.test("User retrieved successfully", function () {
    pm.response.to.have.status(200);
});
```

Ahora tenemos:

```text
user_id = 1
```

## Segunda request

Podemos utilizar esa variable:

```http
GET {{base_url}}/users/{{user_id}}
```

Esto permite crear flujos donde una request utiliza información obtenida de otra.

---

# 10. Organización de la Collection

Una posible estructura para el ejercicio:

```text
API Testing - JSONPlaceholder
│
├── Users
│   ├── Get Users
│   ├── Get User
│   ├── Create User
│   ├── Update User
│   └── Delete User
│
└── Posts
    ├── Get Posts
    └── Create Post
```

La organización mediante Collections y carpetas facilita el mantenimiento de las pruebas.

---

# 11. Ejecutar la Collection

Después de crear las requests y sus pruebas automatizadas:

1. Abrir la Collection.
2. Seleccionar **Run** o **Run collection**.
3. Seleccionar el Environment.
4. Ejecutar las requests.
5. Revisar los resultados.

El resultado mostrará qué pruebas fueron exitosas y cuáles fallaron.

Conceptualmente:

```text
Request
   ↓
API
   ↓
Response
   ↓
Automated Tests
   ↓
PASS / FAIL
```

---

# 12. Ejercicio para estudiantes

Crear una Collection llamada:

```text
API Testing - JSONPlaceholder
```

## Requerimientos

### Request 1 - Obtener usuarios

```http
GET /users
```

Automatizar:

* Código `200`.
* La respuesta debe ser un array.
* Debe existir al menos un usuario.

### Request 2 - Obtener usuario

```http
GET /users/1
```

Automatizar:

* Código `200`.
* Debe existir `id`.
* El `id` debe ser `1`.
* Debe existir `name`.
* Debe existir `email`.

### Request 3 - Crear usuario

```http
POST /users
```

Enviar un usuario mediante JSON.

Automatizar:

* Código `201`.
* Debe existir un `id`.
* Validar `name`.
* Validar `email`.

### Request 4 - Actualizar usuario

```http
PUT /users/1
```

Automatizar:

* Código `200`.
* Validar que el nombre actualizado sea correcto.
* Validar que el correo actualizado sea correcto.

### Request 5 - Eliminar usuario

```http
DELETE /users/1
```

Automatizar:

* Código `200`.

---

# 13. Resultado esperado

Al ejecutar la Collection, el estudiante debe poder demostrar que sabe:

* Crear una Collection.
* Crear y organizar requests.
* Utilizar variables.
* Trabajar con diferentes métodos HTTP.
* Crear pruebas automatizadas en Postman.
* Validar códigos de respuesta.
* Validar datos de una respuesta.
* Reutilizar variables entre requests.
* Ejecutar una Collection completa.
* Identificar pruebas **PASS** y **FAIL**.

---

# 14. Conceptos clave

| Concepto          | Descripción                                   |
| ----------------- | --------------------------------------------- |
| Collection        | Agrupa requests relacionadas                  |
| Environment       | Permite administrar variables para un entorno |
| Variable          | Permite reutilizar valores                    |
| Request           | Solicitud enviada a la API                    |
| Response          | Respuesta recibida de la API                  |
| Test              | Validación automatizada                       |
| Status Code       | Código HTTP de la respuesta                   |
| PASS              | La validación fue correcta                    |
| FAIL              | La validación no se cumplió                   |
| Collection Runner | Ejecuta varias requests de una Collection     |

---

## Flujo general de automatización

```text
          COLLECTION
               │
               ▼
        ┌──────────────┐
        │   REQUEST    │
        └──────┬───────┘
               │
               ▼
             API
               │
               ▼
        ┌──────────────┐
        │  RESPONSE    │
        └──────┬───────┘
               │
               ▼
        ┌──────────────┐
        │ AUTOMATED    │
        │    TESTS     │
        └──────┬───────┘
               │
          ┌────┴────┐
          ▼         ▼
        PASS       FAIL
```
