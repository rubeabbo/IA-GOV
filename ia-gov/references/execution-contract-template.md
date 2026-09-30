# EXECUTION CONTRACT — plantilla v2.0.0

## Encargo y versiones

ID/versión del contrato y grafo: [datos].
Pedido original y Mission Contract: [referencias accesibles/versionadas].
Objetivo, producto final y nivel IA-Gov: [resultado, formato/destino, N0–N6 justificado].
Fuentes e invariantes: [referencias, qué conservar, profundidad y modalidades aplicables].
Decisiones abiertas/cerradas: [autorizaciones y límites de interpretación].

## Cobertura de la misión

| Requisito | Productor/nodo | Artefacto o acción real | Nodo de integración/destino | Validador/gate | Prueba y evidencia requerida |
|---|---|---|---|---|---|
| R01 | [rol con capacidad verificada] | [tipo, contenido, versión/ruta esperada] | [quién lo incorpora o por qué no aplica] | [responsable] | [prueba sobre objeto real] |

Un requisito puede requerir varios nodos; un nodo puede satisfacer varios requisitos. Cada cadena debe llegar al producto final. Investigación/plan no cierra una obligación de producción. Los requisitos de proceso se verifican con evidencia de ejecución.

## Actores, herramientas y contexto

Por actor: rol/definición/versionado, misión local, puede interpretar/modificar, no puede modificar, input y fuentes necesarias, output, herramientas disponibles y permisos, prueba, handoff y fallback. Registrar cómo se comprobó capacidad, instalación y acceso. No asumir que nombres o archivos .md acreditan un agente ejecutable.

Especialistas semánticos/visuales/técnicos: [owners no superpuestos sin explicación].
Productores materiales y compositor/integrador: [obligación concreta de producir e incorporar].
Contexto excluido por privacidad o irrelevancia: [clasificación y minimización].
Principal, alternativa y contingencia: [disparador; equivalencia y autorización necesarias].

## Grafo y prompt de cada tarea

Representar con IDs estables en Markdown, YAML o JSON según el runtime. Cada nodo declara:

```yaml
task_id: T01
type: production  # research / planning / production / integration / validation / delivery
owner: ROL_VERIFICADO
mission_requirements: [R01]
depends_on: []
required_predecessor_gates: []
inputs: []  # referencias/versiones; incluir imágenes u otros activos cuando sean necesarios
task: ACCION_CONCRETA
cannot_change: []
tools_and_permissions: []
outputs: []  # tipo de artefacto, contenido, ruta esperada y propiedades; no sólo "informe"
incorporated_by: NODO_O_DESTINO
acceptance_tests: []
cerbero_gate: C_T01
fallback: CONDICION_Y_ACCION
```

El ejemplo contiene marcadores: no es un grafo ejecutado. Evitar ciclos y dependencias implícitas. Definir arranque, ramas paralelizables, sincronización, estados y condiciones de bloqueo. El prompt local incluye el objetivo global mínimo, fuente de verdad, invariantes, tarea, límites, salida, prueba, handoff y recuperación, sin obligar a reconstruir toda la arquitectura.

## Gates e intervención humana

Preproducción: MISSION COVERAGE GATE de Cerbero, contrastado con pedido y fuentes, no sólo contrato.
Intermedios: cada tarea/subtarea relevante exigida, con evidencia y bloqueo de dependientes.
Final: producto integrado → criterios globales de misión, contenido/profundidad, modalidad, edición/función y entrega aplicables.
Intervención humana: [decisiones, autorizaciones y cambios materiales; quién decide].
No liberar un sucesor hasta que el artefacto predecesor y su gate sean habilitantes.

## Prueba de suficiencia y recuperación

Contraejemplo buscado: [producto que cumpliría todos los nodos pero incumpliría la misión].
Huecos encontrados y reparados: [requisitos, productores, integración, pruebas].
Riesgos restantes: [no confundir un plan consistente con garantía de ejecución].
Reintentos/presupuesto: [dos intentos por actor para un mismo defecto, salvo límite acordado; luego cambio/escalamiento].
Replanificación: [disparadores, dueño, versionado, diferencias y gates afectados].

## Salida y trazabilidad

Condición de salida: [artefactos reales, prueba, destino, ningún bloqueo esencial, gate final].
Registro mínimo: tarea, agente/modelo real si consta, herramientas, inputs/outputs/versiones, errores, fallback, decisiones y evidencia del gate. Medir costos/tiempos sólo cuando existan datos. Los registros administrativos no prueban calidad ni invocación por sí solos.
Estado actual: [pendiente de Cerbero / aprobado / bloqueado]; evidencia del gate: [referencia].
