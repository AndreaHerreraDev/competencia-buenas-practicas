# Reporte de Prueba QA: INFO-007

**ID del Caso:** INFO-007
**Módulo:** Información Personal
**Descripción:** Verificar que los cambios guardados en el perfil persistan al cerrar sesión y volver a iniciarla.
**Fecha:** 21-10-2026
**Tipo de Prueba:** Caja negra — Prueba de sistema

## Datos / Acciones de Entrada
Modificar un dato de contacto, guardar, cerrar sesión y volver a iniciarla.

## Resultado Esperado
El dato modificado se conserva correctamente.

## Resultado Obtenido
El dato modificado ('QA TEST PERSISTENCIA') se conserva correctamente tras cerrar e iniciar sesión. Adicionalmente, se verificó mediante phpMyAdmin que el registro se actualizó en la base de datos.

## Estado y Observaciones
*   **Estado:** `Aprobada`
*   **Observaciones:** Prueba de persistencia y base de datos exitosa. El guardado se refleja correctamente tanto en la interfaz como en el motor de la base de datos.

---
*Documentación generada por: Andrea Herrera (QA)*