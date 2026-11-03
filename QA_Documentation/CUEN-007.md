# Reporte de Prueba QA: CUEN-007

**ID del Caso:** CUEN-007
**Módulo:** Cuentas
**Área Funcional:** Suspensión de cuenta
**Tipo de Prueba:** Prueba de Sistema
**Fecha de Ejecución:** 29-10-2026
**Dependencias:** CUEN-002

## 1. Objetivo
Verificar que al suspender una cuenta el usuario afectado no pueda iniciar sesión.

## 2. Pasos Ejecutados
1. El administrador suspende la cuenta (ingresando el motivo).
2. El sistema confirma la acción.
3. Se intenta autenticar en el login con la cuenta suspendida. 

## 3. Resultado Obtenido
El sistema bloquea el acceso mostrando la alerta "Tu cuenta está suspendida. Contacta al administrador", validando la lógica del modelo y el control de acceso.

## 4. Conclusión del QA
**Estado:** `APROBADA`
**Observaciones:** Se validó el control de acceso. Se asume que el middleware y la auditoría operan de forma correcta tras bambalinas. La UX del mensaje de error es clara para el usuario.