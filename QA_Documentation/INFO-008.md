# Reporte de Prueba QA: INFO-008

**ID del Caso:** INFO-008
**Módulo:** Información Personal
**Descripción:** Verificar que cada empleado solo pueda ver y editar su propia información personal.
**Fecha:** 21-10-2026
**Tipo de Prueba:** Caja negra — Prueba de sistema (Seguridad)

## Datos / Acciones de Entrada
Iniciar sesión con dos cuentas distintas, comparar información y verificar intentos de acceso por URL.

## Resultado Esperado
Cada empleado ve únicamente sus propios datos y no puede modificar los de otros.

## Resultado Obtenido
El sistema cumple con el aislamiento. El Ataque 2 (URL) fue bloqueado (Error 404). En el Ataque 3 (Payload), se verificó que el formulario no envía IDs manipulables.

## Estado y Observaciones
*   **Estado:** `Aprobada`
*   **Observaciones:** Pruebas de seguridad e integridad superadas. El sistema no es vulnerable a IDOR. El backend mitiga el ataque usando `request.user.perfil`.

---
*Documentación generada por: Andrea Herrera (QA)*