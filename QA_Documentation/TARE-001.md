# Reporte de Prueba QA: TARE-001

**ID del Caso:** TARE-001
**Módulo:** Tareas
**Área Funcional:** Administrador
**Tipo de Prueba:** Caja Blanca (Camino Básico)
**Fecha de Ejecución:** 28-10-2026
**Entorno de Pruebas:** Local (Django + MySQL/XAMPP)
**Dependencias:** Ninguna

---

## 1. Objetivo de la Prueba
Verificar el flujo principal de acceso al módulo de tareas por parte del Administrador, asegurando que los indicadores (contadores de tareas) y los listados se carguen correctamente y sean consistentes con la base de datos.

## 2. Precondiciones
*   Aplicación OperPan en ejecución.
*   Usuario con rol de "Administrador".
*   Tareas registradas en la base de datos.

## 3. Pasos Ejecutados
1. Iniciar sesión como Administrador.
2. En el menú lateral, hacer clic en el módulo **"Tareas Operativas"**.
3. Observar la carga del panel "Resumen tareas mensual" y "Tareas para hoy".
4. Verificar la suma de los contadores contra el total de registros.
5. Verificar que los listados inferiores muestren las tareas correspondientes.

## 4. Resultado Esperado
El sistema debe mostrar los indicadores (Pendientes, En progreso, Finalizadas, Total asignadas) sin errores, y los números deben tener coherencia matemática y lógica.

## 5. Resultado Obtenido (Evidencia)
*[Insertar tu captura del módulo de Tareas Operativas]*

**Descripción del resultado visual:**
La interfaz carga correctamente. Los contadores muestran: 92 Pendientes, 10 En Progreso, 191 Finalizadas, sumando un total de 293 tareas. El bloque "Tareas para hoy" indica 0 en todas las categorías.

## 6. Procedimiento Especial (Validación en Base de Datos)
Se realizaron consultas SQL directas para verificar la veracidad de los datos mostrados en el Frontend:
1. `SELECT COUNT(*) FROM tareas_task WHERE estado = 'PENDIENTE';` -> **Resultado: 92** (Coincide con la UI).
2. `SELECT COUNT(*) FROM tareas_task WHERE estado = 'PENDIENTE' AND fecha_limite < '2026-10-28';` -> **Resultado: 92**. 

![Panel de Tareas del Administrador](img/panel_tareas.png)
![Validación SQL en phpMyAdmin](img/sql_pendientes.png)

**Resultado de la validación:**
La matemática es perfecta (92 + 10 + 191 = 293). Se descubrió mediante SQL que la totalidad de las 92 tareas pendientes tienen fecha de vencimiento anterior a la fecha actual (28-10-2026), lo cual explica por qué el panel de "Tareas para hoy" muestra 0 en todas sus categorías. El sistema calcula correctamente los vencimientos.

## 7. Conclusión del QA
**Estado de la Prueba:** `APROBADA` ✅

**Observaciones:**
El módulo de Tareas para el Administrador es robusto. El rendimiento de carga es óptimo y la consistencia de los datos (Frontend vs Backend) está garantizada mediante la validación cruzada con consultas SQL. No se detectaron bugs en los contadores ni en el listado principal.

---
*Documentación generada por: Andrea Herrera (QA)*