# Reporte de Prueba QA: INFO-004

**ID del Caso:** INFO-004
**Módulo:** Información Personal
**Descripción:** Verificar que el sistema rechace la edición del perfil cuando el correo tenga formato inválido.
**Fecha:** 21-10-2026
**Tipo de Prueba:** Caja negra — Valores límite

## Datos / Acciones de Entrada
Intentar guardar un correo sin arroba o sin dominio.

## Resultado Esperado
El sistema rechaza la edición con un mensaje indicando que el correo no es válido.

## Resultado Obtenido
El navegador bloquea el envío del formulario al detectar un formato de correo inválido, mostrando un mensaje de advertencia.

## Estado y Observaciones
*   **Estado:** `Aprobada`
*   **Observaciones:** Prueba de valores límite exitosa. La etiqueta type='email' del HTML cumple su función.

---
*Documentación generada por: Andrea Herrera (QA)*