# Propuesta de Desarrollo: Modelo 4P + T

## 1. Descripción general del sistema
**a. Nombre:** Los Brosgaming.
**b. Problema que resuelve:** Actualmente, los talleres de reparación de consolas en Ciudad Juárez carecen de un control digital de refacciones. Esto provoca errores al comprar piezas incompatibles, pérdida de stock y descontrol en el inventario.
**c. Usuarios principales:** Administrador (control de inventario), Técnico (consulta de piezas) y Cliente (consulta de precios).
**d. Objetivo general:** Desarrollar una plataforma para centralizar y automatizar el inventario de refacciones, asegurando la compatibilidad técnica por modelo de consola para optimizar las reparaciones y ventas.

## 2. Procesos (de la aplicación)
**a. Proceso de desarrollo:**
- **i. Metodología de desarrollo elegida:** SCRUM.
- **ii. Justificación:** Se elige SCRUM por ser una metodología ágil que permite la colaboración en equipo a través de ciclos de trabajo (Sprints). Facilita la adaptación a cambios y permite que cada integrante avance de forma independiente usando Jira y GitHub.

**b. Actividades principales:**
- **i. Análisis:** Reunir requisitos con entrevistas a técnicos y administradores. Escribir historias de usuario.
- **ii. Diseño:** Definir criterios de aceptación y modelado de la base de datos para relacionar piezas con consolas. Diseño de interfaz.
- **iii. Desarrollo:** Codificación de la lógica del inventario, revisiones de código e integración continua.
- **iv. Pruebas:** Pruebas funcionales con datos de consolas y validación de que el sistema descuenta correctamente el stock. Pruebas de aceptación con técnicos reales.
- **v. Entrega:** Despliegue a producción, capacitación para los usuarios y entrega de documentación/manuales.

**c. Flujo de trabajo:** *(Nota: El diagrama de flujo visual se encuentra anexado en la documentación PDF del proyecto, mostrando el proceso desde que se recibe la consola hasta la actualización del inventario).*

**d. Control de calidad:**
- **i. ¿Cómo evitarán errores?:** Exigiendo que cada historia tenga código, pruebas y revisión aprobada antes de cerrarse. Revisiones de código por al menos otro desarrollador, backups de la base de datos y validación de datos desde el servidor.
- **ii. ¿Qué prácticas utilizarán?:** Empezar con pruebas para funciones críticas (cálculo de stock), checklist de despliegue con opción a rollbacks, revisión en pares y registro estricto de incidencias (bugs) en Jira.

## 3. Proyecto
**a. Definición del proyecto:**
- **i. Alcance:** Gestionar el inventario de refacciones dentro de un taller. Permitirá registrar piezas, consultar compatibilidad y controlar el stock. No incluirá pagos en línea ni comercio electrónico externo.
- **ii. Entregables:** Repositorio de código fuente, base de datos configurada, software funcional, y manual de operación para administradores y técnicos.

**b. Planificación básica (en Jira):**
- **i. Cronograma (6 semanas simuladas):**
  - Semana 1: Análisis de requerimientos, configuración de Jira/GitHub y diseño de Base de Datos.
  - Semana 2: Diseño de interfaz de usuario e inicio de programación de la estructura.
  - Semana 3: Desarrollo del módulo de registro de inventario (Administrador).
  - Semana 4: Desarrollo del módulo de consulta y compatibilidad (Técnicos/Clientes).
  - Semana 5: Integración del sistema y periodo de pruebas funcionales (resolución de bugs).
  - Semana 6: Pruebas de aceptación finales, documentación y despliegue.
- **ii. Fases:** Sprint 0 (Planeación), Sprint 1 (Backend/BD), Sprint 2 (Frontend y Lógica), Sprint 3 (Pruebas y Cierre).

**c. Recursos:**
- **i. Humanos:** Equipo de desarrollo organizado en Líder del proyecto, Desarrolladores, Tester y Encargado de documentación.
- **ii. Técnicos:** Computadoras personales, internet, GitHub, Jira y lenguajes de programación.

