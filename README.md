

# Urban Grocers – QA API Testing Project

Este repositorio contiene el proyecto de **pruebas de aseguramiento de calidad sobre la API REST de Urban Grocers**, desarrollado como parte del programa de **QA Engineer en TripleTen**.  
El objetivo principal es validar la correcta gestión de pedidos desde el backend, asegurando integridad de datos, manejo adecuado de errores y cumplimiento de los requisitos funcionales.

---

## 📌 Contexto del proyecto

**Urban Grocers** es una aplicación backend que permite la gestión de pedidos de supermercado mediante una API REST.  
El sistema expone múltiples endpoints que permiten crear, consultar, actualizar y eliminar pedidos, los cuales pueden ser consumidos por aplicaciones frontend u otros servicios.

Desde el rol de QA, este proyecto se enfoca en **verificar la confiabilidad del backend sin depender de la interfaz gráfica**, utilizando pruebas de API.

---

## 🎯 Objetivo del testing

- Validar que los endpoints REST funcionen según lo especificado.
- Verificar que la API maneje correctamente datos válidos e inválidos.
- Detectar defectos en la lógica de negocio del backend.
- Asegurar respuestas HTTP correctas (status codes y body).
- Identificar riesgos que puedan impactar al frontend o a otros sistemas integrados.

---

## 🧠 Problemas abordados

Durante el análisis de la API se identificaron riesgos como:
- Endpoints que aceptan datos inválidos.
- Falta de validaciones obligatorias.
- Respuestas exitosas en escenarios que deberían fallar.
- Mensajes de error poco claros o inexistentes.

El proyecto busca detectar estos problemas antes de que lleguen a producción.

---

## 👨‍💻 Mi contribución como QA Engineer

En este proyecto realicé las siguientes actividades:

- Análisis de la documentación de la API.
- Identificación de endpoints críticos para el negocio.
- Diseño de **casos de prueba de API** (escenarios positivos y negativos).
- Ejecución de pruebas manuales utilizando **Postman**.
- Validación de:
  - Status codes HTTP
  - Estructura del response body
  - Reglas de negocio
- Detección y documentación de defectos en **Jira**, incluyendo:
  - Severidad
  - Prioridad
  - Resultado esperado vs actual
- Recolección de evidencias (capturas de Postman).

---

## 🧪 Tipos de pruebas realizadas

- Functional testing
- API testing
- Negative testing
- Validation testing
- Smoke testing de endpoints críticos

---

## 🔗 Endpoints probados (ejemplos)

- `POST /orders` – Crear pedido
- `GET /orders/{id}` – Consultar pedido
- `PUT /orders/{id}` – Actualizar pedido
- `DELETE /orders/{id}` – Eliminar pedido

*(Los endpoints exactos se detallan en los casos de prueba y colecciones Postman.)*

---

## 🐞 Ejemplo de defecto encontrado

**Título:** El endpoint POST /orders permite crear pedidos sin productos  
**Severidad:** Alta  
**Prioridad:** Alta  

- **Resultado esperado:**  
  El sistema debe rechazar el request y devolver un error 400 (Bad Request).
- **Resultado actual:**  
  El pedido se crea exitosamente con status 201, aun sin productos.

Este defecto representa un riesgo alto para la integridad del negocio.

---

## 🧰 Herramientas utilizadas

- **Postman** – Ejecución de pruebas de API
- **Jira** – Gestión y seguimiento de bugs
- **Git / GitHub** – Control de versiones y documentación

---

