---
name: demanda-nulidad-venta-participaciones-sin-cumplir-mer-0786
description: "Demanda de nulidad de venta de participaciones sin cumplir requisitos estatutarios y legales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de nulidad de venta de participaciones sin cumplir requisitos estatutarios y legales

> Formulario **MER-0786** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 25-11-2026.

## Qué es

Demanda de juicio ordinario por la que un socio de una sociedad de responsabilidad limitada impugna la compraventa voluntaria inter vivos de participaciones sociales realizada entre otros socios y un tercero sin cumplir los requisitos legales y estatutarios de comunicación a los administradores y de consentimiento de la sociedad (arts. 107, 108 y 112 de la Ley de Sociedades de Capital), para que se declare su nulidad o ineficacia y se mantenga la composición social anterior.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de nulidad de venta de participaciones sin cumplir requisitos estatutarios y legales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de nulidad de venta de participaciones sin cumplir requisitos estatutarios y legales” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:demanda-nulidad-venta-participaciones-sin-cumplir-mer-0786`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (9 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº DE DOCUMENTO (6 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA SOCIEDAD ADQUIRENTE (4 veces)
- [ ] DOMICILIO (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] PLAZO (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] NOMBRE DEL NOTARIO (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL CODEMANDADO (3 veces)
- [ ] REPETIR PARA CADA CODEMANDADO PERSONA FÍSICA: (3 veces)
- [ ] NIF (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (2 veces)
- [ ] Nº (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] AÑO
- [ ] COLEGIO DE ABOGADOS
- [ ] DESCRIPCIÓN DE LA ACTIVIDAD O ESTABLECIMIENTOS
- [ ] DOMICILIO SOCIAL
- [ ] DÍA
- [ ] IMPORTE EN LETRA
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR
- [ ] Nº DE ARTÍCULO
- [ ] Nº DE COLEGIADO
- [ ] OBJETO SOCIAL
- [ ] PORCENTAJE
- [ ] SEDE

## Normas que cita el formulario

- art. 107.2 Real Decreto Legislativo 1/2010
- art. 87 LOPJ
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 107 TRLSC
- art. 253.1 LEC
- art. 251 LEC
- art. 23 LEC
- art. 399 LEC
- art. 42 Código de Comercio
- art. 108 TRLSC
- art. 112 TRLSC
- art. 1311 CC
- art. 394.1 LEC

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…y también el domicilio social de la codemandada persona jurídica (art. 87 LOPJ).»: comprobar la cita de la LOPJ tras la reforma de la LO 1/2025 en cuanto a las secciones de lo mercantil de los tribunales de instancia.
- Junto a «…/Dña. [NOMBRE Y APELLIDOS] Representación procesal: D./Dña. [NOMBRE Y APELLIDOS]»: requisito de procedibilidad (art. 5 LO 1/2025): antes de demandar hay que intentar un medio adecuado de solución de controversias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2.
- Junto a «…ersias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2.]»: el original citaba la STS de 10 de abril de 2007 con dos números de recurso distintos (2928/2000 y 2028/2000); se ha unificado con el primero, comprobar el dato antes de usarlo.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTA EXPLICATIVA

El art. 107 de la Ley de Sociedades de Capital determina en su apartado primero dos regímenes diferentes para la transmisión de las participaciones sociales de sociedades limitadas. Un régimen de libre transmisión entre socios, extensible a los cónyuges, ascendientes o descendientes de los mismos, o a favor de sociedades del mismo grupo, en los términos previstos en el art. 42 del Código de Comercio. Y un segundo régimen sometido a restricciones, cuando la transmisión se haga a personas diferentes de las antes relacionadas, que incluye comunicación a los administradores y acuerdo de la Junta. En el supuesto de este modelo no se ha puesto en conocimiento de los socios la transmisión a persona extraña a la entidad, por lo que se pide que se declare la nulidad de la compraventa en cuestión, de manera que el cambio de titularidad de las participaciones sociales sea ineficaz, manteniéndose la composición social existente antes del acto impugnado.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
