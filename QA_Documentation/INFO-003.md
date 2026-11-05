# Reporte de Prueba QA: INFO-003

**ID del Caso:** INFO-003
**Módulo:** Información Personal
**Descripción:** Verificar el flujo principal de cambio de contraseña desde el perfil del empleado.
**Fecha:** 21-10-2026
**Tipo de Prueba:** Caja blanca — Cambio de contraseña

## Datos / Acciones de Entrada
Abrir el modal "Cambiar contraseña", ingresar contraseña actual, nueva contraseña y confirmación.

## Resultado Esperado
La contraseña se actualiza correctamente y el usuario mantiene su sesión activa.

## Resultado Obtenido
El sistema valida la contraseña actual, actualiza el registro de forma exitosa mostrando un mensaje de confirmación. La sesión del usuario permanece activa.

## Estado y Observaciones
*   **Estado:** `Aprobada`
*   **Observaciones:** Prueba del camino básico exitosa. No se presentan novedades.

---
*Documentación generada por: Andrea Herrera (QA)*