**d. Riesgos identificados:**
1. **Retraso en la integración del equipo:** *Mitigación:* Establecer fechas límite estrictas para alta en plataformas.
2. **Curva de aprendizaje de herramientas:** *Mitigación:* El líder de proyecto proporcionará una guía rápida de GitHub/Jira.
3. **Información técnica errónea:** *Mitigación:* Validar cada entrada con manuales oficiales de las consolas.
4. **Pérdida de avances de código:** *Mitigación:* Uso obligatorio de "Branches" (ramas) en GitHub.
5. **Incumplimiento de fechas en tareas:** *Mitigación:* Revisión semanal del tablero Kanban para destrabar tareas estancadas.

**e. Métricas del proyecto:**
- **i. Tiempo:** 6 semanas (simuladas en la planeación).
- **ii. Costo estimado:** $0 MXN (uso de herramientas Open Source y capas gratuitas).
- **iii. Indicadores de avance:** Porcentaje de incidencias movidas a "Finalizado" en Jira y cantidad de "commits" en la rama principal de GitHub.

## 4. Personas
**a. Roles:**
- **Alex:** Líder del Proyecto / Scrum Master.
- **David:** Desarrollador y Encargado de Documentación.
- **Oscar:** Encargado de Pruebas (Tester).
- **Kenneth:** Desarrollador (Backend y Base de Datos).
- **Osiel:** Desarrollador (Frontend e Interfaz).

**b. Responsabilidades:** El líder coordina, organiza tareas y elimina bloqueos. Los desarrolladores programan las funcionalidades, estructuran la base de datos y diseñan las pantallas. El tester diseña y ejecuta pruebas para cazar errores y validar el sistema. El encargado de documentación redacta reportes, manuales y mantiene el repositorio.

**c. Estrategia de comunicación:** Comunicación asíncrona a través de comentarios en los tickets de Jira para temas técnicos, y reuniones semanales (Daily/Weekly Scrum) de 15 a 45 minutos para sincronización.

**d. Reglas internas del equipo:** Todos los miembros deben mantener actualizado el estatus de sus tareas en Jira. Ningún código sube a la rama principal (main) en GitHub sin ser revisado por al menos otro integrante.

**e. Reglas para el manejo de conflictos:** Si hay desacuerdos técnicos, se somete a votación fundamentada en documentación oficial. Si alguien se atrasa con una entrega, se le reasignan temporalmente tareas de menor prioridad para que el equipo lo apoye a nivelar el avance general.

## 5. Producto
**a. Funcionalidades principales:** Registro de refacciones, búsqueda de compatibilidad de piezas por modelo de consola, apartado de piezas (ticket) y visualización en tiempo real del stock.
**b. Requisitos Básicos:** El sistema debe diferenciar vistas entre Administrador, Técnico y Cliente. Debe actualizar el stock automáticamente al apartar una pieza.
**c. Características del software:** Interfaz intuitiva, despliegue local o web ligero, respuesta rápida en búsquedas y alta fiabilidad en los datos de compatibilidad.
**d. Criterios de calidad:** El sistema no debe permitir apartar una refacción si el stock está en cero. Las búsquedas por modelo no deben tardar más de 2 segundos. Todo código debe pasar las pruebas unitarias.
**e. ¿Qué haría que el producto fracase?:** Que la base de datos inicial se llene con compatibilidades incorrectas, causando que los técnicos compren piezas que no sirven para la consola reparada. También fracasaría si la interfaz es demasiado compleja y los técnicos prefieren seguir usando papel.

## 6. Tecnología
**a. Lenguaje elegido:** C++ (para la lógica estructurada y rendimiento) y Python.
**b. Herramientas:** Base de datos en MySQL. Jira para la gestión ágil del proyecto.
**c. Control de versiones:** Repositorio en GitHub utilizando el sistema de ramas (branches) y Pull Requests.
**d. Herramientas de prueba:** Frameworks de pruebas unitarias compatibles con el lenguaje elegido y pruebas manuales de caja negra.
**e. Infraestructura:** Entorno local en las computadoras del equipo para el desarrollo, utilizando servidores locales para simular la conexión a la base de datos MySQL.
