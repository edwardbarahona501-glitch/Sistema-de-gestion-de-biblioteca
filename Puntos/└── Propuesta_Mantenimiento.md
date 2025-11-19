# 📚 Propuesta de Plan de Mantenimiento (Sistema de Gestión de Biblioteca)

## 📊 Tipo de Mantenimiento Seleccionado: Mantenimiento Perfectivo

**Motivo de la Selección:** El sistema actual es funcional, pero las pruebas de rendimiento y el feedback de los bibliotecarios indican que la **búsqueda de libros** es lenta en grandes volúmenes de datos. Además, se necesita mejorar la **interfaz de registro de nuevos usuarios** para reducir errores de captura.

### 🎯 Objetivo Principal

Optimizar la velocidad de las consultas de búsqueda de la base de datos en un **mínimo de 50%** y mejorar la experiencia del usuario (UX) en los formularios clave para reducir el tiempo de operación del personal.

---

### 📝 Tareas Detalladas y Fases

| Fase | Tarea Específica | Prioridad | Estimación |
| :--- | :--------------- | :-------- | :--------- |
| **Diagnóstico** | Analizar las consultas SQL más lentas (usando `EXPLAIN`), auditar índices y recopilar feedback sobre la UX del formulario. | Alta | 10 horas |
| **Optimización de BD** | Implementar índices compuestos en tablas clave (`Libros`, `Ejemplares`, `Usuarios`) y refactorizar consultas lentas. | Crítica | 25 horas |
| **Refactorización UI/UX** | Rediseñar el formulario de alta de usuario (validación en tiempo real, campos obligatorios claros) y aplicar cache a los resultados de búsqueda. | Alta | 20 horas |
| **Pruebas (QA)** | Pruebas de carga para validar la mejora de velocidad y pruebas funcionales de los nuevos formularios. | Crítica | 15 horas |
| **Despliegue** | Despliegue de la nueva versión en el entorno de producción durante un horario de bajo uso. | Media | 2 horas |

---

### 🔄 Impacto y Riesgos

* **Impacto Esperado:**
    * Tiempo de respuesta de búsqueda reducido, mejorando la eficiencia del bibliotecario.
    * Menos errores de captura de datos de usuarios.
    * Mejor experiencia general para el personal.

* **Riesgo Potencial:** La creación de nuevos índices puede ralentizar ligeramente las operaciones de inserción de datos.
* **Mitigación:** Se realizará un monitoreo de las operaciones de inserción para asegurar que el impacto sea mínimo y aceptable frente a la ganancia en la velocidad de búsqueda.

---

**Próximos Pasos:** Se requiere la aprobación formal para iniciar la fase de **Diagnóstico y Optimización de BD**, con un total de **72 horas** de trabajo estimadas.
