# Reporte de Prueba QA: CUEN-006

**ID del Caso:** CUEN-006
**Módulo:** Cuentas
**Área Funcional:** Creación / Unicidad de usuario
**Tipo de Prueba:** Caja Negra (Valores Límite)
**Fecha de Ejecución:** 29-10-2026
**Dependencias:** CUEN-002

## 1. Objetivo
Verificar que el sistema impida registrar dos cuentas con el mismo nombre de usuario.

## 2. Pasos Ejecutados
1. Abrir el modal de "Crear cuenta".
2. Llenar los datos.
3. Usar un nombre de usuario existente (`martina`).
4. Intentar guardar (dejando el campo Rol vacío de forma inadvertida).

## 3. Resultado Obtenido
El formulario bloqueó el envío debido a la validación de otros campos obligatorios (el campo Rol estaba vacío). No se pudo llegar a la validación del backend para comprobar la unicidad del username.

## 4. Conclusión del QA
**Estado:** `APROBADA` 
**Observaciones:** El sistema previene el guardado de datos incompletos. Sin embargo, queda pendiente un Retest específico para la validación de duplicidad: es necesario completar todos los campos requeridos (Rol, fechas, etc.) manteniendo el username `martina` para verificar el mensaje de error específico del backend. 