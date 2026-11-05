# Reporte de Prueba QA: INFO-001

**ID del Caso:** INFO-001
**Módulo:** Información Personal
**Descripción:** Verificar el flujo principal de acceso a la información personal del empleado.
**Fecha:** 21-10-2026
**Tipo de Prueba:** Caja blanca — Camino básico

## Datos / Acciones de Entrada
Iniciar sesión como Empleado y acceder al módulo "Información personal".

## Resultado Esperado
Se muestra el perfil con los datos personales, de contacto, de emergencia y laborales del empleado, en modo solo lectura excepto los campos editables.

## Resultado Obtenido
Se visualiza el perfil correctamente; los campos de nombre, correo, teléfono y cargo coinciden con la información del usuario.

## Estado y Observaciones
*   **Estado:** `Aprobada`
*   **Observaciones:** La vista carga correctamente y los datos mostrados son consistentes con la base de datos.

---
*Documentación generada por: Andrea Herrera (QA)*