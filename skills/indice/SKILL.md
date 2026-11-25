---
name: indice
description: "Índice de los 33 formularios de Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso: índice de formularios

> Plugin `formularios-pleitos-mercantiles-y-concurso` · 33 formularios · normativa revisada el 25-11-2026.

## Qué es

Para litigar ante la Sección de lo Mercantil: impugnación de acuerdos sociales, acción social e individual de responsabilidad de administradores, disolución judicial, derecho de información y de separación del socio, competencia desleal y publicidad ilícita, y escritos en el concurso de acreedores.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Demanda de impugnación de acuerdos de la junta general»
- «Acción social de responsabilidad contra el administrador»
- «Demanda por actos de competencia desleal»

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

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-pleitos-mercantiles-y-concurso:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (24)

| Código | Formulario | Skill |
|---|---|---|
| MER-0782 | Demanda del socio contra la sociedad en ejercicio de la acción de regreso (art. 331 LSC) | `demanda-socio-contra-sociedad-ejercicio-accion-regreso-mer-0782` |
| MER-0783 | Demanda de reclamación de la aportación no devuelta al socio tras reducir capital en una SL | `demanda-reclamacion-aportacion-no-devuelta-socio-tras-mer-0783` |
| MER-0784 | Demanda de juicio ordinario por prohibición absoluta de registro de marca | `demanda-juicio-ordinario-prohibicion-absoluta-registro-mer-0784` |
| MER-0785 | Demanda del socio de una SL que ejerce el derecho de separación por falta de reparto de dividendos | `demanda-socio-sl-ejerce-derecho-separacion-falta-mer-0785` |
| MER-0786 | Demanda de nulidad de venta de participaciones sin cumplir requisitos estatutarios y legales | `demanda-nulidad-venta-participaciones-sin-cumplir-mer-0786` |
| MER-0787 | Demanda del acreedor contra el liquidador y los socios de una SL (arts. 397 y 399 LSC) | `demanda-acreedor-contra-liquidador-socios-sl-arts-397-mer-0787` |
| MER-0788 | Demanda de los administradores solicitando la disolución judicial de una SL | `demanda-administradores-solicitando-disolucion-mer-0788` |
| MER-0791 | Demanda mercantil para cesar al administrador de una SL que incumple la prohibición de competencia | `demanda-mercantil-cesar-administrador-sl-incumple-mer-0791` |
| MER-0794 | Demanda de exclusión de un socio de SL con participación igual o superior al 25 por ciento | `demanda-exclusion-socio-sl-participacion-igual-mer-0794` |
| MER-0795 | Demanda de nombramiento judicial de auditor de una SL pedida por socios con el 5 por ciento | `demanda-nombramiento-judicial-auditor-sl-pedida-socios-mer-0795` |
| MER-0796 | Demanda de impugnación de acuerdos del consejo de administración de una sociedad anónima | `demanda-impugnacion-acuerdos-consejo-administracion-mer-0796` |
| MER-0797 | Demanda de impugnación de acuerdos del consejo de administración de una SA conforme a la antigua LEC | `demanda-impugnacion-acuerdos-consejo-administracion-sa-mer-0797` |
| MER-0798 | Demanda de impugnación de acuerdos de la junta general ordinaria de una sociedad anónima | `demanda-impugnacion-acuerdos-junta-general-ordinaria-mer-0798` |
| MER-0799 | Demanda de impugnación de acuerdos de la junta general ordinaria de una SA conforme a la antigua LEC | `demanda-impugnacion-acuerdos-junta-general-ordinaria-mer-0799` |
| MER-0800 | Demanda de la sociedad contra los administradores de una SL por la acción social de responsabilidad | `demanda-sociedad-contra-administradores-sl-accion-mer-0800` |
| MER-0801 | Demanda de impugnación de acuerdos de una SL con suspensión y anotación preventiva de la demanda | `demanda-impugnacion-acuerdos-sl-suspension-anotacion-mer-0801` |
| MER-0802 | Demanda de impugnación de acuerdos del consejo de administración de una sociedad limitada | `demanda-impugnacion-acuerdos-consejo-administracion-mer-0802` |
| MER-0803 | Demanda de disolución judicial de una sociedad anónima presentada por el administrador o por socios | `demanda-disolucion-judicial-sociedad-anonima-mer-0803` |
| MER-0804 | Demanda de impugnación de acuerdos de una SA con suspensión y anotación preventiva de la demanda | `demanda-impugnacion-acuerdos-sa-suspension-anotacion-mer-0804` |
| MER-0805 | Demanda de disolución judicial de una sociedad anónima presentada por accionistas | `demanda-disolucion-judicial-sociedad-anonima-mer-0805` |
| MER-0806 | Demanda de socios contra los administradores de una SL por la acción individual de responsabilidad | `demanda-socios-contra-administradores-sl-accion-mer-0806` |
| MER-0807 | Demanda de disolución judicial de una sociedad limitada presentada por socios | `demanda-disolucion-judicial-sociedad-limitada-mer-0807` |
| MER-0809 | Demanda de acción social de responsabilidad de un administrador-socio contra otro administrador | `demanda-accion-social-responsabilidad-administrador-mer-0809` |
| MER-0814 | Demanda de reducción de precio por vicios ocultos contra la sociedad vendedora y sus administradores | `demanda-reduccion-precio-vicios-ocultos-contra-mer-0814` |

### Resoluciones judiciales (autos, decretos, providencias, diligencias) (1)

| Código | Formulario | Skill |
|---|---|---|
| MER-0811 | Auto que acuerda acumular el juicio declarativo civil al procedimiento concursal | `auto-acuerda-acumular-juicio-declarativo-civil-mer-0811` |

### Contratos, pactos y cláusulas (3)

| Código | Formulario | Skill |
|---|---|---|
| MER-0792 | Acuerdo con la administración concursal para resolver un leasing sin indemnización ni deuda nueva | `acuerdo-administracion-concursal-resolver-leasing-sin-mer-0792` |
| MER-0793 | Acuerdo de resolución de un contrato de renting con un cliente en concurso | `acuerdo-resolucion-contrato-renting-cliente-concurso-mer-0793` |
| MER-0808 | Contrato de cesión de un crédito frente a una sociedad en concurso | `contrato-cesion-credito-frente-sociedad-concurso-mer-0808` |

### Comunicaciones, requerimientos y cartas (2)

| Código | Formulario | Skill |
|---|---|---|
| MER-0789 | Solicitud sobrevenida de medida cautelar de suspensión de acuerdo social sin audiencia del demandado | `solicitud-sobrevenida-medida-cautelar-suspension-mer-0789` |
| MER-0790 | Solicitud al Juzgado de lo Mercantil de nombramiento judicial de auditor | `solicitud-juzgado-lo-mercantil-nombramiento-judicial-mer-0790` |

### Escritos de trámite y otros (3)

| Código | Formulario | Skill |
|---|---|---|
| MER-0810 | Diligencia de ordenación que acusa recibo del juicio civil acumulado al concurso | `diligencia-ordenacion-acusa-recibo-juicio-civil-mer-0810` |
| MER-0812 | Otrosí que pide acumular acciones de impugnación de acuerdos sociales a la de otra demanda anterior | `otrosi-pide-acumular-acciones-impugnacion-acuerdos-mer-0812` |
| MER-0813 | Desistimiento de las medidas cautelares pedidas con la demanda en juicio por publicidad ilícita | `desistimiento-medidas-cautelares-pedidas-demanda-mer-0813` |
