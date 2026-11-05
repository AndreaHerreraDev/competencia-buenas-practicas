# Reporte de Prueba QA: INFO-005

**ID del Caso:** INFO-005
**Módulo:** Información Personal
**Descripción:** Verificar que el sistema rechace la edición del perfil cuando el teléfono no cumpla con el formato esperado.
**Fecha:** 21-10-2026
**Tipo de Prueba:** Caja negra — Valores límite

## Datos / Acciones de Entrada
Intentar guardar un teléfono vacío o con caracteres no numéricos.

## Resultado Esperado
El sistema rechaza la edición con un mensaje específico.

## Resultado Obtenido
El sistema bloquea letras y caracteres especiales, pero permite guardar el perfil con el campo de teléfono vacío y permite guardar números con longitud menor a la mínima (ej. '123').

## Estado y Observaciones
*   **Estado:** `Fallida`
*   **Observaciones:** Dos Bugs detectados: 1. El campo Teléfono no es obligatorio en el HTML ni en el Backend. 2. No hay validación de longitud mínima para el teléfono. Se requiere ajustar el código.

---
*Documentación generada por: Andrea Herrera (QA)*