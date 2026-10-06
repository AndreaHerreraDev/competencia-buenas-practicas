# 📊 Análisis de Métricas COCOMO - OperPan

Este documento detalla la aplicación del modelo **COCOMO (Constructive Cost Model)** al proyecto **OperPan**, un sistema de gestión de personal desarrollado para la panadería **Estación Paisa**.

---

## 1. Clasificación del Proyecto

Según el modelo COCOMO Original (Barry Boehm, 1981), los proyectos se clasifican en tres tipos: **Orgánico**, **Semi-acoplado** y **Empotrado**. 

OperPan se clasifica como un proyecto **ORGÁNICO** debido a las siguientes características:

| Característica | OperPan | Justificación |
| :--- | :--- | :--- |
| **Tamaño del equipo** | 3 desarrolladores | Equipo pequeño (2-5 personas). |
| **Tamaño del proyecto** | ~10 KLOC (estimado) | Menos de 50 KLOC. |
| **Requisitos** | Flexibles | Proyecto interno para una panadería local. |
| **Experiencia del equipo** | Mixta | Equipo en formación, con conocimiento en Django y MySQL. |
| **Entorno** | Controlado | Sin restricciones de hardware extremas ni sistemas legados. |
| **Complejidad** | Media-Baja | Aplicación web estándar (CRUDs, autenticación, reportes). |

---

## 2. Estimación del Tamaño (KLOC)

Para aplicar las fórmulas de COCOMO, primero se estimó el tamaño del proyecto en **KLOC** (miles de líneas de código).

| Módulo | Líneas de Código Estimadas |
| :--- | :--- |
| Configuración Django (settings, urls, wsgi) | 500 |
| Módulo de Usuarios (login, roles, permisos) | 1,500 |
| Módulo de Asistencia (entrada/salida) | 1,200 |
| Módulo de Solicitudes (permisos, vacaciones) | 1,000 |
| Módulo de Certificados (PDFs) | 800 |
| Módulo de Notificaciones (API Gmail) | 1,000 |
| Frontend (HTML, CSS, JS) | 2,500 |
| Homepage (index.html, style.css, theme-home.css, index.js) | 1,500 |
| **Total Estimado** | **~10,000 líneas** |

**Tamaño = 10 KLOC** (10,000 líneas de código).

---

## 3. Coeficientes COCOMO (Orgánico)

Para un proyecto de tipo Orgánico, los coeficientes son:

| Coeficiente | Valor |
| :--- | :--- |
| **a** | 2.4 |
| **b** | 1.05 |
| **c** | 2.5 |
| **d** | 0.38 |

---

## 4. Fórmulas Aplicadas

### 4.1 Esfuerzo (E)
> **E = a × (KLOC)^b**

**Cálculo:**
