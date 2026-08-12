# Prompts de las 5 tareas — Benchmark Dembix #1

Instrucciones de ejecución:
- Copia y pega el prompt EXACTO (tal cual, sin cambiar ni una palabra) en cada modelo.
- Abre una **conversación nueva** cada vez (no reutilices el chat entre repeticiones ni entre modelos).
- Repite cada tarea 3 veces por modelo (nueva conversación cada repetición).
- Guarda la respuesta completa, tal cual la da el modelo, sin editar.

---

## Tarea 1 — Respuesta a reseña negativa

**Prompt a pegar:**
```
Redacta una respuesta a esta reseña negativa de 2 estrellas, en tono profesional y empático, reconociendo el problema y ofreciendo solucionarlo. Máximo 5 líneas.

Reseña: "La comida bien pero tardaron muchísimo en traer la cuenta, casi 20 minutos esperando para pagar. Al final casi perdemos el siguiente plan que teníamos. Una pena porque el sitio tiene buena pinta."
```

---

## Tarea 2 — Post de Instagram con límite de caracteres

**Prompt a pegar:**
```
Escríbeme un post para Instagram anunciando una promoción: 2x1 en cafés todos los martes de octubre, solo de 9:00 a 12:00, en una cafetería de barrio. Tono cercano y entusiasta. Máximo 280 caracteres, incluyendo espacios.
```

---

## Tarea 3 — Consulta de cliente con datos fijos que debe respetar

**Datos de referencia (fíjalos siempre igual, no cambian entre repeticiones ni modelos):**
```
Negocio: Peluquería "Espacio Bella"
Horario: Martes a sábado, de 9:30 a 14:00 y de 16:00 a 20:00. Domingos y lunes cerrado.
Servicio solicitado por el cliente: corte + tinte
Duración media de corte + tinte: 2 horas
Próximo hueco disponible real: sábado a las 10:00
```

**Prompt a pegar:**
```
Eres el asistente de atención al cliente de la peluquería "Espacio Bella". Estos son los datos reales del negocio, que debes respetar sin inventar nada:

- Horario: martes a sábado, de 9:30 a 14:00 y de 16:00 a 20:00. Domingos y lunes cerrado.
- El próximo hueco disponible para un servicio de corte + tinte (dura 2 horas) es el sábado a las 10:00.

Responde a este mensaje de un cliente por WhatsApp: "Hola! ¿Tenéis hueco esta semana para cortarme el pelo y hacerme un tinte? Solo puedo entre semana por la tarde noche, después de las 19h"
```

*(Nota: este prompt está pensado deliberadamente para comprobar si el modelo detecta que el cliente pide algo que choca con los datos reales —después de las 19h entre semana casi no deja margen para un servicio de 2h que cierra a las 20h— y si inventa o no un hueco que no existe.)*

---

## Tarea 4 — Traducción + respuesta

**Prompt a pegar:**
```
Traduce este mensaje de un cliente al español y redacta una respuesta adecuada en español, en tono amable:

"Hi! Do you ship to the Canary Islands? Also, is there any way to track the order once it's shipped? Thanks a lot!"
```

---

## Tarea 5 — Resumen de reseña larga y confusa

**Prompt a pegar:**
```
Resume en máximo 3 líneas cuál es el problema real que plantea esta reseña:

"Bueno pues nada, fui el sábado pasado con mi pareja porque teníamos ganas de probar el sitio desde hace tiempo, nos habían hablado muy bien de la carta y demás, la verdad que el ambiente está bien, la decoración chula, pero bueno, el caso es que pedimos y tardaron bastante, no pasa nada oye que a veces hay mucha gente, lo entiendo, pero luego cuando llegó mi plato no era lo que había pedido, pedí el de salsa aparte y me lo trajeron ya mezclado, y cuando lo comenté a la camarera pues como que no me hizo mucho caso la verdad, al final nos lo cambiaron pero ya el rato raro se quedó ahí, y mira que las croquetas estaban buenísimas eh, pero bueno, esperaba otra cosa la verdad"
```

---

## Recordatorio del proceso completo

1. Ejecuta las 5 tareas × 3 modelos × 3 repeticiones (45 respuestas en total)
2. Guarda cada respuesta en tu hoja de seguimiento
3. Aleatoriza el orden (A/B/C) antes de pasarlas a evaluación
4. Usa el prompt de evaluación ciega (documento aparte) con Claude + tus evaluadores humanos
5. Para la Tarea 3, al evaluar, pega los mismos "Datos de referencia" de aquí en el campo correspondiente del prompt de evaluación, para que se pueda verificar la precisión factual
