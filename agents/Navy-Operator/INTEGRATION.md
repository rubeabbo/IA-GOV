# Integración de Navy-Operator

Navy-Operator es un agente de observabilidad, no una skill de redacción ni un aprobador. La definición en este repositorio no activa por sí sola un agente del runtime de Codex. Arquitecto debe incluirlo en el grafo como observador transversal; Codex debe invocarlo con acceso de lectura a contratos, eventos, artefactos y gates, y darle un canal visible de estado.

Handoff mínimo por evento (los nombres pueden adaptarse al runtime):
- run_id, occurred_at, graph_version, task_id, event_type, actor, invocation_evidence.
- artifact_ref, artifact_version, artifact_extent, artifact_status.
- gate_id, gate_status, gate_evidence, blocked_successors.
- interpretation_before, interpretation_after, proposer, decision_owner, decision_status.

El orquestador conserva el reloj de los 30 minutos y llama al agente al vencer. Debe existir sesión activa con scheduler/callback o bucle de ejecución persistente; un agente que termina su turno no seguirá enviando reportes por sí mismo. Actualizar el panel también al cambiar de nodo, terminar un activo, fallar un gate o replanificar, sin posponer el reporte periódico.

Prueba de activación: iniciar una ejecución de ensayo con grafo de dos nodos dependientes y un gate fallido. Verificar que el panel reproduzca la versión del grafo, marque el sucesor bloqueado y ubique exactamente el avance del artefacto. Registrar hora de comienzo; comprobar que se emita un reporte a los 30 minutos de ejecución activa y que una reinterpretación propuesta permanezca separada de una decisión aprobada. Si el ensayo dura menos, sólo se verifica el cierre, no la cadencia.

No trasladar archivos de contenido completo a una salida de estado; enlazar versiones y resumir lo necesario para Rube.
