# Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso

> Plugin de Claude Code `formularios-pleitos-mercantiles-y-concurso` · **33 formularios** · Mercantil · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para litigar ante la Sección de lo Mercantil: impugnación de acuerdos sociales, acción social e individual de responsabilidad de administradores, disolución judicial, derecho de información y de separación del socio, competencia desleal y publicidad ilícita, y escritos en el concurso de acreedores.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 33 está al final):

- **Demandas, peticiones y solicitudes iniciales** (24). Por ejemplo: Demanda del socio contra la sociedad en ejercicio de la acción de regreso (art. 331 LSC); Demanda de reclamación de la aportación no devuelta al socio tras reducir capital en una SL; Demanda de juicio ordinario por prohibición absoluta de registro de marca.
- **Resoluciones judiciales (autos, decretos, providencias, diligencias)** (1). Por ejemplo: Auto que acuerda acumular el juicio declarativo civil al procedimiento concursal.
- **Contratos, pactos y cláusulas** (3). Por ejemplo: Acuerdo con la administración concursal para resolver un leasing sin indemnización ni deuda nueva; Acuerdo de resolución de un contrato de renting con un cliente en concurso; Contrato de cesión de un crédito frente a una sociedad en concurso.
- **Comunicaciones, requerimientos y cartas** (2). Por ejemplo: Solicitud sobrevenida de medida cautelar de suspensión de acuerdo social sin audiencia del demandado; Solicitud al Juzgado de lo Mercantil de nombramiento judicial de auditor.
- **Escritos de trámite y otros** (3). Por ejemplo: Diligencia de ordenación que acusa recibo del juicio civil acumulado al concurso; Otrosí que pide acumular acciones de impugnación de acuerdos sociales a la de otra demanda anterior; Desistimiento de las medidas cautelares pedidas con la demanda en juicio por publicidad ilícita.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Demanda de impugnación de acuerdos de la junta general»
   - «Acción social de responsabilidad contra el administrador»
   - «Demanda por actos de competencia desleal»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-pleitos-mercantiles-y-concurso:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-pleitos-mercantiles-y-concurso:demanda-socio-contra-sociedad-ejercicio-accion-regreso-mer-0782`. Los nombres están en la lista de formularios de abajo.

## Qué hace Claude cuando usas un formulario

1. Comprueba que Jurisprudenciator está conectado. Si no lo está, se para y te dice cómo conectarlo: no redacta nada sin él. Todos los datos jurídicos del documento (artículos vigentes, sentencias con su ECLI, datos registrales) salen de Jurisprudenciator; nunca de memoria.
2. Te pide en una sola tanda los datos del caso (partes, órgano, fechas, importes…). Lo que no sepas queda como hueco visible.
3. Resuelve contigo las opciones que el formulario deja abiertas y decide qué párrafos opcionales entran según los hechos.
4. Aplica las notas de actualización de la revisión del 25-11-2026 (reformas legales, órganos judiciales de la LO 1/2025, plazos).
5. Comprueba en el BOE, con Jurisprudenciator, cada norma que cita el documento; si alguna ha cambiado, usa la redacción vigente y te lo dice.
6. Te entrega el documento en Word **tal cual es el formulario**: empieza por su primera línea, sin títulos, notas ni explicaciones añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. En el chat te dice lo que queda pendiente y, si es un escrito, el plazo y ante quién se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Antes de empezar

- **Dónde funciona:** en Claude Code y en Claude (web, escritorio y Cowork). Se instala desde este repositorio de GitHub o subiendo el ZIP del plugin.
- **Jurisprudenciator es imprescindible:** el plugin trae el conector y cada skill trabaja siempre con él. Sin una cuenta de Jurisprudenciator conectada, las skills se paran y no redactan nada. La primera vez hay que iniciar sesión (en Claude Code, con `/mcp`; o con tu URL personal: https://jurisprudenciator.lexiaipro.org/instalacion). Si ya tienes Jurisprudenciator conectado en Claude, las skills usan ese.
- **Espacio que ocupa:** unos 2.162 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-pleitos-mercantiles-y-concurso@formularios-pleitos-mercantiles-y-concurso`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-pleitos-mercantiles-y-concurso
/plugin install formularios-pleitos-mercantiles-y-concurso@formularios-pleitos-mercantiles-y-concurso
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-pleitos-mercantiles-y-concurso`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-pleitos-mercantiles-y-concurso/releases/latest/download/formularios-pleitos-mercantiles-y-concurso.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (33)

| Código | Formulario | Skill |
|---|---|---|
| MER-0782 | Demanda del socio contra la sociedad en ejercicio de la acción de regreso (art. 331 LSC) | `demanda-socio-contra-sociedad-ejercicio-accion-regreso-mer-0782` |
| MER-0783 | Demanda de reclamación de la aportación no devuelta al socio tras reducir capital en una SL | `demanda-reclamacion-aportacion-no-devuelta-socio-tras-mer-0783` |
| MER-0784 | Demanda de juicio ordinario por prohibición absoluta de registro de marca | `demanda-juicio-ordinario-prohibicion-absoluta-registro-mer-0784` |
| MER-0785 | Demanda del socio de una SL que ejerce el derecho de separación por falta de reparto de dividendos | `demanda-socio-sl-ejerce-derecho-separacion-falta-mer-0785` |
| MER-0786 | Demanda de nulidad de venta de participaciones sin cumplir requisitos estatutarios y legales | `demanda-nulidad-venta-participaciones-sin-cumplir-mer-0786` |
| MER-0787 | Demanda del acreedor contra el liquidador y los socios de una SL (arts. 397 y 399 LSC) | `demanda-acreedor-contra-liquidador-socios-sl-arts-397-mer-0787` |
| MER-0788 | Demanda de los administradores solicitando la disolución judicial de una SL | `demanda-administradores-solicitando-disolucion-mer-0788` |
| MER-0789 | Solicitud sobrevenida de medida cautelar de suspensión de acuerdo social sin audiencia del demandado | `solicitud-sobrevenida-medida-cautelar-suspension-mer-0789` |
| MER-0790 | Solicitud al Juzgado de lo Mercantil de nombramiento judicial de auditor | `solicitud-juzgado-lo-mercantil-nombramiento-judicial-mer-0790` |
| MER-0791 | Demanda mercantil para cesar al administrador de una SL que incumple la prohibición de competencia | `demanda-mercantil-cesar-administrador-sl-incumple-mer-0791` |
| MER-0792 | Acuerdo con la administración concursal para resolver un leasing sin indemnización ni deuda nueva | `acuerdo-administracion-concursal-resolver-leasing-sin-mer-0792` |
| MER-0793 | Acuerdo de resolución de un contrato de renting con un cliente en concurso | `acuerdo-resolucion-contrato-renting-cliente-concurso-mer-0793` |
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
| MER-0808 | Contrato de cesión de un crédito frente a una sociedad en concurso | `contrato-cesion-credito-frente-sociedad-concurso-mer-0808` |
| MER-0809 | Demanda de acción social de responsabilidad de un administrador-socio contra otro administrador | `demanda-accion-social-responsabilidad-administrador-mer-0809` |
| MER-0810 | Diligencia de ordenación que acusa recibo del juicio civil acumulado al concurso | `diligencia-ordenacion-acusa-recibo-juicio-civil-mer-0810` |
| MER-0811 | Auto que acuerda acumular el juicio declarativo civil al procedimiento concursal | `auto-acuerda-acumular-juicio-declarativo-civil-mer-0811` |
| MER-0812 | Otrosí que pide acumular acciones de impugnación de acuerdos sociales a la de otra demanda anterior | `otrosi-pide-acumular-acciones-impugnacion-acuerdos-mer-0812` |
| MER-0813 | Desistimiento de las medidas cautelares pedidas con la demanda en juicio por publicidad ilícita | `desistimiento-medidas-cautelares-pedidas-demanda-mer-0813` |
| MER-0814 | Demanda de reducción de precio por vicios ocultos contra la sociedad vendedora y sus administradores | `demanda-reduccion-precio-vicios-ocultos-contra-mer-0814` |

## Privacidad

Ver `PRIVACY.md`.
