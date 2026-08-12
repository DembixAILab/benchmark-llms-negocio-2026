# Evaluación comparativa de respuestas de IA para tareas de negocio

**Evaluador externo independiente**
**Fecha de evaluación:** 2026-08-12

> Nota: informe exploratorio con 1 repetición por tarea. Sirvió como prueba piloto del protocolo antes de ejecutar el estudio completo de 3 repeticiones (ver `informe-2-completo-3-repeticiones.md`).

---

## Metodología

Esta evaluación analiza la calidad de respuestas generadas por distintos modelos de IA conversacional en tareas reales de negocio. Se han evaluado 5 conjuntos de respuestas (Tareas 1-5), cada uno con 3 respuestas anónimas (A, B y C).

### Criterios de evaluación

| Criterio | Escala | Descripción |
|---|---|---|
| **Precisión factual** | SÍ / NO / N-A | Verificación binaria: ¿la respuesta respeta exactamente los datos de referencia? |
| **Tono y naturalidad** | 1-5 | ¿Suena a una persona real? ¿Es adecuado al contexto? |
| **Cumplimiento de formato** | 1-5 | ¿Cumple con los límites y estructura solicitados? |
| **Utilidad directa** | 1-5 | ¿Es usable tal cual o requiere ediciones? |

---

## Tarea 1: Respuesta a reseña negativa

**Contexto:** Cliente se queja de una espera de 20 minutos para pagar en un restaurante, aunque disfrutó de la comida.

### Respuesta A (Tarea 1)
> Sentimos mucho la espera de casi 20 minutos para poder pagar y entendemos perfectamente las molestias que pudo ocasionarle, especialmente teniendo otro plan después. Nos alegra saber que disfrutó de la comida, pero lamentamos que el servicio de la cuenta empañara su experiencia. Tomamos nota de lo ocurrido para evitar que vuelva a suceder. Nos encantaría tener la oportunidad de atenderle de nuevo y ofrecerle la experiencia que merece.

- Precisión factual: N-A
- Tono y naturalidad: 5 — Excelente. Empático, profesional y humano.
- Cumplimiento de formato: 5
- Utilidad directa: 5

### Respuesta B (Tarea 1)
> Lamentamos mucho la demora que experimentó al solicitar su cuenta, ya que nuestra prioridad es ofrecer un servicio ágil. Entendemos perfectamente su frustración por el tiempo perdido y le pedimos disculpas por este inconveniente. Nos gustaría invitarle a contactarnos directamente para compensar esta experiencia en su próxima visita.

- Precisión factual: N-A
- Tono y naturalidad: 4 — Correcto pero algo frío y corporativo.
- Cumplimiento de formato: 5
- Utilidad directa: 4 — La invitación a contactar "directamente" añade un paso extra innecesario.

### Respuesta C (Tarea 1)
> Aquí tienes una posible respuesta: Muchas gracias por tu reseña y por destacar que la comida estuvo a la altura. Lamentamos sinceramente la demora en traer la cuenta y el mal rato que os hizo pasar, entendemos lo molesto que es cuando tenéis otros planes esperando. Vamos a revisar el servicio de sala para que esto no vuelva a repetirse. Nos encantaría invitaros a volver y demostraros que podemos hacerlo mejor; escríbenos cuando quieras.

- Precisión factual: N-A
- Tono y naturalidad: 4 — Muy natural y cercano, pero la coletilla "Aquí tienes una posible respuesta" es un artefacto de IA que debe eliminarse.
- Cumplimiento de formato: 5
- Utilidad directa: 4 — Casi usable, requiere eliminar la frase introductoria.

### Tabla resumen Tarea 1
| Criterio | A | B | C |
|---|---|---|---|
| Precisión factual | N-A | N-A | N-A |
| Tono y naturalidad | 5 | 4 | 4 |
| Cumplimiento de formato | 5 | 5 | 5 |
| Utilidad directa | 5 | 4 | 4 |
| **Media** | **5.0** | **4.3** | **4.3** |

---

## Tarea 2: Promoción de café 2x1

**Contexto:** 2x1 en cafés todos los martes de octubre, 9:00 a 12:00, cafetería de barrio.
**Datos de referencia:** Martes de octubre, 2x1 en cafés, horario 9:00-12:00.

### Respuesta A (Tarea 2)
> ¡Los martes saben mejor! Durante todos los martes de octubre, disfruta de nuestro 2x1 en cafés, de 9:00 a 12:00. Ven con tu persona favorita y compartid un buen café de barrio.

- Precisión factual: SÍ — Respeta todos los datos.
- Tono y naturalidad: 5
- Cumplimiento de formato: 5
- Utilidad directa: 5

### Respuesta B (Tarea 2)
> ¡Buenos días, vecinos! Octubre se pone calentito y delicioso. Ven con tu persona favorita todos los martes del mes, de 9:00 a 12:00, ¡y llévate un 2x1 en cafés! Tu rincón de barrio te espera para empezar el día con la mejor energía. ¡No faltéis!

