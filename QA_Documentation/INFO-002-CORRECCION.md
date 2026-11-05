# Reporte de Prueba QA: INFO-002-CORRECCIÓN (Retest)

**ID del Caso:** INFO-002-CORRECCIÓN
**Módulo:** Información Personal
**Descripción:** Retest del bug de validación en edición de perfil (Teléfono y Ciudad).
**Fecha:** 23-10-2026

## Resultado Obtenido
Se verifica la corrección del bug. El sistema bloquea activamente el ingreso de caracteres alfabéticos en el teléfono y numéricos en la ciudad, mostrando el mensaje de validación nativo del navegador. Los datos válidos se guardan correctamente.

## Estado y Observaciones
*   **Estado:** `Aprobada`
*   **Observaciones:** Bug solucionado (Retest exitoso). Como Dev: Se implementaron validaciones en Frontend (HTML `pattern` y JS) y Backend (Django). Como QA: Se verificó que el sistema impide el guardado de datos inválidos.

---
*Documentación generada por: Andrea Herrera (QA)*