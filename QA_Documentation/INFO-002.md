# Reporte de Prueba QA: INFO-002

**ID del Caso:** INFO-002
**Módulo:** Información Personal
**Descripción:** Verificar la funcionalidad de edición del perfil, validando que el empleado pueda modificar sus datos y guardarlos correctamente.
**Fecha:** 21-10-2026
**Tipo de Prueba:** Caja blanca — Edición del perfil

## Datos / Acciones de Entrada
Abrir el modal "Editar perfil", modificar género, estado civil, teléfono, correo, dirección, ciudad y contacto de emergencia, y guardar.

## Resultado Esperado
El modal de edición se cierra y se reflejan los nuevos datos en la pantalla principal.

## Resultado Obtenido
Múltiples fallas de validación en pestaña 'Contacto': 1. El campo 'Teléfono' permite el ingreso de letras (ej. UYGUUB3333) y las guarda. 2. El campo 'Ciudad' permite el ingreso de valores puramente numéricos (ej. 2315465).

## Estado y Observaciones
*   **Estado:** `Fallida`
*   **Observaciones:** Bug detectado. Se requiere implementar validaciones (frontend y backend) para restringir los tipos de datos según corresponda a cada campo.

---
*Documentación generada por: Andrea Herrera (QA)*