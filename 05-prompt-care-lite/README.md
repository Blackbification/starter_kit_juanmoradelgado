# 5. Prompt CARE lite: redacta casos clínicos con estructura profesional

**[Español](#español) | [English](#english)**

---

## Español

El caso clínico es la puerta de entrada a la publicación para la mayoría de los clínicos. La guía **CARE** (CAse REport, respaldada por la red EQUATOR) define los 13 ítems que toda revista espera encontrar. Este prompt convierte a Claude o ChatGPT en un asistente de redacción que sigue esa estructura.

### Cómo usarlo

1. Copia el contenido de [`prompt_care_lite_es.md`](prompt_care_lite_es.md) (o la [versión en inglés](prompt_care_lite_en.md)).
2. Pégalo como primer mensaje de una conversación nueva, o mejor aún, como instrucciones de un proyecto de Claude o un GPT personalizado.
3. En el mensaje siguiente, aporta los datos clínicos del caso **ya anonimizados**: sin nombres, fechas exactas, números de historia ni cualquier dato que permita identificar al paciente.
4. Responde a las preguntas de clarificación que te haga antes de redactar.

### Qué hace esta versión lite

- Estructura el caso siguiendo los 13 ítems CARE en orden.
- Te pregunta por la información que falte antes de inventar nada.
- Redacta con estilo académico biomédico en español o inglés.

### Qué NO hace (y la versión completa sí)

La versión completa que trabajamos en mis programas añade la checklist expandida con los 31 subítems verificables, el sistema de auditoría automática que puntúa el cumplimiento CARE ítem a ítem de cualquier caso ya escrito, y las adaptaciones de formato a póster, comunicación oral y capítulo de libro. Si te quedas con ganas: [juanmoradelgado.com](https://juanmoradelgado.com).

### Recordatorios innegociables

- **Consentimiento informado**: para publicar un caso necesitas el consentimiento del paciente. Sin él no hay caso, por interesante que sea.
- **Anonimización antes de la IA**: los datos identificables nunca entran en una herramienta de IA generalista.
- **La IA redacta, tú respondes**: la responsabilidad científica y la veracidad clínica del texto final son siempre del autor humano.

---

## English

The case report is the entry door to publication for most clinicians. The **CARE** guideline (CAse REport, endorsed by the EQUATOR Network) defines the 13 items every journal expects. This prompt turns Claude or ChatGPT into a writing assistant that follows that structure.

### How to use it

1. Copy the content of [`prompt_care_lite_en.md`](prompt_care_lite_en.md) (or the [Spanish version](prompt_care_lite_es.md)).
2. Paste it as the first message of a new conversation, or better, as instructions of a Claude Project or a custom GPT.
3. In the next message, provide the clinical data **already de-identified**: no names, exact dates, record numbers or any identifying detail.
4. Answer its clarification questions before it drafts.

### What this lite version does

It structures the case following the 13 CARE items in order, asks for missing information before inventing anything, and writes in biomedical academic style in Spanish or English.

### What it does NOT do (and the full version does)

The full version used in my programs adds the expanded 31-subitem verifiable checklist, an automatic audit system that scores CARE compliance item by item on any already-written case, and format adaptations for posters, oral communications and book chapters. Curious? [juanmoradelgado.com](https://juanmoradelgado.com).

### Non-negotiable reminders

- **Informed consent**: publishing a case requires the patient's consent. No consent, no case.
- **De-identify before AI**: identifiable data never enters a general-purpose AI tool.
- **AI drafts, you answer for it**: scientific responsibility for the final text always rests with the human author.

---

[← Volver al inicio / Back to home](../README.md)
