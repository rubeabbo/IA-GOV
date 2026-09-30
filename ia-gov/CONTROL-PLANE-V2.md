# Arquitecto + Cerbero — reconfiguración 2.0.0

## Alcance

Actualización solicitada por Rube el 30/09/2026. Sustituye las definiciones de `ia-gov/Arquitecto.md` y `ia-gov/Cerbero.md`, conserva sus nombres y responsabilidades útiles, y agrega plantillas y casos de regresión. No modifica Comercializador, Gabineto, Graffitero ni la propuesta. No incorpora nuevos agentes ni frameworks.

La fuente de esta revisión son las dos definiciones vigentes y las decisiones de esta conversación: interpretación separada de arquitectura, trazabilidad hasta productores reales, anti-proxy, preservación de modalidad/profundidad y auditoría contra el pedido. Es un diseño de control propuesto, no una garantía de resultados futuros.

## Cambios principales

Arquitecto: dos fases (Mission Contract, luego Execution Contract/grafo); baseline multimodal; profundidad distinta de cobertura; requisitos con productor, integración y prueba; capacidad verificada en lugar de routing por nombres; contraejemplo del grafo; misión/progreso persistentes y replanificación ante desvíos.

Cerbero: gate previo de correspondencia; acceso directo al pedido y fuentes; inspección real del producto; QA semántico/profundidad, comunicacional y técnico separados; evidencia por requisito; NOT VERIFIED no permite PASS esencial; versión final y gates afectados; diagnóstico sin atribuciones no demostradas.

Se mantienen: jurisdicciones y owners, minimum necessary context, reutilización/free-first con calidad, seguridad/permisos, alternativas, aprobaciones humanas, dependencia de gates, independencia, recuperación y límite recomendado de dos reintentos, seis estados de gate, severidades y trazabilidad.

Se corrige una regla insuficiente de v1: el Execution Contract deja de ser autoridad suficiente para aprobar por sí solo. También se evita otra mala regla: menos páginas no demuestra pérdida de profundidad. El control exige comparación sustantiva, no un tamaño mínimo arbitrario.

## Archivos

- [Arquitecto](Arquitecto.md) y [Cerbero](Cerbero.md): definiciones operativas.
- [Mission Contract](references/mission-contract-template.md), [Execution Contract](references/execution-contract-template.md) y [QA Gate](references/qa-gate-template.md): plantillas bajo el directorio al que las definiciones hacen referencia.
- [Regresión](tests/control-plane-regression.md): 16 casos, incluyendo controles contra falsos positivos.
- [Activación en Codex](ACTIVAR-CODEX-V2.md): actualización de las copias instaladas sin reemplazar modelos, permisos ni configuración no pertinente.

## Validación y límites

La inspección de la estructura del paquete comprueba presencia de archivos, enlaces relativos, metadatos, estados y cobertura textual de reglas. No demuestra que el modelo siga las instrucciones. Los casos de regresión requieren ejecución en Codex y revisión de outputs reales. Mantenerlos NOT RUN hasta contar con esa evidencia.

Actualizar GitHub no actualiza por sí solo `.codex/agents/*.toml`, `~/.codex/agents/*` ni una sesión ya abierta. Registrar por separado estado de repositorio, instalación, carga del runtime y prueba conductual. No afirmar “activado” si sólo se editaron los Markdown.

## Reversión

Las versiones anteriores permanecen en Git. Ante problemas, revertir sólo el commit de esta reconfiguración, preservando cambios posteriores ajenos. Para copias locales, respaldar antes de actualizar y restaurar únicamente las dos definiciones afectadas. No usar un reset destructivo del repositorio.
