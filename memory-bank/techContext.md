# Contexto técnico - HealthCore Digital

## Ubicación del código de producto

- [`uis/`](../uis/): proyectos frontend de la empresa.
- [`uis/website/`](../uis/website/): web corporativa pública de HealthCore; su página de entrada será `/` y su marca y contenido deben alinearse con el [briefing](../CONTEXT-healthcore-briefing.es.md).
- [`uis/backoffice/`](../uis/backoffice/): aplicación interna de HealthCore, con layout propio separado de la web pública y vista de entrada en `/`.
- [`services/`](../services/): APIs, workers y demás servicios backend; cada subcarpeta corresponde a un servicio concreto.

Estas ubicaciones definen dónde desarrollar los productos, no implican que ya estén implementados. Sigue los README de la plantilla y no crees otro árbol paralelo para frontend o APIs.

## Sistemas actuales conocidos

- **EHR:** dos plataformas distintas, una en EE.UU. y otra en el Reino Unido; no se comunican entre sí.
- **Facturación:** plataforma en EE.UU.; hoja de cálculo para el Reino Unido.
- **Citas:** programación por teléfono en EE.UU.; agenda manual en el Reino Unido. No existe un sistema compartido de reservas online.
- **Datos y operaciones:** no hay capa de datos compartida ni telemetría o registro centralizado. El equipo suele enterarse de fallos cuando una clínica los reporta.

Los nombres de productos, proveedores, interfaces y versiones no están especificados en el briefing.

## Capacidades que HealthCore necesita

El briefing plantea como necesidades, no como componentes ya implementados o decisiones técnicas cerradas:

- Una API central para unificar datos de pacientes, citas, facturación y personal de ambos sistemas EHR.
- Telemetría y monitorización desde las 12 sedes.
- Un pipeline de datos para dashboards clínicos, operacionales y financieros.
- Chequeos de salud automatizados, alertas y documentación técnica indexada para búsqueda semántica.

## Restricciones y contexto

- HealthCore opera en EE.UU. y el Reino Unido, bajo HIPAA y UK GDPR respectivamente. Los sistemas que gestionan datos de pacientes deben evaluarse según las obligaciones aplicables en cada jurisdicción.
- Las reglas sobre almacenamiento, acceso y compartición de datos de pacientes difieren entre ambos marcos.
- Los registros de acceso están separados entre los sistemas EHR, las pistas de auditoría están incompletas y las solicitudes de datos de pacientes requieren trabajo manual en varios sistemas.
- La red comprende 12 clínicas: 9 en EE.UU. y 3 en el Reino Unido. El equipo de Tecnología tiene seis personas en Austin.

## Usos de IA mencionados

- Asistencia a la documentación clínica, que actualmente consume 35 minutos diarios del personal clínico.
- Predicción de citas con riesgo de no-show, cuya tasa actual en la red es del 22%.
- Revisión de reclamaciones y sugerencias de codificación; la tasa de rechazo en EE.UU. es del 14%.
- Monitorización de cumplimiento y búsqueda RAG sobre documentación de cumplimiento en dos jurisdicciones.

El briefing describe estos casos como necesidades o desafíos; no especifica modelos, datos de entrenamiento, proveedores ni controles técnicos implementados.

## Información técnica no especificada

El briefing no determina lenguajes, frameworks, bases de datos, hosting, proveedores EHR, APIs disponibles, estándares de interoperabilidad, controles técnicos concretos, presupuesto ni cronograma. Esos elementos requieren investigación y decisión; no deben tratarse como elecciones ya tomadas.
