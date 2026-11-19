# Reporte de Prueba QA: Inclusión de Documento PPT y Validaciones

**ID del Caso:** CUEN-011
**Módulo:** Cuentas / Creación y Edición de Usuarios
**Área Funcional:** Gestión de Documentos de Identidad
**Tipo de Prueba:** Caja Blanca (Backend) y Caja Negra (Frontend / UX)
**Fecha de Ejecución:** Noviembre 2026
**Entorno de Pruebas:** Local (Django + SQLite)

---

## 1. Objetivo
Implementar y verificar la regla de negocio para el documento "Permiso por Protección Temporal (PPT)", eliminando el tipo "Pasaporte" del sistema. El PPT debe tener una validación estricta que solo permita **exactamente 7 caracteres numéricos**.

## 2. Análisis y Solución Implementada (Dev)

El sistema requería ajustes en todas las capas (Base de datos, Backend y Frontend):

*   **Modelo (`models.py`):** Se agregó la opción `('PPT', 'Permiso por Protección Temporal')` y se eliminó `('PA', 'Pasaporte')`. Se ajustó el `max_length` del campo `tipo_documento` a 5 para alojar la nueva opción.
*   **Formulario Backend (`forms.py`):** Se implementó la validación `clean_numero_documento` para rechazar cualquier PPT que no tenga 7 caracteres o que contenga letras/símbolos.
*   **Interfaz (`modal.html`):** Se actualizaron los desplegables (`<select>`) en los modales de "Crear" y "Editar" para reflejar el cambio.
*   **Validación Frontend (`cuentas.js`):** Se programó la lógica en JavaScript para bloquear la escritura de letras y limitar el campo a 7 números en tiempo real. *(Nota técnica: Se solucionó un error de sintaxis (`Unexpected token '}'`) en la línea 420 del JS que impedía la ejecución del script).*

## 3. Casos de Prueba Ejecutados (QA)

| # | Escenario | Resultado Esperado | Resultado Obtenido | Estado |
| :--- | :--- | :--- | :--- | :--- |
| 1 | Verificar opciones en el desplegable "Tipo Documento". | Debe aparecer "PPT" y ya no debe aparecer "Pasaporte". | El desplegable muestra las opciones correctas. | ✅ Aprobado |
| 2 | Validación Frontend (UX): Seleccionar PPT e intentar escribir letras o más de 7 números. | El campo debe borrar las letras y detenerse en el carácter número 7. | El JavaScript bloquea activamente la escritura no numérica y el límite de longitud. | ✅ Aprobado |
| 3 | Validación Backend (Seguridad): Forzar un envío de un PPT inválido (saltando el JS vía F12). | El servidor (Django) debe rechazar la petición y mostrar un mensaje de error. | El sistema lanza el Toast de error: *"El PPT debe tener exactamente 7 números..."* | ✅ Aprobado |
| 4 | Visualización en modo Editar: Crear un usuario con PPT y abrir su modal de edición. | El tipo de documento y el número deben mostrarse correctamente. | El modal refleja correctamente "Permiso por Protección Temporal (PPT)" y el número de 7 dígitos. | ✅ Aprobado |

## 4. Conclusión y Observaciones
**Estado de la Prueba:** `APROBADA` ✅

Se logró blindar el formulario mediante una **estrategia de doble capa**:
1.  **Frontend (JS):** Previene el error antes de que ocurra (mejorando la Experiencia de Usuario).
2.  **Backend (Django):** Protege la integridad de la base de datos si el usuario intenta saltarse el Frontend.

El bug de sintaxis en el archivo `cuentas.js` fue diagnosticado exitosamente utilizando la consola de desarrollador (F12) y corregido, garantizando que los scripts se ejecuten sin errores.

---
*Documentación generada por: Andrea Herrera (QA)*