- Precisión factual: SÍ
- Tono y naturalidad: 5 — Muy cálido, refuerza sentido de comunidad.
- Cumplimiento de formato: 5
- Utilidad directa: 5

### Respuesta C (Tarea 2)
> ¡Los martes de octubre son de 2x1! Todos los martes, de 9:00 a 12:00, ven a por tu café acompañado. Tu cafetería de barrio de siempre, con el sabor y el cariño de siempre. ¡Te esperamos! #Café2x1 #CafeteríaDeBarrio

- Precisión factual: SÍ
- Tono y naturalidad: 5 — Los hashtags son un acierto para redes.
- Cumplimiento de formato: 5
- Utilidad directa: 5

### Tabla resumen Tarea 2
| Criterio | A | B | C |
|---|---|---|---|
| Precisión factual | SÍ | SÍ | SÍ |
| Tono y naturalidad | 5 | 5 | 5 |
| Cumplimiento de formato | 5 | 5 | 5 |
| Utilidad directa | 5 | 5 | 5 |
| **Media** | **5.0** | **5.0** | **5.0** |

---

## Tarea 3: Respuesta a cita en peluquería

**Contexto:** Cliente pregunta por disponibilidad para corte + tinte entre semana después de las 19:00. No hay hueco (cierran 20:00, servicio dura 2h). Próximo hueco: sábado 10:00.
**Datos de referencia:** Sin hueco entre semana después de 19:00, servicio dura 2 horas, próximo hueco sábado 10:00.

### Respuesta A (Tarea 3)
> ¡Hola! Esta semana no tenemos hueco entre semana después de las 19:00 para corte + tinte. El próximo hueco disponible es el sábado a las 10:00, y el servicio dura aproximadamente 2 horas. Si te viene bien, podemos reservarte esa cita.

- Precisión factual: SÍ
- Tono y naturalidad: 4 — Directo y funcional, pero algo seco.
- Cumplimiento de formato: 5
- Utilidad directa: 4 — No ofrece opciones adicionales.

### Respuesta B (Tarea 3)
> Hola, muchas gracias por contactar con Espacio Bella. Te informo de que para el servicio de corte y tinte, que tiene una duración de 2 horas, nuestro próximo hueco disponible es este sábado a las 10:00. Lamentablemente, no disponemos de citas libres entre semana por la tarde después de las 19:00, ya que nuestro horario de cierre es a las 20:00. ¿Te vendría bien el sábado por la mañana o prefieres que busquemos otra opción para la semana que viene? Quedo a la espera de lo que me digas.

- Precisión factual: SÍ — Añade contexto útil (explica el motivo del cierre).
- Tono y naturalidad: 5 — Profesional pero cercano, agradece, explica y ofrece opciones.
- Cumplimiento de formato: 5
- Utilidad directa: 5 — Respuesta modelo para este tipo de consultas.

### Respuesta C (Tarea 3)
> [Nota: texto no capturado íntegramente en el traspaso original — recuperar de la hoja de seguimiento si se necesita el texto exacto. Evaluación registrada: Precisión factual SÍ, Tono 5 ("muy natural y amable, ofrece proactividad al avisar si se libera una cita"), Formato 5, Utilidad 5.]

### Tabla resumen Tarea 3
| Criterio | A | B | C |
|---|---|---|---|
| Precisión factual | SÍ | SÍ | SÍ |
| Tono y naturalidad | 4 | 5 | 5 |
| Cumplimiento de formato | 5 | 5 | 5 |
| Utilidad directa | 4 | 5 | 5 |
| **Media** | **4.3** | **5.0** | **5.0** |

---

## Tarea 4: Consulta sobre envíos a Canarias y seguimiento

**Contexto:** Cliente pregunta si hacen envíos a Canarias y si hay seguimiento del pedido.

### Respuesta A (Tarea 4)
> ¡Hola! ¡Muchas gracias por escribirnos! Sí, realizamos envíos a las Islas Canarias. Una vez que el pedido haya sido enviado, recibirás un número de seguimiento para que puedas consultar el estado del envío en todo momento. Si necesitas cualquier otra información, estaremos encantados de ayudarte. ¡Muchas gracias!

- Precisión factual: SÍ — Responde exactamente a las dos preguntas.
- Tono y naturalidad: 5
- Cumplimiento de formato: 5
- Utilidad directa: 5

### Respuesta B (Tarea 4)
> ¡Hola! Muchas gracias por contactarnos. Sí, realizamos envíos a las Islas Canarias. En cuanto a tu pregunta sobre el seguimiento, una vez que el pedido haya sido enviado, te llegará un correo electrónico con un número de seguimiento para que puedas localizar tu paquete en todo momento. Si tienes alguna otra duda, estaré encantado/a de ayudarte. ¡Saludos!

- Precisión factual: SÍ
- Tono y naturalidad: 5
- Cumplimiento de formato: 5
- Utilidad directa: 5

