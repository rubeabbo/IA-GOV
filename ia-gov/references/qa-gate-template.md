# QA GATE — plantilla v2.0.0

## Identificación

Gate/tarea/versión: [ID]. Revisor real y modo de revisión: [agente independiente / revisión humana / autorrevisión declarada].
Pedido humano y cambios autorizados: [referencia leída directamente].
Mission Contract, Execution Contract, grafo y fuentes: [versiones pertinentes].
Objeto inspeccionado: [archivo, render, datos, servicio o acción; ID/ruta/versión].
Evidencia de herramientas/ejecución: [traza del runtime o limitación; no sólo log autoescrito].

## Antes de producción: correspondencia misión–arquitectura

Fidelidad de intención: [verificado/fallo/no verificado y evidencia].
Requisitos con productor real: [matriz, huecos].
Proxies detectados: [plan/prompts/investigación sustituyendo producción].
Modalidad, profundidad e integración: [cadenas completas o faltantes].
Contraejemplo al grafo: [resultado localmente conforme pero globalmente incorrecto].
Decisiones/autorizaciones pendientes: [datos].
Si no aplica este gate previo, indicar qué gate anterior lo cubrió y si sigue vigente.

## Verificación de requisitos

| Requisito/origen | Esperado | Observado | Evidencia y localización | Estado | Severidad |
|---|---|---|---|---|---|
| R01 / [fuente] | [propiedad o ejecución] | [hecho, no intención] | [página/elemento/test/versionado] | VERIFIED / FAILED / NOT VERIFIED / NOT APPLICABLE | BLOCKER / MAJOR / MINOR / NOTE |

NOT APPLICABLE exige justificación de alcance. Un requisito esencial NOT VERIFIED no permite PASS. Separar cobertura temática, profundidad, fidelidad, cumplimiento comunicacional y corrección técnica. No usar el número de páginas/palabras/activos ni la presencia de títulos como sustituto de la comparación sustantiva.

Para visuales: render abierto, páginas/elementos inspeccionados, referencia visual y funciones requeridas. Para edición o funcionamiento: pruebas efectivamente realizadas y limitaciones. Un PASS previo, hash o tool call exitoso no acredita por sí solo el objetivo.

## Hallazgos, causa y reparación

Por hallazgo: ID, requisito vulnerado, evidencia, impacto, causa verificada o hipótesis, quién repara, acción específica, prueba de revalidación, intentos y dependientes afectados. No atribuir una omisión a un actor sin comprobar su tarea, contexto y output.

Versión revisada tras reparación: [identificador]. Gates invalidados/reutilizados: [cuáles y motivo].
Independencia y cobertura de auditoría: [qué se revisó realmente, qué no y por qué].

## Dictamen

Estado: **PASS / PASS WITH NON-BLOCKING ISSUES / REPAIR REQUIRED / REPLAN REQUIRED / HUMAN DECISION REQUIRED / STOP**.
Motivo sustentado: [requisitos y evidencia].
Puede avanzar: [nodos concretos]. Permanece bloqueado: [nodos y razón].
Siguiente responsable: [actor]. Decisión humana requerida: [sólo si corresponde].
En el gate final: [comparación directa del pedido contra producto integrado y destino].
No emitir PASS con BLOCKER, MAJOR o requisitos esenciales no verificados. No compensar un incumplimiento esencial promediando puntuaciones de otros requisitos.
