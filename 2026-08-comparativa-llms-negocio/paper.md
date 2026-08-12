---
titulo: "Comparativa de modelos de IA conversacional gratuitos en tareas reales de negocio: ChatGPT vs Gemini vs Claude"
tipo: "Estudio comparativo (Benchmark)"
autor: "Dani Miera — Dembix AI Lab"
fecha: "Agosto 2026"
---

# Comparativa de modelos de IA conversacional gratuitos en tareas reales de negocio

**Estudio comparativo (Benchmark) · Dembix AI Lab · Agosto 2026**

---

## Resumen

Este estudio evalúa el rendimiento de las versiones web gratuitas de ChatGPT, Gemini y Claude en 5 tareas representativas de la operativa diaria de un negocio local (atención al cliente, redacción de reseñas, marketing en redes, resolución de consultas con datos fijos, y síntesis de texto). Cada tarea se ejecutó 3 veces por modelo (45 respuestas en total) y se evaluó mediante un protocolo de evaluación ciega asistida por IA (DeepSeek como evaluador externo), con una rúbrica de 4 criterios definida antes de la ejecución. Los tres modelos obtienen puntuaciones muy próximas entre sí (diferencia inferior a 0.1 sobre 5 en la media global), pero muestran patrones de comportamiento claramente diferenciados por tarea, incluyendo un caso de omisión sistemática de información (ChatGPT) y un caso de sobrecarga de información no solicitada con tendencia creciente entre repeticiones (Claude). Se declara como limitación principal la ausencia de evaluadores humanos en esta primera edición del estudio.

---

## 1. Introducción

La mayoría de comparativas públicas de modelos de IA conversacional se centran en benchmarks académicos (matemáticas, código, razonamiento lógico) evaluados en inglés. Existe un vacío notable de comparativas centradas en **tareas reales de negocio, en español, ejecutadas tal como las usaría un dueño de negocio local sin conocimientos técnicos** —es decir, a través de las interfaces web gratuitas, sin API ni configuración avanzada.

Este estudio busca cubrir ese vacío, con un objetivo doble: (1) aportar una comparativa objetiva y reproducible que ayude a negocios locales a decidir qué herramienta gratuita usar según su necesidad, y (2) establecer un protocolo de evaluación propio, reutilizable en futuros estudios de Dembix AI Lab.

## 2. Metodología

### 2.1 Modelos evaluados

Versiones web gratuitas, sin API, tal como las usaría cualquier persona sin conocimientos técnicos:
- ChatGPT (chatgpt.com)
- Gemini (gemini.google.com)
- Claude (claude.ai)

### 2.2 Tareas

Se definieron 5 tareas fijas, representativas de necesidades reales de un negocio local, cada una diseñada para poner a prueba una capacidad distinta:

| # | Tarea | Capacidad evaluada |
|---|-------|---------------------|
| 1 | Responder a una reseña negativa de 2 estrellas | Tono, empatía, resolución de conflicto |
| 2 | Redactar un post de Instagram con límite de caracteres | Creatividad + cumplimiento de restricciones de formato |
| 3 | Responder a una consulta de cliente con datos fijos que generan un conflicto de horario | Precisión factual, honestidad ante una petición imposible de satisfacer |
| 4 | Traducir un mensaje de cliente y responder | Calidad de traducción + coherencia de respuesta |
| 5 | Resumir una reseña larga y confusa en 3 líneas | Comprensión lectora y síntesis |

Cada tarea se ejecutó **3 veces por modelo**, en conversaciones nuevas e independientes cada vez (para evitar que el modelo "aprendiera" de un intento anterior dentro de la misma sesión), dando un total de **45 respuestas evaluadas**.

Los prompts exactos utilizados en las 5 tareas, junto con los datos de referencia empleados en la Tarea 3, se incluyen en el Anexo A.

### 2.3 Protocolo de evaluación

Se definió una rúbrica de 4 criterios **antes** de generar ninguna respuesta, para evitar ajustar los criterios a posteriori según conviniera:

- **Precisión factual** (SÍ / NO / N-A): solo se evalúa cuando la tarea incluye datos de referencia explícitos y verificables. Se marca N/A cuando no existe ningún dato de referencia contra el que verificar la respuesta — información adicional correcta pero no solicitada nunca se considera un fallo de precisión factual, y se valora en su lugar dentro de "Utilidad directa" si sobrecarga la respuesta.
- **Tono y naturalidad** (1-5): con anclas de puntuación predefinidas, desde "sonaría a una persona real, se enviaría tal cual" (5) hasta "claramente artificial o inadecuado" (1).
- **Cumplimiento de formato** (1-5): grado en que la respuesta respeta las restricciones pedidas (longitud, estructura).
- **Utilidad directa** (1-5): si la respuesta sería usable tal cual o requeriría edición.

