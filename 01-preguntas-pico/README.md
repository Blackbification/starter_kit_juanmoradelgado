# 1. Preguntas PICO con IA

**[Español](#español) | [English](#english)**

---

## Español

Toda investigación clínica que llega a publicarse empieza igual: con una pregunta bien formulada. El formato PICO es el estándar para construirla, y la IA puede ayudarte a pasar de "me gustaría estudiar algo sobre insuficiencia cardiaca" a una pregunta concreta, factible y publicable en minutos.

### Qué es PICO

| Componente | Pregunta que responde | Ejemplo |
|---|---|---|
| **P** (población) | ¿En qué pacientes? | Adultos mayores de 75 años hospitalizados por insuficiencia cardiaca |
| **I** (intervención o exposición) | ¿Qué se hace o a qué están expuestos? | Inicio de iSGLT2 durante el ingreso |
| **C** (comparador) | ¿Frente a qué se compara? | Inicio diferido tras el alta |
| **O** (outcome, desenlace) | ¿Qué se mide? | Reingreso a 30 días |

Pregunta resultante: en adultos mayores de 75 años hospitalizados por insuficiencia cardiaca, ¿el inicio de iSGLT2 durante el ingreso, comparado con el inicio diferido tras el alta, reduce el reingreso a 30 días?

### Prompt 1: de idea vaga a preguntas PICO

Copia esto en Claude o ChatGPT y sustituye lo que va entre corchetes:

```
Actúa como metodólogo de investigación clínica. Tengo esta idea de
investigación todavía sin concretar: [describe tu idea en 1-3 frases,
por ejemplo: "algo sobre el uso de antibióticos en pacientes ancianos
con infección urinaria"].

Mi contexto: trabajo en [tipo de centro y servicio] y tengo acceso a
[tipo de datos o pacientes].

Genera 5 preguntas de investigación en formato PICO derivadas de mi
idea. Para cada una, presenta una tabla con los 4 componentes PICO,
el diseño de estudio más adecuado para responderla y una valoración
en una frase de su factibilidad en mi contexto.
```

### Prompt 2: someter la pregunta al filtro FINER

Una pregunta PICO correcta puede seguir siendo mala idea. El filtro FINER (factible, interesante, novedosa, ética, relevante) lo detecta:

```
Evalúa esta pregunta PICO con los criterios FINER: [pega tu pregunta].
Para cada criterio, puntúa de 1 a 5, justifica en una frase y propón
una mejora concreta. Termina con la versión revisada de la pregunta
incorporando las mejoras.
```

### Prompt 3: de la pregunta al protocolo

```
A partir de esta pregunta PICO: [pega tu pregunta], genera un esquema
preliminar de protocolo: diseño, criterios de inclusión y exclusión,
variable principal y secundarias, y los 3 principales sesgos que
amenazan este diseño con una estrategia de mitigación para cada uno.
No inventes cifras de tamaño muestral: indica qué datos necesitaría
para calcularlo.
```

### Tres errores que debes evitar

1. **Aceptar la primera pregunta que te devuelva el modelo.** Genera siempre varias y compáralas: la mejor rara vez es la primera.
2. **Dejar que la IA decida el desenlace principal.** El outcome lo eliges tú según relevancia clínica y datos disponibles; el modelo solo propone.
3. **Saltarte la verificación de novedad.** Antes de enamorarte de la pregunta, busca en PubMed si ya está respondida (el recurso 4 de este kit te enseña a hacerlo).

---

## English

Every published clinical study starts the same way: with a well-built question. PICO is the standard framework, and AI can take you from "I would like to study something about heart failure" to a specific, feasible, publishable question in minutes.

### What PICO is

| Component | Question it answers | Example |
|---|---|---|
| **P** (population) | Which patients? | Adults over 75 hospitalized for heart failure |
| **I** (intervention or exposure) | What is done or what are they exposed to? | SGLT2 inhibitor started during admission |
| **C** (comparator) | Compared with what? | Deferred initiation after discharge |
| **O** (outcome) | What is measured? | 30-day readmission |

### Prompt 1: from vague idea to PICO questions

```
Act as a clinical research methodologist. I have this still-unshaped
research idea: [describe your idea in 1-3 sentences].

My context: I work in [type of center and department] and I have
access to [type of data or patients].

Generate 5 research questions in PICO format derived from my idea.
For each one, present a table with the 4 PICO components, the most
appropriate study design to answer it and a one-sentence feasibility
assessment in my context.
```

### Prompt 2: run the FINER filter

```
Evaluate this PICO question against the FINER criteria (feasible,
interesting, novel, ethical, relevant): [paste your question]. Score
each criterion 1 to 5, justify in one sentence and propose a concrete
improvement. End with a revised version of the question incorporating
the improvements.
```

### Prompt 3: from question to protocol outline

```
From this PICO question: [paste your question], generate a preliminary
protocol outline: design, inclusion and exclusion criteria, primary
and secondary outcomes, and the 3 main biases threatening this design
with a mitigation strategy for each. Do not invent sample size
figures: state what data you would need to calculate it.
```

### Three mistakes to avoid

1. **Accepting the first question the model returns.** Always generate several and compare them.
2. **Letting the AI choose your primary outcome.** You choose it based on clinical relevance and available data; the model only proposes.
3. **Skipping the novelty check.** Before committing, search PubMed to see whether the question is already answered (resource 4 in this kit shows you how).

---

[← Volver al inicio / Back to home](../README.md)
