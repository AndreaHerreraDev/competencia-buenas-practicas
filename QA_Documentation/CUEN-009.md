# Reporte de Prueba QA: CUEN-009

**ID del Caso:** CUEN-009
**Módulo:** Cuentas
**Área Funcional:** Reincorporación
**Tipo de Prueba:** Prueba de Sistema
**Fecha de Ejecución:** 29-10-2026
**Dependencias:** CUEN-008

## 1. Objetivo
Verificar que un empleado retirado pueda ser reincorporado y que su estado se actualice correctamente.

## 2. Pasos Ejecutados
1. Presionar "Reincorporar" sobre un empleado en estado "Retirado".

## 3. Resultado Obtenido
La acción se ejecuta correctamente mostrando la notificación de éxito ("felipe fue reincorporado"). El estado en la tabla se actualiza inmediatamente a "Pendiente".

## 4. Conclusión del QA
**Estado:** `APROBADA`
**Observaciones:** Lógica de transición de estados correcta. El sistema permite reincorporar al empleado, cambiando su perfil a activo y gestionando su cuenta como "Pendiente" para garantizar un nuevo acceso seguro.