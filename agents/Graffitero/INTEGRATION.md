# Integración de Graffitero

Ubicación recomendada: `agents/Graffitero/`.

Graffitero recibe tareas visuales desde otros agentes o desde el usuario, genera un plan visual, elige representación y herramienta, compila instrucciones, ejecuta cuando la herramienta está disponible y realiza QA sobre el artifact resultante.

No duplicar una skill genérica llamada `Graffitero`: la identidad corresponde al agente. Las skills deben nombrarse `graffitero-*`.
