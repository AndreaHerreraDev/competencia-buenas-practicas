# Reporte de Prueba QA: CUEN-008

**ID del Caso:** CUEN-008
**Módulo:** Cuentas
**Área Funcional:** Retiro de empleado
**Tipo de Prueba:** Prueba de Sistema
**Fecha de Ejecución:** 29-10-2026
**Dependencias:** CUEN-002

## 1. Objetivo
Verificar que el retiro de un empleado conserve su historial y cambie el estado correctamente.

## 2. Pasos Ejecutados
1. Desde el panel de Cuentas, presionar "Retirar empleado" y confirmar.
2. Intentar autenticarse con la cuenta retirada.

## 3. Resultado Obtenido
La interfaz muestra el modal de confirmación y notifica el éxito de la acción, garantizando la persistencia del historial. Al intentar autenticarse con la cuenta retirada, el sistema deniega el ingreso mostrando la alerta "Esta cuenta no está disponible".

## 4. Conclusión del QA
**Estado:** `APROBADA`
**Observaciones:** Prueba de sistema y de seguridad exitosa. La baja lógica del empleado protege la información histórica pero bloquea su acceso al sistema.