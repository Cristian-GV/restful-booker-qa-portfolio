# Casos de Prueba - Interfaz de Usuario (UI)

## Módulo: Formulario de Contacto ("Submit a message")

| ID | Título | Precondiciones | Pasos | Datos de Prueba | Resultado Esperado |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **CDP-01** | Enviar formulario con datos válidos (Happy Path) | - Navegador abierto en: `https://automationintesting.online/`<br>- La página cargó correctamente. | 1. Desplazarse al formulario al final de la página.<br>2. Llenar todos los campos del formulario.<br>3. Hacer clic en el botón **"Submit"**. | **Name:** Cristian Galdames<br>**Email:** cristiango84@gmail.com<br>**Phone:** +5217711134730<br>**Subject:** Consulta Single<br>**Message:** Quiero información de la habitación Single | Aparece un mensaje de confirmación dinámico: <br>*"Thanks for getting in touch Cristian Galdames! We'll get back to you about Consulta Single as soon as possible."* |
