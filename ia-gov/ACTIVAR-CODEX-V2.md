# Activar Arquitecto y Cerbero v2 en Codex

Este archivo es una instrucción para ejecutar en el proyecto local de Codex. No acredita que la instalación haya ocurrido. No pegar ambas skills enteras en cada pedido; actualizar primero sus definiciones efectivas.

## Prompt de actualización

> Actualizá exclusivamente Arquitecto y Cerbero a la versión 2.0.0 de IA-Gov, sin reformar todavía la propuesta comercial. Primero leé las instrucciones AGENTS.md aplicables y localizá la copia de `rubeabbo/agency-agents-ia-gov` o `rubeabbo/IA-GOV` usada por este proyecto. Verificá que `ia-gov/Arquitecto.md` y `ia-gov/Cerbero.md` declaren version 2.0.0 y leé sus referencias. Si la copia está desactualizada, obtené las versiones vigentes sin sobrescribir cambios locales; ante conflicto, detené la actualización y mostrámelo.
>
> Identificá las definiciones que realmente carga este runtime: `.codex/agents/Arquitecto.toml`, `.codex/agents/Cerbero.toml`, las globales bajo `~/.codex/agents/` u otras rutas declaradas. No deduzcas instalación por ver Markdown. Respaldá las definiciones efectivas y actualizá únicamente sus instrucciones, conservando nombres/IDs del runtime, modelo, esfuerzo de razonamiento, permisos, herramientas y el resto de configuración. Usá el mecanismo de instalación/conversión ya existente si corresponde; no inventes un formato de agente.
>
> Asegurá que las plantillas de `ia-gov/references/` y la regresión sean accesibles desde las definiciones instaladas, resolviendo sus referencias según el directorio de la fuente. Verificá sintaxis y volvé a leer los archivos resultantes. Comprobá que no quedó una copia antigua con precedencia. Si hace falta una sesión nueva para cargar cambios, indicámelo sin afirmar que la sesión actual ya los adoptó.
>
> Cuando se pueda confirmar carga efectiva, ejecutá una prueba en seco con los casos R01, R03, R04, R06, R09 y R11 de `ia-gov/tests/control-plane-regression.md`: nada de producir la propuesta ni escribir en sus fuentes. Usá delegaciones reales a los roles disponibles y revisión de evidencia; no simules agentes ni independencia. Si no podés ejecutar un caso, registralo NOT RUN, no PASS. Entregá rutas cambiadas, versión cargada, respaldos, herramientas reales, outputs de prueba y pendientes. No toques otros agentes ni cambies el alcance para conseguir una aprobación.

## Estado que debe reportar Codex

Separar: fuentes obtenidas → definiciones locales actualizadas → runtime cargado → casos ejecutados. Una fase no prueba la siguiente. No modificar configuración global cuando sólo se autorizó/precisó una copia de proyecto; resolver primero el alcance efectivo de la instalación.
