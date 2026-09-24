# Proyecto Final — QA Web Challenge

## Estrategia de Aseguramiento de la Calidad y Pruebas Manuales

### 🎯 Objetivo

Aplicar los conocimientos aprendidos durante el módulo para evaluar la calidad de una aplicación web, diseñando, ejecutando y documentando pruebas.

El proyecto debe demostrar que puedes:

**Analizar → Planificar → Diseñar → Ejecutar → Reportar → Concluir**

---

## 1. Aplicación a evaluar

Utiliza una aplicación web de demostración indicada por el docente.

Ejemplo:

**Demo Web Shop**
https://demowebshop.tricentis.com/

---

## 2. Análisis de funcionalidades

Selecciona **3 funcionalidades** de la aplicación.

Ejemplos:

* Registro de usuario
* Inicio de sesión
* Búsqueda de productos
* Visualización de productos
* Carrito de compras
* Modificación de cantidades
* Proceso de checkout

Para cada funcionalidad identifica brevemente:

* Objetivo de la funcionalidad
* Reglas de negocio que puedas identificar
* Datos necesarios
* Comportamiento esperado
* Posibles riesgos
* Ambigüedades o aspectos que deberían ser aclarados

---

## 3. Casos de prueba

Diseña al menos **10 casos de prueba**.

Incluye:

* ID
* Título
* Precondiciones
* Datos
* Pasos
* Resultado esperado

Los casos deben incluir diferentes escenarios, como positivos y negativos.

---

## 4. Ejecución y Bug Reporting

Ejecuta los casos de prueba y registra:

* PASS / FAIL
* Resultado obtenido
* Evidencia
* Observaciones

Para los defectos encontrados, crea **Bug Reports** que incluyan:

* Título
* Pasos para reproducir
* Resultado esperado
* Resultado actual
* Severidad
* Evidencia

---

## 5. API Testing

Realiza pruebas utilizando **Postman** sobre una AP.

Puedes utilizar una API pública autorizada por el docente, por ejemplo:

**JSONPlaceholder**

https://jsonplaceholder.typicode.com/

Como mínimo:

* 1 GET
* 1 POST
* 1 PUT/PATCH
* 1 DELETE
* 2 assertions


Para las peticiones verifica cuando corresponda:
* Método HTTP
* URL
* Status Code
* Response Body
* Headers
* Datos esperados

Debes incluir evidencia de la ejecución.
---

## 6. Usabilidad y accesibilidad

### Usabilidad

Identifica **2 problemas de usabilidad**.

Para cada uno indica:

* Problema
* Impacto
* Evidencia
* Propuesta de mejora

### Accesibilidad

Identifica **2 problemas de accesibilidad** utilizando herramientas o técnicas vistas en clase, por ejemplo:

* WAVE
* Prueba con teclado

Incluye:

* Problema
* Método utilizado
* Posible usuario afectado
* Evidencia
* Recomendación

---

## 7. Mini Test Plan

Elabora un Mini Test Plan que incluya:

* Objetivo
* Alcance
* Fuera de alcance
* Tipos de prueba
* Ambiente
* Datos de prueba
* Riesgos
* Criterios de entrada
* Criterios de salida

---

## 8. Informe final

Presenta un resumen de los resultados:

| Métrica                    | Resultado |
| -------------------------- | --------: |
| Casos diseñados            |           |
| Casos ejecutados           |           |
| PASS                       |           |
| FAIL                       |           |
| Bugs encontrados           |           |
| Problemas de usabilidad    |           |
| Problemas de accesibilidad |           |

### Conclusión

Explica brevemente:

* Principales problemas encontrados.
* Riesgos identificados.
* Estado de las pruebas.
* Recomendaciones principales.

Las conclusiones deben estar respaldadas por las evidencias obtenidas durante las pruebas.

---

# 📦 Entrega

Organiza el proyecto de la siguiente manera:

```text
QA-Web-Challenge/
│
├── 01-Analisis-Requerimientos/
│   └── analisis-requerimientos.pdf
│
├── 02-Casos-Prueba/
│   └── casos-prueba.xlsx
│
├── 03-Evidencias/
│   ├── screenshots/
│   └── resultados.xlsx
│
├── 04-Bug-Reports/
│   └── bug-reports.pdf
│
├── 05-API-Testing/
│   ├── postman-collection.json
│   └── evidencias/
│
├── 06-Usabilidad-Accesibilidad/
│   └── reporte-usabilidad-accesibilidad.pdf
│
├── 07-Test-Plan/
│   └── test-plan.pdf
│
└── 08-Informe-Final/
    └── informe-final.pdf
```

---

# 📊 Evaluación

| Criterio                   | Porcentaje |
| -------------------------- | ---------: |
| Análisis de requerimientos |        10% |
| Casos de prueba            |        20% |
| Ejecución y evidencias     |        10% |
| Bug Reporting              |        15% |
| API Testing                |        15% |
| Usabilidad y accesibilidad |        15% |
| Mini Test Plan             |        15% |
| **Total**                  |   **100%** |

---

## 💡 Regla principal

> **No basta con decir que algo está mal. Debes demostrarlo.**

Cada hallazgo debe tener:

**Observación → Evidencia → Análisis → Impacto**

El objetivo es demostrar que puedes aplicar un proceso básico de QA de principio a fin.
