# 4. Búsqueda en PubMed con MeSH e IA

**[Español](#español) | [English](#english)**

---

## Español

Una búsqueda bien construida en PubMed es la base de cualquier introducción, discusión o revisión. La IA acelera muchísimo el proceso, pero tiene una trampa concreta que debes conocer. Esta chuleta te da el flujo completo.

### La anatomía de una buena estrategia

Una estrategia profesional combina, para cada concepto de tu pregunta PICO:

1. **Términos MeSH**: el vocabulario controlado de PubMed. Ejemplo: `"Heart Failure"[Mesh]`
2. **Términos libres en título y resumen**: capturan los artículos aún no indexados. Ejemplo: `"heart failure"[tiab]`
3. **Operadores booleanos**: `OR` dentro de cada concepto, `AND` entre conceptos, `NOT` casi nunca.

Esqueleto tipo:

```
("Heart Failure"[Mesh] OR "heart failure"[tiab] OR "cardiac failure"[tiab])
AND
("Sodium-Glucose Transporter 2 Inhibitors"[Mesh] OR "SGLT2 inhibitor*"[tiab]
 OR empagliflozin[tiab] OR dapagliflozin[tiab])
AND
("Patient Readmission"[Mesh] OR readmission*[tiab] OR rehospitalization*[tiab])
```

### Prompt: generar la estrategia con IA

```
Actúa como documentalista biomédico experto en PubMed. Mi pregunta de
investigación es: [pega tu pregunta PICO].

Construye una estrategia de búsqueda para PubMed:
1. Identifica los 2-4 conceptos clave (normalmente P, I y O; el
   comparador rara vez se incluye).
2. Para cada concepto, propón términos MeSH y sinónimos en texto libre
   con la etiqueta [tiab], incluyendo variantes con truncamiento (*).
3. Combina con OR dentro de cada concepto y AND entre conceptos.
4. Presenta la estrategia final en un solo bloque listo para pegar en
   PubMed, y una versión más sensible y otra más específica.
```

### La trampa: los MeSH inventados

Los modelos de lenguaje se inventan términos MeSH que suenan perfectamente plausibles pero no existen. Un término inventado no da error en PubMed: simplemente devuelve resultados incompletos sin que te des cuenta. Por eso el paso de verificación no es opcional:

1. Abre la [MeSH Database](https://www.ncbi.nlm.nih.gov/mesh/) y comprueba **uno por uno** que cada término MeSH propuesto existe y con esa grafía exacta.
2. De paso, revisa en cada ficha los *Entry Terms*: sinónimos oficiales que quizá la IA no te haya propuesto.
3. Pega la estrategia en PubMed y revisa el recuadro *Search details* para confirmar cómo la ha interpretado.

### Calibrar el resultado

- **¿Miles de resultados?** Añade el concepto de desenlace, usa [Filters] de tipo de estudio o cambia [tiab] por [ti] en el concepto más genérico.
- **¿Menos de 20 resultados?** Elimina el concepto menos esencial, añade sinónimos o quita filtros. Cuidado: pocas veces significa que no hay literatura; muchas veces significa que tu estrategia es demasiado estrecha.
- **Prueba del algodón**: busca 2-3 artículos clave que ya conozcas sobre el tema. Si tu estrategia no los recupera, está mal construida.

### Última milla

Exporta los resultados a un gestor de referencias (Zotero es gratuito) desde el primer día. Guardar PDFs sueltos en el escritorio es la principal causa de sufrimiento evitable en la redacción posterior.

---

## English

A well-built PubMed search underpins any introduction, discussion or review. AI speeds up the process enormously, but there is one specific trap you must know about.

### Anatomy of a good strategy

For each concept in your PICO question, combine: **MeSH terms** (PubMed's controlled vocabulary, e.g. `"Heart Failure"[Mesh]`), **free-text terms in title/abstract** (`"heart failure"[tiab]`) to capture not-yet-indexed articles, and **Boolean operators**: `OR` within each concept, `AND` between concepts, `NOT` almost never.

### Prompt: generate the strategy with AI

```
Act as a biomedical librarian expert in PubMed. My research question
is: [paste your PICO question].

Build a PubMed search strategy:
1. Identify the 2-4 key concepts (usually P, I and O; the comparator
   is rarely included).
2. For each concept, propose MeSH terms and free-text synonyms tagged
   [tiab], including truncation variants (*).
3. Combine with OR within each concept and AND between concepts.
4. Present the final strategy in a single block ready to paste into
   PubMed, plus a more sensitive and a more specific version.
```

### The trap: hallucinated MeSH terms

Language models invent MeSH terms that sound perfectly plausible but do not exist. An invented term does not throw an error in PubMed: it silently returns incomplete results. Verification is therefore not optional: check every proposed MeSH term one by one in the [MeSH Database](https://www.ncbi.nlm.nih.gov/mesh/), harvest the official *Entry Terms* while you are there, and confirm in PubMed's *Search details* how your query was interpreted.

### Calibrating

Thousands of hits: add the outcome concept, use study-type filters, or switch [tiab] to [ti] on the broadest concept. Fewer than 20: drop the least essential concept or add synonyms. Acid test: if your strategy does not retrieve 2-3 key articles you already know, it is badly built. And export everything to a reference manager (Zotero is free) from day one.

---

[← Volver al inicio / Back to home](../README.md)
