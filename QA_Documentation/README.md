# Portafolio de Quality Assurance (QA) - OperPan

Bienvenido a mi repositorio de documentación de pruebas de software. 
Aquí documento el proceso de aseguramiento de calidad (QA) del sistema de gestión de empleados "OperPan", actuando en el rol de QA y Developer.

## Módulos Probados:
1. **Información Personal (Perfil Empleado):** Pruebas de validación de datos, persistencia y seguridad (IDOR).
2. **Gestión de Tareas:** Pruebas de carga y consistencia de datos.

## Estructura del Repositorio:
* `QA_Documentation/`: Contiene los reportes detallados en formato Markdown.


# Módulo de Aseguramiento de Calidad (QA) - OperPan

Esta sección del repositorio contiene la documentación, evidencias y matrices de pruebas realizadas para garantizar la calidad del sistema OperPan.

## Índice de Pruebas

### Módulo de Tareas

* [TARE-001](TARE-001.md) - Validación de Panel de Tareas (Administrador).
* [TARE-002](TARE-002.md) - Creación y asignación de tareas (Administrador).
* [TARE-003](TARE-003.md) - Ciclo de vida de tareas (Empleado).
* [TARE-004](TARE-004.md) - Validación de horas límite en tareas (Administrador).
* [TARE-005](TARE-005.md) - Validación de fecha límite anterior a hoy (Administrador).
* [TARE-006](TARE-006.md) - Clasificación de tareas vencidas (Empleado).
* [TARE-007](TARE-007.md) - Reapertura de Tareas (Administrador).
* [TARE-008](TARE-008.md) - Memorandos automáticos (Administrador)
* [TARE-009](TARE-009.md) - Intento de ingreso con rol empleado a panel administrador, mediante la manipulación de la  URL (Empleado)


### Módulo de Cuentas
* [CUEN-001](CUEN-001.md) - Carga del panel y validación de indicadores.
* [CUEN-002](CUEN-002.md) - reporte CUEN-002 sobre creacion de cuenta y cambio de contraseña obligatorio.
* [CUEN-002](CUEN-002.md) - Visualización del detalle de un usuario desde módulo cuentas(Administrador).
* [CUEN-004](CUEN-004.md) - Validación de campos obligatorios vacíos.
* [CUEN-005](CUEN-005.md) - Validación de documento duplicado.
* [CUEN-006](CUEN-006.md) - Validación de nombre de usuario duplicado.
* [CUEN-007](CUEN-007.md) - Suspensión de cuenta y bloqueo de acceso.
* [CUEN-008](CUEN-008.md) - Retiro de empleado e historial.
* [CUEN-009](CUEN-009.md) - Reincorporación de empleado.
* [CUEN-010](CUEN-010.md) - Control de acceso al módulo de Cuentas.

### Módulo de Información Personal
* [INFO-001](INFO-001.md) - Carga del perfil (Camino básico).
* [INFO-002](INFO-002.md) - Edición de perfil (Bug de validación encontrado).
* [INFO-003](INFO-003.md) - Cambio de contraseña.
* [INFO-004](INFO-004.md) - Validación de correo inválido.
* [INFO-005](INFO-005.md) - Validación de teléfono inválido (Bug encontrado).
* [INFO-006](INFO-006.md) - Validación de contraseña (reglas mínimas).
* [INFO-007](INFO-007.md) - Persistencia de datos.
* [INFO-008](INFO-008.md) - Aislamiento de datos (Seguridad IDOR).
* [INFO-002-CORRECCIÓN](INFO-002-CORRECCION.md) - Retest: Corrección de bug de edición.
* [INFO-005-CORRECCIÓN](INFO-005-CORRECCION.md) - Retest: Corrección de bug de teléfono.



---
*Nota: La carpeta `Archivo_Practicas_Competencia` contiene ejercicios y documentación de prácticas previas relacionadas con bases de datos y migración, como parte de mi formación técnica.*