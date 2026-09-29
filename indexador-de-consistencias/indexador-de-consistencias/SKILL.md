---
name: indexador-de-consistencias
description: "Indexar y conciliar afirmaciones, indicadores, decisiones y versiones entre fuentes de un proyecto. Usar cuando Rube pida verificar coherencia, comparar minutas, tableros, presentaciones, propuestas o capítulos, resolver cifras discrepantes, auditar una entrega basada en varias fuentes o identificar qué cambió y qué sigue pendiente. No activar para una corrección de estilo ni para una fuente única sin conflicto material."
---

# Indexador_de_consistencias

## Función

Crear un índice breve de **afirmaciones verificables**, comparar solo las que comparten definición y rastrear cómo una fuente se transformó en una entrega. Detectar también pérdidas de sentido: un texto puede conservar cifras y omitir la acción, el método o el entregable central.

## Procedimiento

1. **Delimitar la comparación.** Identificar decisión o pieza que se debe validar, fuentes y versiones, corte temporal y afirmaciones de mayor impacto. Si el contexto está disperso, usar `recopilador` para ubicar los originales; no abrir todo el proyecto por defecto.
2. **Extraer afirmaciones atómicas.** Por cada dato o definición material, registrar texto o valor exacto, fuente y pasaje, fecha, estado (`observado`, `calculado`, `estimado`, `propuesto`, `acordado`, `aprobado`) y quién lo valida si consta. No convertir una propuesta discutida en decisión.
3. **Construir la clave de comparación.** Identificar concepto/indicador, universo o denominador, ámbito, período, unidad, granularidad, fuente y método. Comparar valores solo después de comprobar esa clave. Usar [índice y matriz](references/indice.md) si la tarea requiere una tabla de conciliación.
4. **Clasificar cada diferencia.** Marcar `coincide`, `actualización legítima`, `no comparable`, `contradicción`, `derivación errónea`, `pérdida semántica` o `evidencia insuficiente`. Explicar el mecanismo de la diferencia: unidad, corte, universo, duplicación, estado de decisión, cálculo, redacción u otra causa concreta.
5. **Resolver con criterio explícito.** Priorizar fuente primaria, propiedad del dato, definición, aprobación, alcance y vigencia. La fecha más reciente por sí sola no decide. Recalcular operaciones verificables desde valores originales; no corregir una serie por intuición. Si hay dos fuentes válidas para objetos distintos, conservar ambas y nombrar la distinción.
6. **Revisar la traducción al producto final.** Comprobar que el resumen, minuta, slide, propuesta o tesis no amplía conclusiones ni borra componentes centrales. En propuestas comerciales, aplicar además la regla de `comercializador` sobre problema, intervención, entregable y cambio; esta skill comprueba fidelidad entre fuente y salida, no reemplaza la redacción comercial.
7. **Entregar la versión utilizable.** Presentar primero la conclusión de consistencia y la corrección necesaria; luego una matriz compacta para conflictos materiales. Dejar explícito qué está resuelto, qué necesita validación y qué conclusiones dependen de ello. Si se pidió editar el producto, aplicar las correcciones y verificarlo, no detenerse en el diagnóstico.

## Reglas de evidencia

- Conservar el pasaje y la versión de origen; citar o enlazar el documento cuando la herramienta lo permita. No usar un resumen previo como prueba de una cifra cuando el dato original esté disponible.
- Separar `filas`, `entidades únicas`, `horas`, `turnos`, `oferta formal`, `oferta neta`, `otorgados` y `producción`; equivalencias aparentes no son equivalencias metodológicas.
- Marcar la ausencia de definición, denominador o corte como límite de comparabilidad. No declarar contradicción entre magnitudes que miden fenómenos distintos.
- No hacer que la coincidencia textual sustituya a la validación factual; tampoco tratar una reformulación de estilo como un cambio de política.

## Subagentes y costo

Delegar la extracción por fuentes independientes solo cuando el volumen lo justifique. Enviar a cada agente el corpus acotado, la clave de comparación y un formato de hallazgos con pasajes. Reservar al agente principal la conciliación y una revisión crítica de los conflictos de mayor impacto. Una tarea pequeña se resuelve sin delegación; paralelizar puede reducir tiempo, pero aumentar tokens totales.

## Control final

Comprobar que cada corrección tiene fuente; los cálculos se pueden reproducir; ninguna propuesta figura como acuerdo; la salida conserva el significado operativo; y las discrepancias abiertas no se esconden tras una cifra única. No fabricar un puntaje global de consistencia cuando las evidencias tienen distinta relevancia.
