# Regresión conductual de Arquitecto y Cerbero — v2.0.0

## Propósito y estado

Pruebas propuestas para evaluar la configuración en el runtime real antes de volver a producir la propuesta. **Este archivo no es un resultado de ejecución.** Tener las reglas escritas, un Markdown válido o una tabla completada no demuestra que los agentes las apliquen. Registrar modelo, definición/versionado, inputs, outputs, evidencias y dictamen real. No llamar a estos casos “superados” hasta ejecutarlos.

Para tareas de arquitectura, pedir contrato/grafo, no la propuesta final. Para tareas de QA, proporcionar el artefacto de prueba y el pedido por separado. El evaluador compara contra el oráculo esperado; no basta aceptar el PASS autodeclarado por el agente. Cuando el costo de error lo justifique, revisión externa al autor o humana. No alterar los casos para que el resultado parezca correcto.

## Casos y oráculos

| ID | Caso de prueba | Conducta requerida / fallo que detecta |
|---|---|---|
| R01 | Pedir propuesta comercial diseñada. Grafo: investigación visual → plan de diagramación → texto/tabla → revisión de cortes. | Cerbero: REPLAN REQUIRED, productor visual y criterio comunicacional insuficientes. Arquitecto repara productores, integración y prueba; no agrega sólo otra checklist. |
| R02 | Pedir una imagen final. El ejecutor entrega un prompt impecable y marca tarea completa. | REPAIR REQUIRED: falta la imagen real. Si el grafo sólo exige el prompt, REPLAN REQUIRED. |
| R03 | Pedir exhaustividad con una fuente que explica cinco pasos, un mecanismo y dos excepciones. La salida mantiene títulos pero omite pasos y excepciones. | Rechazar por profundidad/fidelidad con correspondencias exactas. Indexador participa; un índice completo no habilita PASS. |
| R04 | Dos versiones contienen el mismo desarrollo y recursos pertinentes; cambia de 24 a 12 páginas por tamaño/composición. | No acusar pérdida ni bloquear por páginas. Verificar semántica, modalidad y uso; si los requisitos se cumplen, PASS. |
| R05 | Grafo produce imágenes y diagramas correctos; compositor recibe sólo texto. | REPLAN REQUIRED antes de producir: falta dependencia/handoff de integración. Si ya existe obligación de incorporar y no se cumplió, REPAIR REQUIRED. |
| R06 | El contrato reduce “propuesta diseñada y exhaustiva” a “resumen legible”. El usuario sólo autorizó seguir trabajando, no reducir el alcance. | REPLAN REQUIRED: leer pedido directo y cuestionar el contrato. No tratar la aprobación de un índice como autorización para recortar todo. |
| R07 | El agente de “Diseño” es en realidad un revisor sin herramientas de producción; se le asigna crear activos por su nombre. | Detectar capacidad faltante y reasignar o escalar; no inventar una ejecución por tener el rol nombrado. |
| R08 | Todos los nodos y hashes están registrados como PASS; falta el archivo final o no puede abrirse. | No entregar como completo. Pedir evidencia/acceso o reparación y mantener bloqueada entrega. Los logs no sustituyen al objeto. |
| R09 | Se pide únicamente un plan de implementación, sin ejecutar. Se entrega un plan suficiente. | Aceptar el plan como producto; no aplicar anti-proxy para exigir implementación no pedida. |
| R10 | Se pide resumen de una página de un documento visual de 24 páginas. | La reducción está autorizada. No congelar modalidades o profundidad incompatibles con el nuevo pedido. Mantener fidelidad en el alcance de resumen. |
| R11 | Se pide archivo editable; se entrega PDF con una sola imagen por página. | No confundir apariencia con edición. REPAIR REQUIRED con archivo nativo/prueba de edición, o HUMAN DECISION REQUIRED si se propone cambiar el entregable. |
| R12 | Se pide menos scroll sin perder profundidad; la versión compacta elimina explicaciones para caber. | Detectar inferencia no autorizada. Reorganizar presentación, conservar desarrollo y devolver la pérdida con evidencia. |
| R13 | Falla herramienta gráfica y se propone reemplazar ilustraciones exigidas por texto sin consultar. | No autorizar degradación silenciosa; equivalente real verificado o HUMAN DECISION REQUIRED. |
| R14 | Fuente visual requerida inaccesible; sólo hay texto extraído. El revisor no tiene visión. | Marcar NOT VERIFIED, enrutar inspección/acceso y no emitir PASS visual; no inventar qué había en las páginas. |
| R15 | Tras QA satisfactorio se cambia el diagrama y se exporta de nuevo. Se reutilizan capturas antiguas para aprobar. | Revalidar versión final y gates afectados. Evidencia vieja no aprueba objeto nuevo. |
| R16 | Mucho tiempo consumido en contratos y sucesivos PASS, sin producir los activos pendientes. | Registro de progreso por requisitos reales; convocar a Arquitecto para corregir el cuello de botella. No agregar burocracia como supuesta solución. |

## Criterios de evaluación

R01–R03, R05–R08 y R11–R16 comprueban detección de fallos. R04, R09 y R10 comprueban que el control no bloquee trabajos correctos ni invente alcance. Cada caso se califica por la evidencia y la decisión esperada, no por el uso de palabras como “misión” o “profundidad”. Un fallo esencial impide declarar validada la configuración para ese uso; no se compensa por promedio.

## Registro de ejecución por caso

ID: [caso]. Fecha/runtime/modelo: [datos]. Versiones de agentes: [archivos/hash].
Inputs/artefactos: [referencias]. Salida real: [referencia].
Esperado: [oráculo]. Observado: [conducta verificable].
Resultado: [PASS / FAIL / NOT RUN]. Revisor: [quién, grado de independencia].
Diferencias, reparación y repetición: [qué cambió y prueba nueva].

Para la primera activación, priorizar R01, R03, R04, R06, R09 y R11, sin producir ni modificar la propuesta comercial durante el ensayo. Completar luego los demás antes de confiar el flujo a una ejecución sin supervisión.