Adicionalmente, se evaluó la **consistencia entre las 3 repeticiones** de cada modelo por tarea (Alta / Media / Baja), para capturar no solo la calidad media sino la fiabilidad del modelo.

### 2.4 Evaluación ciega asistida por IA

Las 45 respuestas se anonimizaron (etiquetadas como Respuesta A, B, C, en orden no revelado al evaluador) y se evaluaron mediante DeepSeek, un modelo no incluido entre los 3 comparados, para evitar el sesgo de autopreferencia que se produciría si uno de los modelos comparados evaluara también sus propias respuestas. El evaluador recibió instrucciones explícitas para mitigar sesgos conocidos en evaluación asistida por IA (verbosidad, posición, estilo/confianza, familiaridad) y se le exigió razonar por escrito antes de asignar cada puntuación.

Durante la ejecución se detectó y corrigió una inconsistencia en la aplicación del criterio de Precisión factual en la Tarea 4 (ver sección 5, Limitaciones), lo cual llevó a fijar la regla descrita en 2.3 y a repetir esa evaluación con el criterio ya corregido.

## 3. Resultados

### 3.1 Tabla global

| Tarea | ChatGPT | Gemini | Claude |
|---|---|---|---|
| 1 — Reseña negativa | 5.00 | 4.33 | 5.00 |
| 2 — Promoción café | 5.00 | 4.67 | 5.00 |
| 3 — Cita peluquería (tarea trampa) | 4.67 | 5.00 | 5.00 |
| 4 — Envíos Canarias | 4.75 | 5.00 | 4.17 |
| 5 — Resumen de reseña | 5.00 | 5.00 | 5.00 |
| **Media global** | **4.88** | **4.80** | **4.83** |

Los tres modelos obtienen resultados muy próximos entre sí (rango de 0.08 puntos sobre 5 en la media global), lo que sugiere que, para tareas cotidianas de negocio en español, **la elección del modelo importa menos que el hecho de usar alguno**. Las diferencias reales aparecen al analizar tarea por tarea, no en el promedio general.

### 3.2 Consistencia entre repeticiones

Todos los modelos mostraron consistencia **Alta** en 4 de las 5 tareas. La única excepción fue **Claude en la Tarea 4**, con consistencia **Media**: sus 3 repeticiones muestran una tendencia decreciente en utilidad directa (5 → 5 → 5 en tono, pero 3 → 3 → 2 en utilidad), coincidiendo con respuestas cada vez más extensas y técnicas sobre normativa aduanera no solicitada.

### 3.3 Casos destacados

**Caso 1 — Omisión sistemática (ChatGPT, Tarea 3).** En las 3 repeticiones, ChatGPT respondió correctamente sobre la disponibilidad (sábado 10:00) pero omitió consistentemente mencionar el motivo del cierre de disponibilidad entre semana (el horario de cierre a las 20:00), a diferencia de Gemini y Claude, que sí lo explicaron. No se trató de un fallo puntual, sino de un patrón repetido en las 3 ejecuciones independientes.

**Caso 2 — Sobrecarga de información no solicitada con tendencia creciente (Claude, Tarea 4).** Ante una pregunta simple sobre envíos a Canarias y seguimiento de pedido, Claude añadió en las 3 repeticiones información no solicitada sobre régimen fiscal y posibles gastos aduaneros. Si bien esta información es correcta y potencialmente útil, el evaluador la calificó como una sobrecarga que resta naturalidad y usabilidad directa a la respuesta, con una tendencia a empeorar (no a estabilizarse) entre repeticiones.

**Caso 3 — Equilibrio consistente (Gemini).** Gemini no obtuvo la puntuación más alta en ninguna tarea de forma aislada, pero tampoco registró ningún punto débil marcado — fue el modelo con el perfil de resultados más uniforme entre las 5 tareas.

## 4. Conclusiones prácticas

Para un negocio local que use estas herramientas en su versión gratuita, sin configuración técnica:

- **Para respuestas breves y con restricciones de formato** (posts, promociones): los tres modelos rinden de forma prácticamente idéntica.
- **Para consultas donde hay que comunicar límites o negativas** (disponibilidad, horarios): Gemini y Claude tienden a dar explicaciones más completas que ChatGPT, que tiende a omitir el "por qué" de una limitación.
- **Para consultas simples que no requieren información extra**: ChatGPT y Gemini tienden a mantenerse más ceñidos a lo preguntado; Claude muestra una tendencia a añadir contexto adicional que puede no ser bienvenido en un primer contacto con el cliente.

