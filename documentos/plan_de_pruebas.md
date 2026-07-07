# Plan de Pruebas - Proyecto Restful-Booker (Hotel Platform)

## 1. Introducción
Este documento define la estrategia, el alcance y el enfoque de pruebas para la plataforma de gestión hotelera **Restful-Booker**. El objetivo principal es validar tanto la experiencia del usuario en la interfaz web (Frontend) como la consistencia y seguridad de la API subyacente (Backend), asegurando un producto estable y funcional.

## 2. Objetivos de las Pruebas
*   Validar que los usuarios puedan interactuar correctamente con la interfaz web (visualizar habitaciones, enviar mensajes de contacto y realizar reservas).
*   Garantizar que la API REST responda con los códigos de estado HTTP correctos, tiempos de respuesta adecuados y estructuras JSON válidas.
*   Asegurar que las reglas de negocio se cumplan (por ejemplo, no permitir reservas sin datos obligatorios o fechas inválidas).

## 3. Alcance de las Pruebas (Scope)

### En Alcance (Lo que SÍ se va a probar):
*   **Pruebas de Interfaz de Usuario (UI):**
    *   Formulario de contacto de la página principal.
    *   Flujo visual de reserva de habitaciones (selección de fechas y llenado de datos).
*   **Pruebas de API REST (Postman):**
    *   Autenticación de usuarios (`/auth`).
    *   Gestión de reservas: Creación (`POST`), Consulta (`GET`), Actualización (`PUT`/`PATCH`) y Eliminación (`DELETE`) de reservas sobre `/booking`.

### Fuera de Alcance (Lo que NO se va a probar):
*   Pruebas de carga o estrés masivo (Rendimiento extremo).
*   Pruebas de seguridad contra vulnerabilidades complejas (Penetration Testing).
*   Pasarelas de pago reales (no implementadas en el entorno de pruebas).

## 4. Tipos de Prueba a Ejecutar
*   **Pruebas Funcionales (Caja Negra):** Validación manual de botones, formularios y flujos completos en la web.
*   **Pruebas de Integración de API:** Verificación de contratos, métodos HTTP y aserciones automatizadas mediante scripts en Postman.
*   **Pruebas de Frontera (Boundary Testing):** Validación de campos con límites de caracteres o formatos incorrectos (correos inválidos, números de teléfono erróneos).

## 5. Entorno de Pruebas
*   **Aplicación Web (UI):** https://automationintesting.online/
*   **Documentación de API:** https://restful-booker.herokuapp.com/apidoc/index.html
*   **Herramientas de Ejecución:** Google Chrome (DevTools) y Postman Desktop.
*   **Reporte y Evidencia:** Repositorio público de GitHub.

## 6. Criterios de Aceptación y Rechazo
*   **Criterio de Éxito:** El 100% de los casos de prueba críticos (caminos felices) deben ejecutarse sin errores. Las automatizaciones de Postman deben pasar todas sus aserciones.
*   **Criterio de Rechazo:** Presencia de errores críticos (Bloqueantes/Critical) que impidan la creación de una reserva o bloqueen la respuesta del servidor (Errores 500).
