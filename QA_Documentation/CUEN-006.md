# Reporte de Prueba QA: CUEN-006

**ID del Caso:** CUEN-006
**Módulo:** Cuentas
**Área Funcional:** Creación / Unicidad de usuario
**Tipo de Prueba:** Caja Negra (Valores Límite)
**Fecha de Ejecución:** 05-11-2026
**Dependencias:** CUEN-002

## 1. Objetivo
Verificar que el sistema impida registrar dos cuentas con el mismo nombre de usuario (username).

## 2. Pasos Ejecutados
1. Abrir el modal de "Crear cuenta".
2. Llenar los datos.
3. Usar un nombre de usuario existente (`vivianagil`).
4. Intentar guardar.

## 3. Resultado Obtenido (Post-Fix)
*[Inserta la captura que me acabas de mostrar de los dos mensajes de error]*

**Descripción:** El sistema bloqueó la creación y mostró la notificación específica: "Error en username: Ese nombre de usuario ya existe". (Adicionalmente, detectó y notificó el documento duplicado al mismo tiempo).

## 4. Conclusión del QA
**Estado:** `APROBADA` ✅

**Observaciones:**
La corrección aplicada en el backend para el CUEN-005 (extracción de errores del `user_form` y `perfil_form`) resolvió también el manejo de errores para el `username`. El sistema es capaz de mostrar múltiples errores de validación simultáneamente, mejorando la Experiencia de Usuario (UX).

---
*Documentación generada por: Andrea Herrera (QA)*