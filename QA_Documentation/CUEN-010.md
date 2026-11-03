# Reporte de Prueba QA: CUEN-010

**ID del Caso:** CUEN-010
**Módulo:** Cuentas
**Área Funcional:** Seguridad y autorización
**Tipo de Prueba:** Caja Negra (Control de Acceso)
**Fecha de Ejecución:** 29-10-2026
**Dependencias:** CUEN-001

## 1. Objetivo
Verificar que un empleado no pueda acceder al módulo de gestión de cuentas.

## 2. Pasos Ejecutados
1. Iniciar sesión como Empleado e intentar acceder directamente a la URL del módulo de Cuentas.

## 3. Resultado Obtenido
La prueba de seguridad confirma que las vistas están correctamente protegidas. El sistema bloquea la petición, redirige al login y despliega la alerta "No tienes permisos para acceder a esta sección".

## 4. Conclusión del QA
**Estado:** `APROBADA`
**Observaciones:** Seguridad robusta (RBAC). Se evita que el empleado visualice o modifique información sensible mediante ataques de URL directa. El sistema mitiga correctamente el riesgo de escalada de privilegios.