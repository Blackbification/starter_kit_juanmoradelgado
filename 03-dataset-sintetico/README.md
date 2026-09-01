# 3. Dataset sintético para practicar análisis con IA

**[Español](#español) | [English](#english)**

---

## Español

La mejor forma de aprender a analizar datos con IA es practicar con una base de datos que se parezca a las reales, pero sin ningún riesgo de confidencialidad. Este dataset contiene **150 pacientes ficticios** ingresados por insuficiencia cardiaca, generado íntegramente por ordenador con relaciones estadísticas plausibles. Ningún dato procede de pacientes reales.

**Archivo**: [`pacientes_ic_sintetico.csv`](pacientes_ic_sintetico.csv)

### Diccionario de variables

| Variable | Tipo | Descripción |
|---|---|---|
| `id_paciente` | Texto | Identificador ficticio (P001 a P150) |
| `edad` | Numérica | Edad en años |
| `sexo` | Categórica | Mujer / Hombre |
| `fevi_pct` | Numérica | Fracción de eyección del ventrículo izquierdo (%). Tiene valores perdidos |
| `tipo_ic` | Categórica | FEr (reducida, < 40 %), FElr (ligeramente reducida, 40-49 %), FEp (preservada, ≥ 50 %). Procede del registro clínico, por lo que puede constar aunque falte la FEVI numérica |
| `diabetes`, `epoc`, `fibrilacion_auricular`, `erc` | Binarias | Comorbilidades (1 = sí, 0 = no). ERC = enfermedad renal crónica |
| `creatinina_mg_dl` | Numérica | Creatinina sérica al ingreso (mg/dl) |
| `fge_ml_min` | Numérica | Filtrado glomerular estimado (ml/min/1,73 m²) |
| `ntprobnp_pg_ml` | Numérica | NT-proBNP al ingreso (pg/ml). Tiene valores perdidos |
| `hemoglobina_g_dl` | Numérica | Hemoglobina al ingreso (g/dl). Tiene valores perdidos |
| `sodio_meq_l` | Numérica | Sodio sérico al ingreso (mEq/l) |
| `isglt2`, `betabloqueante`, `ieca_ara2_arni` | Binarias | Tratamiento al alta (1 = sí, 0 = no) |
| `dias_estancia` | Numérica | Duración del ingreso en días |
| `reingreso_30d` | Binaria | Reingreso por cualquier causa a 30 días (1 = sí) |
| `mortalidad_90d` | Binaria | Mortalidad por cualquier causa a 90 días (1 = sí) |

### Cómo practicar

Sube el CSV a Claude o ChatGPT y trabaja los tres ejercicios en orden. La gracia no es que la IA "te haga el análisis", sino aprender a dirigirla y a auditar lo que devuelve.

#### Ejercicio 1: exploración y tabla 1

```
Te adjunto una base de datos sintética de pacientes ingresados por
insuficiencia cardiaca. Antes de analizar nada: describe la estructura,
identifica valores perdidos y valores imposibles o sospechosos, y dime
qué decisiones debo tomar antes del análisis. Después genera una tabla 1
de características basales estratificada por reingreso a 30 días, usando
mediana y rango intercuartílico para las variables no normales.
```

Comprueba: ¿ha detectado los valores perdidos de FEVI, NT-proBNP y hemoglobina? ¿Te ha preguntado qué hacer con ellos o ha decidido por su cuenta?

#### Ejercicio 2: comparación entre grupos

```
Compara los pacientes con y sin reingreso a 30 días. Elige el test
estadístico adecuado para cada variable justificando la elección
(normalidad, tipo de variable), presenta los resultados con su tamaño
de efecto e interpreta clínicamente los hallazgos. Señala explícitamente
que esta base es sintética y los resultados no son generalizables.
```

Comprueba: ¿ha comprobado la normalidad antes de elegir entre t de Student y U de Mann-Whitney? ¿Ha caído en interpretar los valores de p como importancia clínica?

#### Ejercicio 3: modelo multivariable

```
Ajusta una regresión logística con reingreso a 30 días como variable
dependiente. Propón qué variables incluir y justifica cada inclusión
(criterio clínico, no solo estadístico). Presenta odds ratios con
intervalos de confianza al 95 %, evalúa la bondad de ajuste y la
posible colinealidad, y redacta el párrafo de resultados como si fuera
para un manuscrito.
```

Comprueba: ¿el número de eventos soporta el número de variables incluidas (regla orientativa de 10 eventos por variable)? ¿Ha incluido a la vez FEVI numérica y tipo de IC (colinealidad)?

### La lección de fondo

Si la IA comete errores con estos 150 pacientes ficticios, los cometerá con tus datos reales. Aprender a detectarlos es la diferencia entre usar la IA como juguete y usarla como herramienta de investigación.

---

## English

The best way to learn AI-assisted data analysis is to practice on a database that looks real but carries zero confidentiality risk. This dataset contains **150 fictional patients** admitted for heart failure, fully computer-generated with plausible statistical relationships. No data comes from real patients.

**File**: [`pacientes_ic_sintetico.csv`](pacientes_ic_sintetico.csv)

### Data dictionary (summary)

Variables include demographics (`edad` = age, `sexo` = sex), left ventricular ejection fraction (`fevi_pct`, with missing values) and HF type (`tipo_ic`: reduced, mildly reduced, preserved), comorbidities (`diabetes`, `epoc` = COPD, `fibrilacion_auricular` = atrial fibrillation, `erc` = chronic kidney disease), admission labs (`creatinina_mg_dl`, `fge_ml_min` = eGFR, `ntprobnp_pg_ml`, `hemoglobina_g_dl`, `sodio_meq_l`), discharge treatment (`isglt2`, `betabloqueante`, `ieca_ara2_arni`), length of stay (`dias_estancia`) and outcomes: 30-day all-cause readmission (`reingreso_30d`) and 90-day all-cause mortality (`mortalidad_90d`).

### How to practice

Upload the CSV to Claude or ChatGPT and work through three exercises: (1) data exploration and a Table 1 stratified by readmission, checking whether the model detects missing values before analyzing; (2) group comparison with justified test selection and effect sizes; (3) a logistic regression for 30-day readmission, checking events-per-variable and collinearity (numeric LVEF and HF type together). The point is not that the AI "does the analysis for you" but learning to steer it and audit what it returns: if it makes mistakes with 150 fictional patients, it will make them with your real data.

---

[← Volver al inicio / Back to home](../README.md)
