# Plantilla: diccionario de variables / Template: variable dictionary

Rellena una fila por variable de tu base de datos. Las primeras filas van cumplimentadas como ejemplo; sustitúyelas por las tuyas.

Fill one row per variable in your database. The first rows are filled in as an example; replace them with your own.

## Identificación del proyecto / Project identification

| Campo | Contenido |
|---|---|
| Título del proyecto / Project title | |
| Investigador responsable / Lead investigator | |
| Unidad de análisis (qué es una fila) / Unit of analysis (what one row is) | Un paciente / One patient |
| Fecha de creación del diccionario / Dictionary creation date | AAAA-MM-DD |
| Versión / Version | 1.0 |

## Diccionario / Dictionary

| Variable | Etiqueta / Label | Tipo / Type | Unidades o códigos / Units or codes | Rango plausible / Plausible range | Fuente / Source | Notas / Notes |
|---|---|---|---|---|---|---|
| id_paciente | Identificador anonimizado | Texto | P001, P002... | | Asignado al incluir | Correspondencia con NHC guardada aparte en entorno seguro |
| fecha_ingreso | Fecha de ingreso | Fecha | AAAA-MM-DD | | Historia clínica | |
| edad | Edad al ingreso | Numérica | Años | 18-110 | Historia clínica | |
| sexo | Sexo | Binaria | 0 = hombre; 1 = mujer | 0-1 | Historia clínica | |
| diabetes | Diabetes mellitus | Binaria | 0 = no; 1 = sí | 0-1 | Historia clínica | Cualquier tipo |
| creatinina_mg_dl | Creatinina sérica al ingreso | Numérica | mg/dl | 0,2-15 | Laboratorio | Primera determinación del ingreso |
| exitus_90d | Mortalidad a 90 días | Binaria | 0 = no; 1 = sí | 0-1 | Historia clínica y registro | Desenlace principal |
| | | | | | | |
| | | | | | | |
| | | | | | | |

## Recordatorios / Reminders

- Perdidos en blanco, nunca 999 ni "ND" / Missing left blank, never 999 or "N/A".
- Una celda, un dato / One cell, one fact.
- Nombres de variable sin espacios, tildes ni eñes / Variable names without spaces or accents.
- Ningún dato identificable en esta hoja / No identifiable data in this sheet.
- Registra en "Versión" cualquier cambio del diccionario una vez empezada la recogida / Log any dictionary change in "Version" once collection has started.
