# Reporte de Prueba QA: INFO-006

**ID del Caso:** INFO-006
**Módulo:** Información Personal
**Descripción:** Verificar que el sistema rechace el cambio de contraseña cuando no cumpla con las reglas mínimas.
**Fecha:** 21-10-2026
**Tipo de Prueba:** Caja negra — Valores límite

## Datos / Acciones de Entrada
Intentar cambiar la contraseña con menos de 8 caracteres, o igual al número de documento, o con confirmación distinta.

## Resultado Esperado
El sistema rechaza el cambio con mensajes específicos en cada caso.

## Resultado Obtenido
El sistema rechaza correctamente los intentos inválidos. Muestra un mensaje de texto rojo debajo del campo cuando las contraseñas no coinciden, y despliega una notificación Toast cuando la contraseña es igual al documento.

## Estado y Observaciones
*   **Estado:** `Aprobada`
*   **Observaciones:** Pruebas de valores límite exitosas. El sistema cuenta con validaciones robustas tanto a nivel de interfaz como lógico.

---
*Documentación generada por: Andrea Herrera (QA)*