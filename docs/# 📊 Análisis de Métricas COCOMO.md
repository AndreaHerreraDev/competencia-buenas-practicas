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
P = 26.93 / 8.6
P = 3.13 Personas


---

## 5. Resultados Obtenidos

| Métrica | Resultado |
| :--- | :--- |
| **Esfuerzo (E)** | 26.93 Persona-Mes |
| **Tiempo de Desarrollo (D)** | 8.6 Meses |
| **Personal Necesario (P)** | 3.13 Personas |

---

## 6. Interpretación de Resultados

- **Esfuerzo:** Se requieren aproximadamente **27 meses-persona** de trabajo para completar el proyecto. Esto significa que una sola persona tardaría 27 meses, o que 3 personas tardarían ~9 meses.
- **Tiempo:** El proyecto debería completarse en **8.6 meses** con el equipo actual.
- **Personal:** El equipo ideal es de **3.13 personas**. Dado que son 3 desarrolladores, el equipo está ligeramente por debajo de la estimación ideal, lo que implica un mayor esfuerzo individual.

### Comparación con la Realidad
Si el equipo ha estado trabajando durante **2 meses** (tiempo real transcurrido), el esfuerzo real sería:
Esfuerzo Real = 3 personas × 2 meses = 6 Persona-Mes


**Conclusión:** El equipo ha trabajado con una productividad **mayor** a la estimada por COCOMO, o el tamaño real del proyecto es menor a 10 KLOC. Esto es común en proyectos orgánicos donde el equipo tiene buena comunicación y los requisitos son flexibles.

---

## 7. Limitaciones del Análisis

1. **KLOC Estimado:** El tamaño del proyecto (10 KLOC) es una estimación basada en los módulos identificados, no en un conteo real de líneas de código.
2. **Coeficientes Estándar:** Se usaron los coeficientes originales de COCOMO 81. No se aplicaron los multiplicadores de esfuerzo (EM) para ajustar por complejidad, experiencia del equipo o uso de herramientas modernas.
3. **Proyecto en Desarrollo:** OperPan aún está en fase de desarrollo, por lo que el KLOC final podría variar.

---

## 8. Recomendaciones

1. **Realizar un conteo real de líneas de código** (usando herramientas como `cloc` o `tokei`) para obtener un KLOC más preciso.
2. **Aplicar los multiplicadores de esfuerzo (EM)** de COCOMO II para ajustar el cálculo según la experiencia del equipo y la complejidad del proyecto.
3. **Documentar el progreso** en el repositorio para comparar las estimaciones teóricas con el avance real.

---

*Documento generado AndreaHerreraDev · Octubre 2026*
