# Metodología de evaluación

La evaluación de las 45 respuestas (5 tareas × 3 modelos × 3 repeticiones) se realizó mediante evaluación ciega asistida por IA, usando DeepSeek como evaluador externo — un modelo no incluido entre los 3 comparados (ChatGPT, Gemini, Claude), para evitar sesgo de autopreferencia.

## Rúbrica de evaluación

| Criterio | Escala | Regla |
|---|---|---|
| Precisión factual | SÍ / NO / N-A | Se marca **N/A** siempre que la tarea no incluya datos de referencia explícitos y verificables. Información adicional correcta pero no solicitada **nunca** cuenta como fallo de precisión factual — se valora, si procede, en "Utilidad directa". |
| Tono y naturalidad | 1-5 | 5 = suena a persona real, se enviaría tal cual. 1 = claramente artificial o inadecuado. |
| Cumplimiento de formato | 1-5 | 5 = cumple exactamente las restricciones pedidas (longitud, estructura). |
| Utilidad directa | 1-5 | 5 = usable tal cual, sin ninguna edición. |
| Consistencia entre repeticiones | Alta / Media / Baja | Compara las 3 repeticiones de un mismo modelo dentro de una tarea. |

## Reglas de imparcialidad aplicadas al evaluador

1. No debe intentar identificar qué modelo generó cada respuesta.
2. Sesgo de longitud/verbosidad: una respuesta más larga no es automáticamente mejor.
3. Sesgo de posición: el orden A/B/C es aleatorio y no indica calidad.
4. Sesgo de estilo/confianza: no puntuar más alto por sonar más formal o estructurado si el contenido no lo justifica.
5. Sesgo de familiaridad: no valorar mejor un estilo "parecido a como el propio evaluador escribiría".
6. Debe razonar por escrito antes de asignar cada puntuación numérica (evita puntuaciones intuitivas sin justificar).

## Corrección metodológica documentada

Durante la primera pasada de evaluación, el criterio de Precisión factual se aplicó de forma contradictoria en la Tarea 4 (penalizando primero la inclusión de información no solicitada sobre normativa aduanera, y penalizando después su omisión en la misma tarea). Se detectó esta inconsistencia, se definió la regla explícita indicada arriba, y se repitió la evaluación de esa tarea completa con el criterio ya corregido. Los resultados publicados en `paper.md` corresponden a la versión corregida.

## Prompt exacto utilizado con el evaluador (DeepSeek)

El prompt completo, con las reglas de imparcialidad y el formato de salida exigido, se adjunta como referencia reproducible. Cualquier persona puede tomar este mismo prompt, las respuestas en `datos-crudos/`, y repetir la evaluación de forma independiente.

```
Actúas como evaluador externo e independiente en un estudio comparativo (benchmark)
que analiza la calidad de respuestas generadas por distintos modelos de IA
conversacional en tareas reales de negocio. Tu único papel es puntuar 3 respuestas
anónimas (Respuesta A, B y C) con el máximo rigor y objetividad posible.

[Ver reglas de imparcialidad completas arriba]

Para cada respuesta, razona brevemente (2-3 frases) por criterio ANTES de asignar
el número. Cierra con la tabla resumen de la rúbrica y, en tareas con 3 repeticiones,
la tabla agregada de consistencia.
```

*(Versión íntegra del prompt, incluyendo el formato de salida exacto, disponible bajo petición o en el historial de desarrollo del estudio.)*