Ninguno de los tres modelos mostró alucinaciones graves (invención de datos contradictorios con los proporcionados) en ninguna de las 45 respuestas evaluadas.

## 5. Limitaciones

- **Evaluación basada en un único evaluador-IA, sin evaluadores humanos.** Esta primera edición del estudio no contó con evaluadores humanos por disponibilidad de recursos. La evaluación asistida por IA, aunque diseñada para mitigar sesgos conocidos (autopreferencia, verbosidad, posición, estilo), no sustituye por completo al juicio humano. Se recomienda incorporar evaluación humana en futuras ediciones de este estudio.
- **Muestra reducida.** 3 repeticiones por tarea y modelo permiten detectar patrones consistentes, pero no equivalen a un análisis estadístico robusto sobre una muestra amplia.
- **Inconsistencia detectada y corregida durante el proceso.** En una primera pasada, el criterio de Precisión factual se aplicó de forma contradictoria a la Tarea 4 (penalizando primero la inclusión de información no solicitada, y penalizando después su omisión). Se detectó esta inconsistencia, se definió una regla explícita para resolverla (sección 2.3) y se repitió la evaluación de esa tarea con el criterio ya corregido. Se documenta aquí por transparencia metodológica.
- **Los modelos evaluados cambian con el tiempo.** Los resultados corresponden a las versiones gratuitas disponibles en agosto de 2026 y no son necesariamente representativos de versiones futuras.
- **Un solo idioma y un solo país de referencia.** El estudio se centra en tareas en español con contexto de negocio local en España; los resultados no son necesariamente extrapolables a otros idiomas o contextos culturales.

## 6. Trabajo futuro

- Incorporar evaluadores humanos ciegos como contraste de la evaluación asistida por IA, y reportar el grado de acuerdo entre ambos.
- Ampliar el número de repeticiones por tarea.
- Extender el estudio a más tareas y, potencialmente, a modelos open-source ejecutables en local.

---

## Anexo A — Prompts exactos utilizados

**Tarea 1:**
> Redacta una respuesta a esta reseña negativa de 2 estrellas, en tono profesional y empático, reconociendo el problema y ofreciendo solucionarlo. Máximo 5 líneas.
> Reseña: "La comida bien pero tardaron muchísimo en traer la cuenta, casi 20 minutos esperando para pagar. Al final casi perdemos el siguiente plan que teníamos. Una pena porque el sitio tiene buena pinta."

**Tarea 2:**
> Escríbeme un post para Instagram anunciando una promoción: 2x1 en cafés todos los martes de octubre, solo de 9:00 a 12:00, en una cafetería de barrio. Tono cercano y entusiasta. Máximo 280 caracteres, incluyendo espacios.

**Tarea 3:**
> Eres el asistente de atención al cliente de la peluquería "Espacio Bella". Estos son los datos reales del negocio, que debes respetar sin inventar nada: Horario: martes a sábado, de 9:30 a 14:00 y de 16:00 a 20:00. Domingos y lunes cerrado. El próximo hueco disponible para un servicio de corte + tinte (dura 2 horas) es el sábado a las 10:00. Responde a este mensaje de un cliente por WhatsApp: "Hola! ¿Tenéis hueco esta semana para cortarme el pelo y hacerme un tinte? Solo puedo entre semana por la tarde noche, después de las 19h"

**Tarea 4:**
> Traduce este mensaje de un cliente al español y redacta una respuesta adecuada en español, en tono amable: "Hi! Do you ship to the Canary Islands? Also, is there any way to track the order once it's shipped? Thanks a lot!"

**Tarea 5:**
> Resume en máximo 3 líneas cuál es el problema real que plantea esta reseña: "Bueno pues nada, fui el sábado pasado con mi pareja porque teníamos ganas de probar el sitio desde hace tiempo [...] pero bueno, esperaba otra cosa la verdad"

*(Texto completo de la reseña de la Tarea 5 disponible en el repositorio de datos del estudio.)*

## Anexo B — Datos y respuestas completas

Las 45 respuestas completas, junto con las tablas de evaluación detalladas por repetición, están disponibles como material complementario reproducible en el repositorio de Dembix AI Lab.

---

*Estudio publicado por Dembix AI Lab, Cantabria. Agosto 2026.*