### Respuesta C (Tarea 4)
> ¡Hola! Muchas gracias por escribirnos. Sí, realizamos envíos a las Islas Canarias sin problema. Ten en cuenta que, al tratarse de un territorio con un régimen fiscal especial, es posible que el pedido esté sujeto a trámites aduaneros o gastos adicionales según el tipo de producto, así que si tienes dudas sobre un artículo en concreto, contáctanos y te confirmamos los detalles antes de que hagas la compra. En cuanto al seguimiento, una vez que tu pedido salga de nuestro almacén recibirás un correo electrónico con el número de seguimiento y un enlace para consultar el estado del envío en tiempo real. Si tienes cualquier otra pregunta, no dudes en escribirnos. ¡Estamos encantados de ayudarte! Un saludo cordial.

- Precisión factual (criterio original, ver corrección en informe 3): NO — Añade información no solicitada sobre trámites aduaneros. Frase señalada: "Ten en cuenta que, al tratarse de un territorio con un régimen fiscal especial, es posible que el pedido esté sujeto a trámites aduaneros o gastos adicionales según el tipo de producto".
- Tono y naturalidad: 5
- Cumplimiento de formato: 5
- Utilidad directa: 3 — Requiere edición para ceñirse a lo preguntado (criterio revisado posteriormente, ver informe 3).

### Tabla resumen Tarea 4
| Criterio | A | B | C |
|---|---|---|---|
| Precisión factual | SÍ | SÍ | NO |
| Tono y naturalidad | 5 | 5 | 5 |
| Cumplimiento de formato | 5 | 5 | 5 |
| Utilidad directa | 5 | 5 | 3 |
| **Media** | **5.0** | **5.0** | **4.3** |

---

## Tarea 5: Resumen de reseña larga y confusa

### Respuesta A (Tarea 5)
> El problema real es una mala gestión del servicio: hubo una espera considerable y, sobre todo, entregaron un plato incorrecto. La situación empeoró porque la camarera no atendió adecuadamente la reclamación, dejando al cliente con una sensación de indiferencia.

- Precisión factual: SÍ — Resume correctamente los elementos clave.
- Tono y naturalidad: 5
- Cumplimiento de formato: 5
- Utilidad directa: 5

### Respuesta B (Tarea 5)
> El problema real es la pésima gestión del servicio y la indiferencia del personal: un pedido erróneo (salsa mezclada en lugar de aparte), una espera excesiva y una camarera que ignoró la queja inicial, arruinando la experiencia a pesar de la buena comida y el ambiente.

- Precisión factual: SÍ
- Tono y naturalidad: 5
- Cumplimiento de formato: 5
- Utilidad directa: 5

### Respuesta C (Tarea 5)
> El problema principal fue un error en el pedido (le sirvieron el plato con la salsa mezclada cuando la había pedido aparte), agravado por la falta de atención del personal al reportarlo. Aunque lo corrigieron, la mala gestión de la queja dejó una sensación incómoda que empañó la experiencia, pese al buen ambiente y la comida.

- Precisión factual: SÍ — Con matices adicionales.
- Tono y naturalidad: 5
- Cumplimiento de formato: 5
- Utilidad directa: 5

### Tabla resumen Tarea 5
| Criterio | A | B | C |
|---|---|---|---|
| Precisión factual | SÍ | SÍ | SÍ |
| Tono y naturalidad | 5 | 5 | 5 |
| Cumplimiento de formato | 5 | 5 | 5 |
| Utilidad directa | 5 | 5 | 5 |
| **Media** | **5.0** | **5.0** | **5.0** |

---

## Resumen global (informe exploratorio, 1 repetición)

| Tarea | A | B | C |
|---|---|---|---|
| Tarea 1 | 5.0 | 4.3 | 4.3 |
| Tarea 2 | 5.0 | 5.0 | 5.0 |
| Tarea 3 | 4.3 | 5.0 | 5.0 |
| Tarea 4 | 5.0 | 5.0 | 4.3 |
| Tarea 5 | 5.0 | 5.0 | 5.0 |
| **Media Global** | **4.86** | **4.86** | **4.72** |

## Alertas de sesgo (informe exploratorio)

1. Tarea 4 - Respuesta C: la información extra sobre aduanas podría valorarse como "proactividad" desde un sesgo personal, pero se penalizó por ir más allá de lo preguntado (criterio revisado en informe 3).
2. Tarea 1 - Respuesta C: la coletilla "Aquí tienes una posible respuesta" es un marcador de IA; se penalizó correctamente.
3. Diferenciación sutil: en la mayoría de tareas las respuestas son de alta calidad; se ha sido estricto con matices pequeños para evitar el sesgo de "todas son buenas, pongo un 5 a todo".
4. Sesgo de familiaridad: los tonos cálidos y coloquiales (Respuestas C en Tareas 1 y 3) resultan personalmente más atractivos; se ha evaluado objetivamente, penalizando cuando ese tono venía acompañado de fallos.

*Fin del informe exploratorio*
