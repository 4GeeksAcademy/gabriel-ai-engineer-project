---
name: healthcore-patient-data-flow-review
description: Revisa un flujo propuesto de datos de pacientes de HealthCore frente al contexto y las restricciones jurisdiccionales descritas en el briefing. Úsala al diseñar o cambiar sistemas que almacenen, accedan o compartan datos de pacientes en EE.UU., el Reino Unido o ambos.
---

# Revisión de flujos de datos de pacientes de HealthCore

## Objetivo

Producir una revisión trazable de brechas e incógnitas para **un flujo propuesto de datos de pacientes**, considerando por separado HIPAA para EE.UU. y UK GDPR para el Reino Unido cuando apliquen. Esta revisión no es asesoría legal, una evaluación formal ni una certificación de cumplimiento.

## Inputs requeridos

Solicita o identifica en la propuesta:

1. **Propósito y alcance** del flujo.
2. **Jurisdicción o sedes** involucradas: EE.UU., Reino Unido, ambas o no especificado.
3. **Tipos de datos de pacientes** y su nivel de sensibilidad; describe categorías, no incluyas registros reales identificables.
4. **Origen y destino** de los datos, incluyendo sistemas EHR u otros sistemas involucrados.
5. **Acceso y uso:** quién accede y para qué.
6. **Almacenamiento, compartición y retención/eliminación** previstas.
7. **Auditoría:** qué accesos y cambios se registran y cómo se consultan.
8. Documentación técnica o políticas pertinentes disponibles.

Si un dato no está disponible, regístralo como **No especificado**. No lo deduzcas ni inventes. Si la solicitud incluye datos reales identificables de pacientes, no los reproduzcas en el análisis; pide una descripción redactada o datos sintéticos.

## Procedimiento

1. Resume el propósito y dibuja en texto el recorrido origen → procesamiento → destino, usando solo los componentes indicados.
2. Determina qué jurisdicciones aplican a partir de los inputs. Si no se puede determinar, marca la jurisdicción como **No especificado**.
3. Revisa por separado los aspectos descritos para HIPAA (EE.UU.) y UK GDPR (Reino Unido), según el alcance. Considera almacenamiento, acceso, compartición y auditoría; las reglas pueden diferir entre jurisdicciones.
4. Contrasta el diseño con los hechos del briefing: los dos EHR no se comunican, no hay capa de datos compartida, los registros de acceso están separados, las pistas de auditoría son incompletas y las solicitudes de datos requieren trabajo manual.
5. Para cada aspecto, asigna uno de estos estados:
   - **Evidencia proporcionada:** el input describe cómo se aborda el aspecto; esto no significa cumplimiento legal.
   - **Brecha identificada:** el input describe una carencia o contradicción con una necesidad del briefing.
   - **No evaluable:** falta información suficiente.
6. Enumera las preguntas o evidencias necesarias para resolver cada estado **No evaluable**. Deriva decisiones de cumplimiento a Claire Whitfield; no emitas conclusiones legales.

## Formato de salida

1. **Resumen del flujo** y jurisdicciones indicadas.
2. **Matriz de revisión** con columnas: aspecto, HIPAA (EE.UU.), UK GDPR (Reino Unido), evidencia del input y preguntas/acciones pendientes.
3. **Brechas y riesgos operativos** identificados, vinculados a evidencia concreta.
4. **Información faltante** y decisiones que requieren revisión de Cumplimiento y Gobierno del Dato.
5. **Límite de la revisión:** indicar que no certifica cumplimiento legal.

No repitas datos personales de pacientes en la salida. No propongas transferencias transfronterizas ni controles técnicos como si estuvieran aprobados por el briefing.

## Criterios de aceptación verificables

- [ ] Se analiza un único flujo, con propósito y recorrido descritos o marcados **No especificado**.
- [ ] Las jurisdicciones están identificadas a partir de los inputs o marcadas **No especificado**.
- [ ] HIPAA y UK GDPR se evalúan en columnas separadas cuando corresponda; lo no aplicable o no determinable queda explícito.
- [ ] Almacenamiento, acceso, compartición y auditoría aparecen en la matriz; cada aspecto sin evidencia queda marcado **No evaluable**.
- [ ] Cada brecha o evidencia está vinculada a un dato de entrada o a un hecho del briefing; no se agregan supuestos como hechos.
- [ ] La salida incluye preguntas/acciones pendientes y deriva las decisiones de cumplimiento a Claire Whitfield.
- [ ] La salida no reproduce datos identificables de pacientes ni afirma o certifica cumplimiento legal.
