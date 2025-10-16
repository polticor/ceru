<!-- Habilitar Mermaid en GitHub Pages (cliente) -->
<script type="module">
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
  mermaid.initialize({
    startOnLoad: true,
    securityLevel: 'strict'  // usa 'loose' sólo si necesitas <br/> u HTML en labels
  });
</script>


# PROYECTO: Planta de Tratamiento de Residuos Hospitalarios — Polticor S.A.

## Portada

- **Proyecto:** *Planta de Tratamiento de Residuos Hospitalarios – Polticor S.A.*  
- **Titular:** **Polticor S.A.** — **RUT 214860570013**  
- **Contacto institucional:** info@polticor.com | Colman 4590 – San Salvador 1478, CP 11800, Montevideo, UY | Tel. 0800 1444* | https://polticor.com/  
- **Ubicación del proyecto:** **Camino Oncativo 3154, Padrón 60790, Montevideo, Uruguay**  
- **Objetivo regulatorio:** **Clasificación Ambiental A** (DINACEA), con **EsIA** adjunto  
- **Tecnologías principales:** **Autoclave por vapor (950×3000 mm; 165 kg/ciclo; ~45 min/ciclo) + trituración**  
- **Configuración inicial:** **3 líneas** (escalable a **5–7** líneas)  
- **Generación de vapor:** **2 × 530 kgv/h** (**N+1**, desfase entre líneas de **15 min**)  
- **Capacidad meta:** **360 t/mes (régimen normal, OEE 75%)**; **475 t/mes (extraordinario, OEE 100%)**  
- **Efluentes:** **sistema interno** con **templado < 40 °C** y **punto de muestreo**; **descarga a colector**  
- **Trazabilidad y datos:** **Odoo on-premise** (QR por lote/ciclo; CSV/PDF con **hash SHA-256**; **retención ≥ 5 años**; **backup** diario incremental + semanal completo off-site)  
- **Observación:** **Potencia eléctrica disponible pendiente de confirmación con UTE**  
- **Control documental:** Versión: **v0.1 (Borrador)** | Fecha: **[AAAA-MM-DD]** | Responsable: **[Nombre / Cargo / Firma]**

> **Nota de auditoría (portada / control de versión):** Registrar versión, fecha, responsable técnico, y vincular a la **Matriz de Control de Documentos** (códigos, vigencias, histórico de cambios).

---

## Declaración metodológica (ISO 14040/14044)

### 1) Meta y alcance
- **Meta del estudio:** sustentar técnica y documentalmente la **Clasificación Ambiental A** y el **EsIA**, demostrando desempeño superior a prácticas de referencia mediante **gestión integrada ISO** (9001/14001/45001/50001/17665-1/EN 285/27001/19011/31000).  
- **Alcance (límite del sistema):** desde **recepción** (portal gamma, báscula, verificación QR) → **almacenamiento “sucio”** (depresión/ extracción) → **autoclave** → **trituración** → **acondicionamiento** → **expedición**. Auxiliares incluidos: **vapor/condensado**, **agua de caldera**, **eléctrico/backup/FV**, **aire comprimido**, **HVAC/extracción**, **sistema de efluentes** (templado < 40 °C), **trazabilidad digital** (Odoo).  
- **Exclusiones de tratamiento:** anatómicos, químicos/citotóxicos y radioactivos (estos últimos **detectados y rechazados** en portal). Disposición final **fuera del límite** (operadores autorizados).  
- **Unidad funcional de reporte:** **1 tonelada** de RSS tratados y esterilizados conforme **ISO 17665-1 / EN 285**.

### 2) Inventario del ciclo de vida (LCI)
- **Entradas principales:** RSS por lote (kg), **vapor de proceso** (kg/h), **energía eléctrica** (kWh), **agua de caldera** (m³), aire comprimido (Nm³/h).  
- **Salidas y emisiones controladas:** material **esterilizado y triturado** (kg), **condensado templado < 40 °C** (m³) con parámetros **T/pH/SST/DQO/O&G**, **ruido perimetral** (dB), **bioaerosoles** en salas “sucias” (UFC/m³), **residuos secundarios** (filtros/consumibles).  
- **Puntos de medición/registro:** curvas **T/P** por ciclo; **T vertido** y muestreo en punto de control; energía (kWh), vapor (kg/h) y balance de masa (báscula in/egreso); **ΔP/Q** de HVAC; ruido en línea de propiedad; **trazabilidad Odoo** (hash, QR, CSV/PDF).  
- **Calidad de datos:** fuentes de fabricante, simulaciones validadas, ensayos FAT/SAT y **PMSA** operativo.

### 3) Evaluación de impactos (LCIA)
- **Categorías priorizadas:** **energía** (kWh/t; picos), **agua/efluentes térmicos** (m³/t; T<40 °C; pH/SST/DQO/O&G), **emisiones acústicas** (dB en línea de propiedad), **bioaerosoles/olores** en procesos de recepción y trituración, **riesgos SST** (vapor, vacío, manipulación, tránsito).  
- **Modelos y criterios:** cumplimiento **normativo uruguayo** (vertidos/ruido) y metas internas **ISO 14001/50001**; aceptación de esterilización **ISO 17665-1/EN 285** (BI/IC, curvas T/P).

### 4) Interpretación y mejora continua (PDCA)
- **Interpretación:** análisis de desempeño vs. metas (KPI), identificación de **incertidumbres** (factores de simultaneidad, cargas variables), y priorización de **acciones correctivas**.  
- **Mejora continua:** **recuperación de calor** del condensado (precalentamiento), **arranques escalonados** de líneas, **encapsulados acústicos** y optimización de **HVAC** por ΔP/Q y ACH, uso de **FV** para offset en oficinas y servicios auxiliares.  
- **Verificación:** auditorías internas conforme **ISO 19011**; seguridad de información y backups bajo **ISO 27001**; **pruebas de restauración mensuales** documentadas.

### 5) Integración con el EsIA (DINACEA) y control documental
- **Alineación EsIA:** línea base (ruido/efluentes/bioaerosoles), descripción del proyecto, análisis de impactos, medidas de mitigación, **PMSA**, plan de relación comunitaria y **matriz de cumplimiento**.  
- **Evidencias y anexos:** planos, memorias de cálculo (vapor/agua/eléctrico), fichas de equipos, SOP (recepción, autoclave, trituración, HVAC, efluentes), criterios FAT/SAT, reportes de laboratorio y bitácoras **Odoo**.  
- **Trazabilidad:** **Matriz requisito → evidencia → KPI → responsable → sección/anexo** con control de versiones.

> **Nota de auditoría (metodología):** Referenciar explícitamente **ISO 14040/14044**, **ISO 17665-1/EN 285**, **ISO 9001/14001/45001/50001/27001/19011/31000** en la **Matriz de Correspondencias**. Mantener archivos fuente (curvas, muestreos, registros Odoo) con **códigos y vigencias**.

---

## Justificación del “español internacional neutro”

Se adopta **español internacional neutro** para asegurar **interoperabilidad regional MERCOSUR**, facilitar la **revisión técnica** por contrapartes extranjeras (academia, proveedores, auditores) y promover **transparencia** y **transferencia de conocimiento** sin perjuicio de la **jerarquía normativa uruguaya**. La redacción neutra minimiza ambigüedades, favorece la comparabilidad entre estándares **ISO** y **EN**, y permite la futura publicación de **datos abiertos** (indicadores ambientales y de desempeño) en un formato comprensible más allá del ámbito local.

> **Nota de auditoría (idioma y referencias):** Mantener glosado interno de siglas **en línea** (no glosario separado) la primera vez que aparezcan. Verificar coherencia terminológica con **normativa uruguaya** y con manuales de fabricante.

---

## Índice general (alineado con ISO 14040/14044 y EsIA DINACEA)

1. **Portada**  
2. **Declaración metodológica (ISO 14040/14044)**  
   2.1 Meta y alcance  
   2.2 Inventario (LCI): flujos, puntos de medición y datos  
   2.3 Evaluación de impactos (LCIA)  
   2.4 Interpretación y mejora continua (PDCA)  
   2.5 Integración con EsIA y control documental  
3. **Justificación del español internacional neutro**  
4. **Titular, responsables y datos del sitio (ZIP)**  
   4.1 Identificación del titular y contactos  
   4.2 Responsables técnicos y matrículas  
   4.3 Parámetros del predio y coordenadas (desde ZIP)  
5. **Marco legal y normativo (Uruguay + normas internas)**  
   5.1 Autoridades y licenciamiento (EsIA + Clasificación A)  
   5.2 RSS: tratamiento/transporte y exclusiones  
   5.3 Vertidos y efluentes (templado <40 °C)  
   5.4 Ruido ambiental (metas día/noche)  
   5.5 Recipientes a presión (NR-13 como referencia)  
   5.6 Matriz requisito → evidencia → KPI  
6. **Contexto territorial y compatibilidad de usos**  
   6.1 AID/AII y zonificación IM  
   6.2 Receptores sensibles y accesos  
7. **Descripción del proceso y límites del sistema (ISO 14040)**  
   7.1 Flujo por lotes y PFD ASCII  
   7.2 Límites dentro/fuera y criterios de rechazo  
8. **Capacidad operativa y escalabilidad**  
9. **Memoria de cálculo: capacidad, vapor, agua y electricidad**  
10. **Servicios auxiliares y manejo de vapor/condensado**  
11. **HVAC, aire interior y control de olores**  
12. **Ruido y vibraciones (diseño + PMSA)**  
13. **Logística de residuos y seguridad de descarga**  
14. **SST (ISO 45001), PGR, HAZOP/What-If y emergencias**  
15. **Trazabilidad y control documental (Odoo rss_trace)**  
16. **Plan de Monitoreo y Seguimiento Ambiental (PMSA)**  
17. **Matriz de cumplimiento y compromisos**  
18. **Cronograma, FAT/SAT, entregables y plan de cierre**  
19. **Relacionamiento comunitario y apertura de datos**  
20. **Anexos, planimetría y control de versiones**  
21. **Resumen ejecutivo (para autoridades)**

> **Nota de auditoría (índice y consistencia):** Bloquear numeración de secciones en el **control de cambios**. Toda modificación de alcance o parámetros debe reflejarse en **Cap. 2**, **Cap. 5–11** y en la **Matriz de Cumplimiento** (Cap. 17).

---
# 2. Titular, responsables y datos del sitio (extraídos del ZIP de arquitectura)

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Fuente base:** `/Proyecto Arquitectura Polticor Oncativo 031025/Presentacion PTRH 0609.pdf` (ZIP de arquitectura).

---

## 2.1 Identificación del titular y contactos

**Titular del proyecto**  
**Polticor S.A.** — **RUT 214860570013**  
**Contacto institucional:** info@polticor.com | Colman 4590 – San Salvador 1478, CP 11800, Montevideo, Uruguay | Tel. 0800 1444* | https://polticor.com/

**Objeto del proyecto**  
Instalación y operación de **planta de tratamiento de residuos hospitalarios (RSS)** mediante **autoclave por vapor + trituración**, con **3 líneas** iniciales (escalable a **5–7**), **vapor 2×530 kgv/h (N+1)** y **EsIA adjunto** para **Clasificación Ambiental A (DINACEA)**.

> **Nota de auditoría — evidencia corporativa**  
> Adjuntar: estatuto/contrato social vigente, certificado único de RUT, poder de representación y certificados de domicilio. Codificar como `ANX-RL-POLTICOR-01..04`.

---

## 2.2 Responsables técnicos (designaciones y matrículas)

> Completar con los profesionales firmantes en Uruguay. Incluir **matrículas/colegiaturas**, **ámbito de actuación** y **cartas de designación**.

| Rol / Especialidad                                   | Nombre y título                           | Matrícula / Colegio | Firma | Vigencia | Código Anexo |
|---|---|---|---|---|---|
| Dirección de proyecto                                | `"[Nombre]"`                              | `"[Matr.]"`         | `"[ ]"` | `"[ ]"` | `ANX-RRHH-01` |
| Responsable ambiental (EsIA / DINACEA)               | `"[Nombre]"`                              | `"[Matr.]"`         | `"[ ]"` | `"[ ]"` | `ANX-RRHH-02` |
| Proceso (autoclave + trituración)                    | `"[Nombre]"`                              | `"[Matr.]"`         | `"[ ]"` | `"[ ]"` | `ANX-RRHH-03` |
| Vapor/condensado (“piano” y recipientes a presión)   | `"[Nombre]"`                              | `"[Matr.]"`         | `"[ ]"` | `"[ ]"` | `ANX-RRHH-04` |
| Civil/estructural                                    | `"[Nombre]"`                              | `"[Matr.]"`         | `"[ ]"` | `"[ ]"` | `ANX-RRHH-05` |
| Eléctrica y respaldo (UTE / grupos)                  | `"[Nombre]"`                              | `"[Matr.]"`         | `"[ ]"` | `"[ ]"` | `ANX-RRHH-06` |
| HVAC/Extracción/Acústica                             | `"[Nombre]"`                              | `"[Matr.]"`         | `"[ ]"` | `"[ ]"` | `ANX-RRHH-07` |
| SST (ISO 45001) y emergencias                        | `"[Nombre]"`                              | `"[Matr.]"`         | `"[ ]"` | `"[ ]"` | `ANX-RRHH-08` |
| Documentación y control de calidad (ISO 9001)        | `"[Nombre]"`                              | `"[Matr.]"`         | `"[ ]"` | `"[ ]"` | `ANX-RRHH-09` |

> **Nota de auditoría — designaciones**  
> Incorporar cartas de designación y alcances de responsabilidad firmados por el titular. Registrar control de versiones.

---

## 2.3 Ubicación y parámetros del predio (leídos del ZIP)

**Dirección y padrón**  
**Camino Oncativo 3154**, **Padrón 60790**, **Montevideo, Uruguay**.

**Superficie del predio (área total)**  
**13.748 m²** *(extraído de “Presentación PTRH 0609.pdf” — texto: “Área: 1 ha 3.748 m²”)*.

**Superficies construidas / naves**  
`"[SUP_NAVES_m²]"` *(no legible en los PDFs del ZIP; ver Nota de auditoría)*.

**Cuadro sintético**

| Parámetro                          | Valor                               | Fuente (ZIP)                           |
|---|---|---|
| Padrón                             | **60790**                           | Presentación PTRH 0609.pdf             |
| Dirección                          | **Camino Oncativo 3154**            | Presentación PTRH 0609.pdf             |
| Área total del predio              | **13.748 m²**                       | Presentación PTRH 0609.pdf             |
| Superficie construida / naves      | `"[SUP_NAVES_m²]"`                  | **Por confirmar** (ver planos de arquitectura) |
| Usos internos previstos            | Oficinas, vestuarios, comedor; **planta de tratamiento**; **tratamiento de efluentes**; depósito de acopio; estacionamientos | Presentación PTRH 0609.pdf |

> **Nota de auditoría — superficies de naves**  
> Realizar lectura de **cuadro de superficies** en planos de arquitectura (láminas de implantación/plantas). Si los PDFs son imagen/plot sin OCR, solicitar **planilla de cómputos** o **DWG** con cuadro de áreas. Cargar el dato como `ANX-PLN-SUP-01` y actualizar este capítulo.

---

## 2.4 Coordenadas y cartografía

**Coordenadas geográficas (WGS84)**  
**LAT:** `"[LAT]"` · **LON:** `"[LON]"` *(no informadas en los PDFs del ZIP; ubicar por certificado IM/IME o georreferenciación de plano)*.

**Cartografía y referencias**  
- Plano de **ubicación** y **layout general** incluidos en el ZIP (Presentación PTRH 0609.pdf).  
- Curvas de nivel 1 m: `Padron 60790 curvas 1 m-Curvas.pdf`.  
- Alineaciones y retiros: `alineaciones.pdf`.  
- Viabilidad y movilidad: `Viabilidad y Movilidad.pdf`.  
- Recorrido de camiones: `Recorrido de camiones.pdf`.

> **Nota de auditoría — georreferenciación**  
> Incorporar **croquis con coordenadas** y **sistema de referencia** (WGS84 / UTM-HPS) con tolerancia métrica. Adjuntar certificado de **uso del suelo** y **compatibilidad urbanística** (`ANX-URB-01`).

---

## 2.5 Compatibilidades internas del predio (síntesis del layout del ZIP)

- **Edificio 1:** vestuarios, comedor, oficinas.  
- **Planta de tratamiento:** área de proceso (autoclaves + trituración) con servicios asociados (piano de vapor, HVAC/extracción).  
- **Tratamiento de efluentes:** sistema interno con **templado < 40 °C** y **punto de muestreo** previo a descarga a **colector municipal**.  
- **Depósito de acopio:** post-tratamiento y acondicionamiento.  
- **Estacionamientos** y **recorridos de camiones** (circuito interno, radios de giro, señalización).

> **Nota de auditoría — coherencia de layout**  
> Verificar que el **layout del ZIP** se corresponda con las **capacidades declaradas** (Cap. 6 y 9) y con las **medidas de control** (Cap. 10–12). Incorporar **planos a escala** con **cuadro de superficies** y **simbología**.

---

## 2.6 Requisitos de completitud y control de versiones

1. **Superficie de naves (`SUP_NAVES_m²`):** cargar desde cuadro de áreas de arquitectura (PDF/DWG) → actualizar tabla 2.3.  
2. **Coordenadas (LAT/LON):** insertar desde certificado IM/IME o georreferenciación SIG.  
3. **Cartas de designación y matrículas:** anexar y referenciar en tabla 2.2.  
4. **Vinculación con capítulos posteriores:**  
   - Cap. 4 (**Parámetros del proyecto**), Cap. 7 (**Contexto territorial**), Cap. 11–12 (**HVAC / Ruido**), Cap. 15 (**PMSA**).

> **Nota de auditoría — trazabilidad**  
> Mantener **matriz de cambios** (quién, qué, cuándo, por qué) en control de versiones. Código de documento recomendado: `POL-PTRH-ESIA-02-UBI-V1.0`.

---

### Índice de la sección

- **2.1 Identificación del titular y contactos**  
- **2.2 Responsables técnicos (designaciones y matrículas)**  
- **2.3 Ubicación y parámetros del predio (ZIP)**  
- **2.4 Coordenadas y cartografía**  
- **2.5 Compatibilidades internas del predio (síntesis del layout)**  
- **2.6 Requisitos de completitud y control de versiones**


# 3. Marco legal y normativo aplicable (Uruguay + normas internas)

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Alcance:** Este capítulo compila el **marco regulatorio mínimo** para el proyecto y define la **ruta de licenciamiento**. Las citas legales se **verificarán** en la versión final del EsIA.  
> **Anexos IMPO sugeridos:** `ANX-LEG-01` (Dec. 643/1992), `ANX-LEG-02` (Dec. 253/1979), `ANX-LEG-03` (Dec. 222/1982), `ANX-LEG-XX` (otros complementarios).

---

## 3.1 Autoridades y ruta de licenciamiento

**Autoridad ambiental competente (nacional):** **DINACEA**, Ministerio de Ambiente (Uruguay).  
**Instrumento requerido:** **Estudio de Impacto Ambiental (EsIA)** y solicitud de **Clasificación Ambiental A** para la implantación y operación de planta de tratamiento de **residuos de servicios de salud (RSS)** por **autoclave + trituración**.

**Otras autoridades y coordinaciones:**
- **Intendencia de Montevideo (IM):** uso del suelo, habilitaciones y requisitos municipales (ruido, accesos, obras, seguridad de edificaciones).  
- **OSE:** condiciones de **vertido a colector** (cumplimiento del **Dec. 253/1979** y/o normativa vigente) y **puntos de muestreo**.  
- **UTE:** disponibilidad y **conexión eléctrica** (potencia a confirmar).  
- **MSP / Sanidad:** lineamientos para **gestión sanitaria** de RSS y transportistas habilitados (manifiestos, recipientes, cadena de custodia).

**Ruta regulatoria (resumen):**
1. **Ingreso EsIA** a DINACEA (incluye: descripción del proyecto, marco legal, línea base, matrices de impacto, medidas y **PMSA**).  
2. **Intercambios técnicos** y **clausulado** (condiciones y compromisos).  
3. **Clasificación Ambiental A** (si procede) y obtención de **permisos municipales** (IM) y **técnicos** (OSE/UTE/MSP).  
4. **FAT/SAT** y **puesta en marcha** bajo condiciones establecidas; **monitoreos** y reportes periódicos.

> **Nota de auditoría — coordinación interinstitucional**  
> Mantener un **cronograma de hitos** y **responsables** por trámite. Registrar oficios y respuestas en `ANX-LEG-TRAM-XX`.

---

## 3.2 Normativa base **expresamente citada**

1) **Decreto 643/1992** (IMPO 643-1992) — *Gestión de residuos (alcance urbano / sanitario según aplicación).*  
   - Usado como **marco general** para clasificación, manejo y responsabilidades en residuos, complementando los requisitos sanitarios/municipales aplicables a **RSS**.  
   - **Evidencias asociadas:** SOP de recepción, almacenamiento temporal, acondicionamiento y expedición; manifiestos y registros (Cap. 12 y 14).

2) **Decreto 253/1979** — *Vertidos a colector / curso receptor (límites y condiciones).*  
   - Define **parámetros** y **condiciones de vertido**. El proyecto descarga a **colector municipal**, **tras sistema interno** y con **templado < 40 °C**.  
   - **Evidencias:** punto de muestreo, plan de monitoreo (PMSA), registros de **T, pH, SST, DQO, aceites y grasas**, frecuencia y reporte (Cap. 7 y 15).

3) **Decreto 222/1982** — *Complementario/ambiental según alcance.*  
   - Se incorpora como **marco complementario** para obligaciones y procedimientos ambientales vinculados al proyecto (aplicación específica a confirmar en legal).  
   - **Evidencias:** matriz legal y trazabilidad documental (Cap. 16).

> **Nota de auditoría — verificación legal**  
> Identificar **artículos exactos** aplicables y **criterios de cumplimiento** en la **Matriz requisito→evidencia** (Sección 3.6). Adjuntar PDFs IMPO en `ANX-LEG-01..03`.

**Normativa complementaria (para robustecer aceptabilidad y ESG):**  
- **Ruido:** **Decreto 143/2012** y actualizaciones (**Decreto 281/016**), **Ley 17.852/2004** (*convivencia / ruidos molestos*).  
- **Recipientes a presión / vapor:** **NR-13 (Brasil)** como **referencia técnica** (prontuario, pruebas y certificaciones), con **equivalencias** a **ASME/EN** y **adecuación a exigencias locales**.  
- **Esterilización:** **ISO 17665-1** y **EN 285** (grandes esterilizadores a vapor).  
- **Sistemas de gestión:** **ISO 9001, 14001, 45001, 50001, 19011, 27001, 31000**.

> **Nota de auditoría — criterio de equivalencia técnica**  
> Cuando corresponda, demostrar **concordancia** entre NR-13 y los requisitos locales / internacionales (ASME/EN) mediante **prontuario**, **certificados de válvulas/sensores** y **ensayos** (Cap. 10 y 17). Se utilizará siempre que posible NR-13 visto que es unta regla reconocida en el MercoSur.

---

## 3.3 RSS: tratamiento por autoclave, transporte y exclusiones

**Ámbito del proyecto:** tratamiento **térmico por vapor (autoclave)** **sin pre-triturado**; trituración **posterior** a la verificación de esterilización (BI/IC) y condiciones de seguridad (Cap. 5).  
**Transporte:** únicamente **transportistas habilitados**; **manifiesto** de carga con identificación **QR** por lote; **pesaje** de ingreso/egreso; **balance de masa** mensual (<1 % tolerancia recomendada).  
**Exclusiones:** residuos **radioactivos**, **farmacéuticos** no compatibles, presurizados, **metales pesados** y otros **no conformes**; procedimiento de **rechazo** y **devolución** documentado.

**Evidencias requeridas:**  
- SOP de recepción/clasificación; formación de operadores; registros **Odoo** (hash/QR); **BI/IC** por receta; curva **T/P** por ciclo; trazabilidad por lote (Cap. 14).

> **Nota de auditoría — cadena de custodia**  
> Asegurar **íntegridad** de registros (ISMS/ISO 27001), **retención ≥5 años** y **prueba mensual de restauración** de backups.

---

## 3.4 Vertidos: descarga a colector tras sistema interno (**T < 40 °C**)

**Configuración declarada:** sistema interno de **gestión de condensado** con **intercambiador** para **templado < 40 °C**, **punto de muestreo** y **registro**; descarga final a **colector municipal**.  
**Obligaciones (Dec. 253/1979):** cumplir **parámetros** y condiciones de vertido definidos por OSE y normativa aplicable; notificar **incidentes** y ejecutar **acciones correctivas** (PMSA).

**Trazabilidad de muestreos (PMSA):**  
- **Parámetros mínimos:** **Temperatura**, **pH**, **SST**, **DQO**, **Aceites/Grasas**.  
- **Frecuencia base:** **Mensual** (quincenal en categorías de **alto riesgo**), con **cadena de custodia** y **laboratorio acreditable**.  
- **Evidencias:** planillas firmadas, PDFs con hash/QR (Cap. 15).

> **Meta operativa:** **T de vertido < 40 °C** en continuo, con **alarma** y **parada de seguridad** ante desvíos; reporte a autoridad cuando aplique.

---

## 3.5 Ruido: metas y cumplimiento municipal

**Metas de diseño (placeholders):**  
- **`[META_DÍA_dB]`** (línea de propiedad, horario diurno)  
- **`[META_NOCHE_dB]`** (línea de propiedad, horario nocturno)

**Criterios de control:**  
- **Diseño** con **barreras perimetrales**, **encapsulados** de fuentes (triturador, casa de máquinas) y **gestión horaria** de camiones (≤10 km/h; sin ralentí).  
- **Monitoreo** conforme a metodologías **reconocidas** (p. ej. ISO 1996/9613-2; equipos IEC 61672).  
- **Acciones correctivas** en PMSA: refuerzo de encapsulados, apantallamiento, reasignación horaria.

> **Nota de auditoría — ajuste de metas**  
> Reemplazar placeholders por valores **IM** de la zona y adjuntar la **línea base** (Cap. 12 y 15).

---

## 3.6 Recipientes a presión / calderas: NR-13 como referencia técnica

**Lineamientos técnicos:**  
- **Prontuario** del vaso de presión; **cálculos**, **materiales**, **soldaduras**, **ensayos**, **válvulas de seguridad** y **dispositivos** con **certificados** trazables (NR-13 o si necesario AMSE/EN o equivalentes).  
- **Inspecciones** y **mantenimiento** conforme a programa preventivo; **calibraciones** con certificados.  
- **FAT/SAT**: verificación de **enclavamientos**, **curvas T/P**, válvulas y presostatos; emisión de documentación de conformidad.

> **Nota de auditoría — equivalencias**  
> Documentar la **equivalencia** NR-13 ↔ **normas exigidas localmente** y **estándares internacionales**, adjuntando **certificados** (Cap. 10 y 17).

---

## 3.7 Matriz **requisito → evidencia** (extracto)

| Área | Norma / Requisito | Evidencia solicitada | Sección / Anexo | Periodicidad / Hito |
|---|---|---|---|---|
| EsIA / Clasificación | **DINACEA** (EsIA + Clasificación A) | Documento EsIA, matrices de impacto, PMSA, compromisos | Caps. 3, 7, 15, 16 · `ANX-ESIA` | Ingreso / Respuestas |
| RSS | **Dec. 643/1992** | SOP recepción/almacenamiento/expedición; manifiestos; trazabilidad QR | Caps. 5, 12, 14 · `ANX-SOP-RSS` | Operación continua |
| Vertidos | **Dec. 253/1979** | Punto de muestreo; registros T, pH, SST, DQO, O&G; T<40 °C | Caps. 7, 9, 15 · `ANX-PMSA-EFL` | Mensual / Quincenal |
| Ruido | **Dec. 143/2012 / 281/016** | Línea base; metas día/noche; monitoreo perimetral | Caps. 11, 12, 15 · `ANX-RUIDO` | Trimestral / Según IM |
| Presión | **NR-13** (ref.) + ASME/EN | Prontuario; certificados válvulas/sensores; FAT/SAT | Caps. 10, 17 · `ANX-NR13` | Antes de SAT / Anual |
| Esterilización | **ISO 17665-1 / EN 285** | Curvas T/P por ciclo; BI/IC; recetas y criterios | Caps. 5, 9, 14 · `ANX-QUAL-EST` | Cada lote / Receta |
| Sistemas gestión | **ISO 9001/14001/45001/50001/27001/19011/31000** | Manuales, procedimientos, auditorías, backups y restauraciones | Caps. 14–16 · `ANX-ISMS`, `ANX-QMS` | Según programa |

> **Nota de auditoría — trazabilidad legal**  
> En cada **evidencia**, insertar **cita IMPO** (nº decreto/artículo) y **código documental** (versión/fecha).

---

## 3.8 Gantt regulatorio (texto, 180 días — referencia)

- **Día 0–15:** Compilación EsIA (capítulos, matrices, PMSA, anexos legales y planos).  
- **Día 16:** **Ingreso EsIA** a DINACEA.  
- **Día 17–60:** Rondas de **aclaraciones** / complementos; **ajustes** de compromisos.  
- **Día 61–90:** **Clasificación Ambiental A** (si procede) y clausulado.  
- **Día 91–120:** Trámites **IM** (habilitaciones / obras), **OSE** (descarga a colector), **UTE** (potencia).  
- **Día 121–165:** Montaje, **FAT/SAT**, validaciones (BI/IC, **T<40 °C**, ruido en operación).  
- **Día 166–180:** Inicio de operación y **PMSA** operativo (reportes y publicación resumida).

> **Camino crítico:** respuestas DINACEA, condiciones de OSE para vertidos y **potencia UTE**. Mantener **matriz de dependencias** y **riesgos**.

---

## 3.9 Consideraciones finales y control de versiones

- Este marco se **actualizará** ante cambios normativos o condiciones del **clausulado**.  
- Toda **norma citada** se adjunta en **PDF IMPO** con **control de versiones** y **firma** del responsable legal/técnico.

> **Checklist de cierre (capítulo 3):**  
> ☐ Copias IMPO en anexos (`ANX-LEG-01..03`) · ☐ Tabla requisito→evidencia completa · ☐ Gantt regulatorio validado · ☐ Metas de **ruido** actualizadas (IM) · ☐ Procedimientos de **vertidos** y **muestreos** aprobados.

---
# 4. Contexto territorial y compatibilidad de usos

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Fuente base:** Dirección **Camino Oncativo 3154**, **Padrón 60790**, **Montevideo, Uruguay**.  
> **Anexos asociados:** `ANX-PLN-IMPL` (implantación), `ANX-PLN-UBIC` (ubicación), `ANX-PLN-RECEPTORES` (receptores), `ANX-PLN-PERFILES` (perfiles viales).  
> **Nota:** Donde falten datos del ZIP/dossier, se dejan **placeholders** a completar en la carga del EsIA.

---

## Índice de la sección
- **4.1 Área de influencia (AID/AII) y entorno inmediato**  
- **4.2 Zonificación IM (`[ZONIFICACIÓN_IM]`) y compatibilidad de uso**  
- **4.3 Receptores sensibles y distancias**  
- **4.4 Accesos viales y circulación interna (≤10 km/h, slots 15 min, ≤30 min)**  
- **4.5 Infraestructura y servicios del entorno (UTE/OSE/telecom)**  
- **4.6 Condicionantes físicos/ambientales externos**  
- **4.7 Notas de auditoría, planos y croquis requeridos**

---

## 4.1 Área de influencia (AID/AII) y entorno inmediato

**Ubicación del proyecto**  
- **Sitio:** **Camino Oncativo 3154, Padrón 60790**, Montevideo, Uruguay.  
- **Coordenadas WGS84:** **Lat** `"[LAT]"` · **Lon** `"[LON]"` *(a confirmar por certificado IM/IME o georreferenciación de plano)*.

**Definiciones operativas**  
- **Área de influencia directa (AID):** Predio del Padrón 60790 y frentistas inmediatos.  
- **Área de influencia indirecta (AII):** Radio urbano de `"[RADIO_AII_km]"` km para evaluación de **ruido**, **tránsito** y **compatibilidad** con usos residenciales/servicios.  
- **Entorno inmediato (síntesis por cuadrantes; completar con plano):**  
  - **Norte:** `"[Uso/Referencia_N]"` — retiro `"[DIST_N_m]"`.  
  - **Sur:** `"[Uso/Referencia_S]"` — retiro `"[DIST_S_m]"`.  
  - **Este:** `"[Uso/Referencia_E]"` — retiro `"[DIST_E_m]"`.  
  - **Oeste:** `"[Uso/Referencia_O]"` — retiro `"[DIST_O_m]"`.

> **Nota de auditoría — AID/AII**  
> Trazar **AID** y **AII** en `ANX-PLN-UBIC`, con escala y fuente cartográfica; referenciar datum (WGS84 / UTM-HPS).

---

## 4.2 Zonificación IM (`[ZONIFICACIÓN_IM]`) y compatibilidad de uso

**Zonificación municipal (IM):** `"[ZONIFICACIÓN_IM]"` *(código y descripción a confirmar con Certificado de Uso del Suelo)*.  
**Actividad declarada:** **Tratamiento de residuos de servicios de salud (RSS)** mediante **autoclave por vapor + trituración** (**sin pre-triturado**).  
**Compatibilidad:** La actividad se considera **compatible/condicionada** con `"[ZONIFICACIÓN_IM]"` bajo cumplimiento de:  
- **Metas de ruido** en **línea de propiedad** `"[META_DÍA_dB]"` / `"[META_NOCHE_dB]"` (ver Cap. 11 y PMSA Cap. 15).  
- **Gestión de efluentes** con **templado < 40 °C** y parámetros del **Dec. 253/1979** (ver Cap. 7 y 15).  
- **Tránsito pesado** con **circuito interno unidireccional**, control de velocidad y **ventanas horarias** (Cap. 12).

**Parámetros urbanísticos (si aplican):** FOS `"[FOS_%]"`; FOT `"[FOT]"`; altura `"[ALT_m]"`; retiros `"[RET_frentes_m]"` — *(a confirmar con IM)*.

> **Nota de auditoría — compatibilidad IM**  
> Adjuntar **Certificado de Uso del Suelo** y **condicionantes** en `ANX-URB-01`. Si la IM exige Estudio de Impacto de Tránsito (EIT), referenciarlo en `ANX-TRNS-01`.

---

## 4.3 Receptores sensibles y distancias

**Criterio:** Identificar receptores **residenciales**, **educativos**, **sanitarios** y **otros** en el entorno de la AID/AII, estimando **distancias** desde el **lindero** del predio.

| Receptor / Referencia | Tipo | Distancia a lindero (m) | Dirección / Rumbo | Observación |
|---|---|---:|---|---|
| `"[ESCUELA_x]"` | Educativo | `"[DIST_ESC_m]"` | `"[Rumbo]"` | Línea base de **ruido** requerida |
| `"[VIVIENDA_x]"` | Residencial | `"[DIST_VIV_m]"` | `"[Rumbo]"` | Receptor sensible (día/noche) |
| `"[CAPS_SALUD_x]"` | Salud | `"[DIST_SAL_m]"` | `"[Rumbo]"` | Receptor sensible (bioaerosoles/olores) |
| `"[OTRO_x]"` | — | `"[DIST_OTR_m]"` | `"[Rumbo]"` | — |

**Criterios de diseño asociados:**  
- **Ruido en línea de propiedad:** `"[META_DÍA_dB]"` / `"[META_NOCHE_dB]"` (Cap. 11).  
- **HVAC / bioaerosoles:** Salas “sucias” en **depresión** (Cap. 10); control de **olores** en descarga/trituración.  
- **Tránsito:** Secuenciación **slots 15 min** y permanencia **≤30 min** (Cap. 12).

> **Nota de auditoría — medición de distancias**  
> Determinar distancias en CAD/SIG con **error <±2 m**. Incluir croquis y listado de receptores con **fecha de relevamiento** en `ANX-PLN-RECEPTORES`.

---

## 4.4 Accesos viales y circulación interna (≤10 km/h, *slots* 15 min, ≤30 min)

**Vías de acceso principales (placeholders):**  
- **Primarias:** `"[VIA_PRINC_1]"`, `"[VIA_PRINC_2]"`  
- **Alternativas / desvíos:** `"[VIA_ALT_1]"`

**Parámetros de operación logística:**  
- **Velocidad interna:** **≤ 10 km/h** (señalización vertical y horizontal).  
- **Gestión de ingresos:** **time-slots de 15 min** por **agenda**; tope de simultaneidad `"[N_cam_en_playa]"` camiones.  
- **Permanencia máxima en playa:** **≤ 30 min** por unidad.  
- **Báscula** de **ingreso/egreso** integrada a trazabilidad **QR** (balance de masa).  
- **Cabina de descarga** con **captación localizada** (ver Cap. 12).  
- **Circuito interno:** **unidireccional**, radios de giro `"[R_giro_m]"`, anchos `"[ANCHO_via_m]"`.

**Tabla — dimensionamiento (placeholders):**

| Elemento | Requisito | Valor de diseño |
|---|---|---|
| Radio de giro interno | Camión tipo `"[TIPO_CAM]"` | `"[R_giro_m]"` |
| Ancho de vía interna | Unidireccional | `"[ANCHO_via_m]"` |
| Área de espera | ≥ `"[N_cam]"` camiones | `"[SUP_espera_m2]"` |
| Señalización | Velocidad / Prioridades | Conforme IM |

> **Nota de auditoría — seguridad vial interna**  
> Adjuntar **perfiles viales** y radios de giro (`ANX-PLN-PERFILES`). Incluir **plan de señalética** y **puntos de cruce peatonal**.

---

## 4.5 Infraestructura y servicios del entorno (UTE/OSE/telecom)

**Electricidad (UTE):**  
- **Potencia contratada / en trámite:** `"[POTENCIA_EN_TRÁMITE_UTE]"` *(pendiente de confirmación)*.  
- **Respaldo:** grupos electrógenos para **1 caldera + servicios esenciales** (ver Cap. 9–10).

**Agua y saneamiento (OSE):**  
- Abastecimiento desde red OSE; **tratamiento de alimentación** (ablandamiento/RO, si conviene a **vida útil**).  
- **Efluente**: sistema interno de **condensado** con **intercambiador** para **templado < 40 °C** y **punto de muestreo**; descarga a **colector municipal** (Dec. **253/1979**).  
- **Frecuencia de muestreo:** **mensual** (quincenal alto riesgo) — ver **PMSA** (Cap. 15).

**Telecom / datos:**  
- Conectividad para **Odoo on-premise** (**rss_trace**); **backups** diarios incrementales + **semanal off-site**; **prueba de restauración mensual** (Cap. 14).

**Drenajes pluviales:**  
- **Segregación** de pluviales respecto a efluentes; pendientes dirigidas; **sin** mezcla con condensado/descargas de proceso.

> **Nota de auditoría — servidumbres**  
> Incorporar planos de **conexiones** (eléctrica, agua, saneamiento, telecom) con **coordenadas** y **cotas**. Referenciar permisos/expedientes `ANX-UTE`, `ANX-OSE`.

---

## 4.6 Condicionantes físicos/ambientales externos

- **Topografía y escurrimiento:** Confirmar pendientes y **no anegabilidad** del sector (curvas de nivel en `ANX-PLN-UBIC`).  
- **Vientos dominantes:** Registrar **rosas de viento** para orientar **captaciones/descargas** (informe de base atmosférica en EsIA).  
- **Riesgo hídrico:** Verificar distancias a cursos/canales y **cotas** de seguridad.  
- **Entorno nocturno:** Definir **iluminación apantallada** para minimizar derrame lumínico hacia receptores sensibles.

> **Nota de auditoría — base ambiental**  
> Integrar en el EsIA la **línea base** de **ruido** (día/noche), **calidad de aire interior** y **efluentes**, alineando metas de diseño (Cap. 11 y 15).

---

## 4.7 Notas de auditoría, planos y croquis requeridos

- **Planos/croquis obligatorios:**  
  - `ANX-PLN-IMPL` (implantación, gálibos, accesos).  
  - `ANX-PLN-UBIC` (ubicación, AID/AII, coordenadas).  
  - `ANX-PLN-RECEPTORES` (mapa de receptores y distancias).  
  - `ANX-PLN-PERFILES` (perfiles viales, radios de giro, señalética).  
- **Pendientes a completar (placeholders):**  
  - `"[ZONIFICACIÓN_IM]"`, `"[LAT]"`, `"[LON]"`, `"[RADIO_AII_km]"`.  
  - `"[META_DÍA_dB]"`, `"[META_NOCHE_dB]"` (ver Cap. 11).  
  - Vías `"[VIA_PRINC_1]"`, `"[VIA_PRINC_2]"`, `"[VIA_ALT_1]"`; radios `"[R_giro_m]"`, anchos `"[ANCHO_via_m]"`.  
- **Control de versiones:** Registrar **quién/qué/cuándo/por qué** al actualizar cualquier plano o dato sensible.

> **Checklist de cierre (Cap. 4):**  
> ☐ Certificado de **uso del suelo IM** en `ANX-URB-01` · ☐ Receptores y distancias validadas · ☐ Accesos y logística interna definidos · ☐ Conexiones UTE/OSE nominales y en trámite · ☐ Placeholders sustituidos.

---
# 5. Descripción del proceso y límites del sistema (ISO 14040)

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Normas guía:** ISO 14040/14044 (meta/alcance, LCI/LCIA), ISO 17665-1 / EN 285 (esterilización por vapor), ISO 9001/14001/45001/50001, ISO 27001/19011/31000.  
> **Supuesto clave:** **sin pre-triturado**. Secuencia **autoclave → trituración**. **Portal gamma** en ingreso. **Báscula** en **ingreso** y **egreso**.

---

## 5.1 Flujo por lotes y organización del proceso

**Unidad operativa:** **Lote/ciclo** de RSS (bolsas/contenedores cerrados) identificado por **QR** y guía de transporte.  
**Líneas de proceso:** **L1–L3** (escalables a **5–7**). **Desfase de 15 min** entre líneas para aplanar picos.  
**Servicios auxiliares:** **Piano de vapor** (2×530 kgv/h, N+1), **agua** (ablandamiento/RO si conviene), **electricidad** (UTE + grupos), **aire comprimido**, **HVAC/extracción** (salas “sucias” en depresión), **gestión de condensado** con **templado < 40 °C** y **punto de muestreo**.

**Resumen por etapas (lote típico):**
1) **Ingreso y control** → **Portal gamma** → **Báscula ingreso** → verificación documental.  
2) **Recepción y clasificación** → Identificación **QR** → inspección visual → decisión de **aceptación/rechazo**.  
3) **Sala sucia (ΔP<0)** → **Carga** en **autoclave** (L1/L2/L3).  
4) **Ciclo de esterilización** → registro **T/P vs. tiempo**; **BI/IC** según receta.  
5) **Descarga** → **Trituración pos-esterilización** → **Acondicionamiento** para expedición.  
6) **Báscula egreso** → **Expedición** a operador de disposición final autorizado.  
7) **Gestión de condensado** → intercambiador → **T<40 °C** → **punto de muestreo** → colector.

> **Nota de auditoría — roles y segregación**  
> Definir **roles** (Operador/ Supervisor/ Mantenimiento/ HSE/ Auditor) y su **firma** en cada hito del lote (Odoo **rss_trace**). Ver Cap. 14.

---

## 5.2 Diagrama de flujo de proceso (PFD ASCII)

flowchart TD
  EXT["EXTERIOR / ACCESO AL PREDIO"]
  EXT --> PORTAL["PORTAL GAMMA (RAD-01) - Alarma/Rechazo si radiación > umbral"]
  PORTAL --> BAS_IN["BÁSCULA INGRESO (BAS-01) - Registro peso_in + QR"]
  BAS_IN --> REC["RECEPCIÓN & CLASIFICACIÓN (REC-01) - Identificación por QR"]

  REC -->|"Aceptación"| SUCIA["SALA 'SUCIA' - ΔP negativa: objetivo -15 Pa - Captación localizada + pre-sellos"]

  SUCIA --> AUT1["AUTOCLAVE L1 (AUT-01)"]
  SUCIA --> AUT2["AUTOCLAVE L2 (AUT-02)"]
  SUCIA --> AUT3["AUTOCLAVE L3 (AUT-03)"]

  AUT1 -->|"Ciclo T/P + BI/IC"| DESC1["DESCARGA EST."]
  AUT2 -->|"Ciclo T/P + BI/IC"| DESC2["DESCARGA EST."]
  AUT3 -->|"Ciclo T/P + BI/IC"| DESC3["DESCARGA EST."]

  DESC1 --> TRIT["TRITURACIÓN POS-EST. (TR-01)"]
  DESC2 --> TRIT
  DESC3 --> TRIT

  TRIT --> ACD["ACONDICIONAMIENTO (ACD-01)"]
  ACD --> BAS_OUT["BÁSCULA EGRESO (BAS-02)"]
  BAS_OUT --> EXP["EXPEDICIÓN (EXP-01)"]

  subgraph SVA["SERVICIOS AUXILIARES (SVA)"]
    SVA1["Piano de vapor (2×530 kgv/h, N+1): PRV, separador, purgadores, válvulas seg."]
    SVA2["Gestión de condensado: tanque -> intercambiador placas (ICX-01) -> T < 40 °C -> PME-01 -> colector"]
    SVA3["Aire comprimido (AIR-01), agua tratada (RO-01/ABL-01), energía (TAB-01)"]
    SVA4["HVAC/extracción: ΔP y Q monitorizados; filtros MERV-13 / HEPA selectivo"]
  end

  classDef autoclave fill:#ffe6f2,stroke:#800040,stroke-width:1px;
  classDef service fill:#e6f7ff,stroke:#0077b3,stroke-width:1px;
  classDef process fill:#fff8e6,stroke:#b36b00,stroke-width:1px;

  class EXT,PORTAL,BAS_IN,REC,SUCIA,DESC1,DESC2,DESC3,TRIT,ACD,BAS_OUT,EXP process;
  class AUT1,AUT2,AUT3 autoclave;
  class SVA1,SVA2,SVA3,SVA4 service;



> **Nota de auditoría — planos y tags**  
> Vincular este PFD con **P&ID**, **isométricos** y **lista de equipos/instrumentos** (tags) en `ANX-PLN-PID` y `ANX-MTO`.

---

## 5.3 Límites del sistema (dentro / fuera)

**Dentro del sistema (evaluación y control):**  
- Actividades internas desde **acceso al predio** hasta **expedición** del material **esterilizado/triturado**.  
- Consumo de **vapor/agua/electricidad/aire**, **ruido** perimetral, **calidad de aire interior** y **efluente** (T<40 °C, parámetros).  
- **Datos y trazabilidad** (Odoo, CSV/PDF, hash, QR, retención ≥5 años, backups).

**Fuera del sistema (interfases documentadas):**  
- **Transporte** extra-predial (origen/hospitales y disposición final).  
- **Operador** de disposición final (contratos, manifiestos).  
- Marco **sanitario-municipal** del origen de los residuos.

> **Nota de auditoría — interfaces**  
> Incluir **matriz de límites** y **contratos** con transportistas/operadores (`ANX-CONTR-OP`), más instructivos de embalaje en origen.

---

## 5.4 Recetas de esterilización y criterios de aceptación (BI/IC)

**Ventanas de receta (orientativas; se ajustan en FAT/SAT):**
- **Temperatura de proceso:** **135–145 °C** (setpoint por tipo/densidad de carga).  
- **Plateau efectivo:** **15–30 min** (según porosidad/masa).  
- **Vacíos/pos-vacíos:** definidos por fabricante/validación.  
- **Objetivo microbiológico:** **STAATT IV** (reducción ≥**6 log10**), conforme **ISO 17665-1 / EN 285**.

**Aceptación automática del ciclo (criterios mínimos):**
- Curva **T/P** dentro de tolerancias de la receta (±**[ΔT] °C** / ±**[ΔP] bar**).  
- **BI** (indicador biológico) **negativo** y **IC** (indicador químico) conforme.  
- Sin **alarmas** críticas activas durante el plateau.  
- Registro completo (T/P vs. t, lote, operador, estado de puerta) **exportado** (CSV/PDF con **hash**).

**Bloqueo/No conformidad (NCR) del ciclo:**
- **BI positivo** o **IC no conforme** → **bloqueo** del lote y reproceso o disposición según SOP.  
- **Curva fuera de rango** o **sensores no calibrados** → **bloqueo** y **mantenimiento**.  
- **Apertura de puerta** no autorizada → **anulación** del ciclo.

> **Nota de auditoría — calibraciones**  
> Adjuntar certificados **trazables** (PT100, manovacuómetros, válvulas de seguridad) y plan de **calibración** (Cap. 17).

---

## 5.5 Matriz de aceptación / exclusiones y criterios de rechazo

| Categoría | Condición | Aceptación | Tratamiento / Ruta | Evidencia |
|---|---|---|---|---|
| **RSS comunes** (bolsas cerradas) | Integridad de embalaje; sin líquidos libres | **Sí** | Autoclave → Trituración → Acondic. | QR+Guía, fotos opc., registro Odoo |
| **Cortopunzantes** en contenedor rígido | Contenedor homologado, cerrado | **Sí** | Autoclave → Trituración encapsulada | Registro lote, BI/IC |
| **Anatómicos/Patológicos** | Según permiso específico | **No/Cond.** | **Excluidos** salvo autorización expresa | SOP de rechazo |
| **Fármacos/Citotóxicos** | Mezclados con RSS | **No** | **Rechazo** / derivación | Acta y trazabilidad |
| **Presurizados** (cilindros/aerosoles) | Riesgo explosión | **No** | **Rechazo** | Acta y comunicación |
| **Radioactivos** | Detección **Portal gamma** | **No** | **Rechazo inmediato** | Log de alarma, notificación |
| **Metales pesados** / químicos | Según SDS | **No** | **Rechazo** / derivación | Acta y manifiesto |
| **Líquidos libres** | Fuga visible | **No** | Rechazo/contención | Registro y limpieza |

**Criterios generales de rechazo:**  
- **Alarma** en portal gamma; **derrame** evidente; **mezcla incompatible**; **envase no conforme**; **documentación** ausente/incompleta.

> **Nota de auditoría — SOP de recepción**  
> Codificar SOPs: `SOP-RSS-REC`, `SOP-RSS-RECH`, `SOP-RSS-CARGA`. Adjuntar **formatos de acta** y **checklists** (Cap. 12 y 14).

---

## 5.6 Gestión de condensado y punto de muestreo

- **Generación:** Condensado de autoclaves y líneas de vapor.  
- **Tratamiento interno:** Tanque de recogida → **intercambiador de placas (ICX-01)** para **precalentar agua de alimentación** (**recuperación energética**) y simultáneo **templado a < 40 °C** antes del vertido.  
- **Control y muestreo:** **Punto PME-01** con **termómetro**, **válvula** y **punto de toma**; plan de muestreo **mensual** (quincenal si **alto riesgo**) para **T, pH, SST, DQO, O&G**.  
- **Descarga final:** **Colector municipal** (Dec. 253/1979).

> **Nota de auditoría — límites de vertido**  
> Insertar **valores límite** específicos en la **Matriz de Cumplimiento** (Cap. 16) cuando OSE confirme condiciones.

---

## 5.7 HVAC, bioaerosoles y control de olores (sala “sucia”)

- **Depresión:** objetivo **−15 Pa** (alarma **−10↔−20 Pa**).  
- **Captación localizada:** en descarga/recepción y trituración (ver Cap. 10).  
- **Filtración:** **MERV-13** general; **HEPA H13** en retornos críticos.  
- **Monitoreo:** **UFC/m³** periódicas; protocolo ante **episodios de olor**.

> **Nota de auditoría — evidencias de control**  
> Bitácoras de **ΔP/Q**, mantenimientos de filtros, y **acciones** ante desvíos (PMSA, Cap. 15).

---

## 5.8 Datos, trazabilidad y seguridad de la información

- **Sistema:** **Odoo on-premise** + módulo **rss_trace**.  
- **Registro por lote:** usuario/rol, receta, **T/P vs. tiempo**, **BI/IC**, estado de puerta, alarmas; **CSV/PDF** con **QR** y **hash SHA-256**.  
- **Retención:** **≥ 5 años**; **backup diario** incremental + **semanal off-site**; **prueba de restauración mensual**.  
- **Bloqueos:** BI positivo/IC no conforme; curva fuera de tolerancia.

> **Nota de auditoría — auditorías internas**  
> Plan anual de auditorías (ISO 19011) y **pruebas de restauración** documentadas (Cap. 14 y 17).

---

## 5.9 FAT / SAT y evidencias requeridas

**FAT (fábrica):**
- Prueba de **enclavamientos** y **seguridad** (válvula de alivio, presostatos, puertas).  
- Corrida de **vacío/calor** y **exportación** de datos (CSV/PDF).  
- **Certificados** de válvulas/sensores y **prontuario** (NR-13 como referencia técnica).

**SAT (sitio):**
- Validación de **curvas T/P** con **agua local** y **carga test**.  
- **BI/IC** por **3 tipos** de carga (porosidad/densidad).  
- Verificación de **T vertido < 40 °C** y toma de **muestra** en PME-01.  
- **Ruido** en operación (línea de propiedad) según Cap. 11.

**Entrega de evidencias (mínimo):**
- Protocolos firmados de **FAT/SAT**, **calibraciones**, **SOPs** aprobados, plan de **mantenimiento preventivo**, y **lista de repuestos críticos**.

> **Nota de auditoría — criterios de aceptación**  
> Documentar **umbrales cuantitativos** (p. ej., rechazo automático si BI positivo; alarma si T vertido ≥ 38 °C, paro si ≥ 40 °C). Vincular con **PMSA** (Cap. 15) y **Matriz de Cumplimiento** (Cap. 16).

---

## 5.10 Índice de la sección

- **5.1 Flujo por lotes y organización del proceso**  
- **5.2 Diagrama de flujo (PFD ASCII)**  
- **5.3 Límites del sistema (dentro/fuera)**  
- **5.4 Recetas y criterios de aceptación (BI/IC)**  
- **5.5 Matriz de aceptación/exclusiones y rechazo**  
- **5.6 Gestión de condensado y muestreo**  
- **5.7 HVAC, bioaerosoles y olores**  
- **5.8 Datos y trazabilidad (ISMS)**  
- **5.9 FAT/SAT y evidencias**  

> **Checklist de cierre (Cap. 5):**  
> ☐ PFD ↔ P&ID/Isométricos alineados · ☐ SOPs de recepción/carga/ciclo/descarga/trituración aprobados · ☐ Criterios FAT/SAT definidos · ☐ Punto de muestreo y alarmas implementados · ☐ Roles, firmas y backups operativos.

# 6. Capacidad operativa y escalabilidad

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Supuestos de cálculo:** Autoclave **165 kg/ciclo**, **45 min/ciclo**, operación **24/7**, **desfase 15 min** entre líneas, **sin pre-triturado**.  
> **OEE declarado:** **75 % (régimen normal)** y **100 % (extraordinario)**.  
> **Nota:** Se asume **mes de 30 días** para equivalencias t/mes. Ajustar si el clausulado fija otro calendario.

---

## 6.1 Productividad por línea y por configuración

**Cálculos base por línea**  
- Ciclos/día = \( \frac{24×60}{45} = 32 \)  
- t/día (100 %) = \( 32 × 0,165 = \mathbf{5{,}28\ t/d} \)  
- t/día (75 %) = \( 5{,}28 × 0{,}75 = \mathbf{3{,}96\ t/d} \)

**Capacidad agregada (3, 4, 5 y 7 líneas)**

| Líneas | Régimen | t/día | t/mes (30 d) | Observación |
|---:|:--|---:|---:|---|
| 3 | **Normal (OEE 75 %)** | **11,88** | **356,4** | Corresponde al objetivo **≈360 t/mes** (normal) |
| 3 | **Extraordinario (100 %)** | **15,84** | **475,2** | Corresponde al objetivo **≈475 t/mes** (extraordinario) |
| 4 | Normal (75 %) | 15,84 | 475,2 | Normal con margen; cubre picos transitorios sin “extraordinario” |
| 4 | Extraordinario (100 %) | 21,12 | 633,6 | Recomendado si la demanda mensual supera 500–600 t |
| 5 | Normal (75 %) | 19,80 | 594,0 | Efectivo ≈**20 t/d**; base para contratos >550 t/mes |
| 5 | Extraordinario (100 %) | 26,40 | 792,0 | Requiere verificación de **vapor** y **logística** |
| 7 | Normal (75 %) | 27,72 | 831,6 | Escala mayor; revisar **ruido**, **PMSA** y **UTE** |
| 7 | Extraordinario (100 %) | 36,96 | 1.108,8 | Solo viable con upgrade integral de **servicios** |

> **Nota de auditoría — redondeos:** Los resultados se presentan con dos decimales. Documentar en **Memoria de cálculo** (Cap. 9) las variaciones por mantenimientos, paradas y feriados.

---

## 6.2 Cobertura operativa y contingencias

- **3 líneas** · Normal 75 % → **356 t/mes**: **cumple** objetivo normal.  
  - **Contingencia con 1 línea fuera** (2 líneas, 75 %): **7,92 t/d** (~**238 t/mes**). Requiere **gestión de turnos** y **reprogramación de recolecciones** para evitar backlog.  
- **4 líneas** · Normal 75 % → **475 t/mes**: cubre **normal** + **picos** sin forzar 100 %.  
  - **Contingencia con 1 línea fuera** (3 líneas, 75 %): **11,88 t/d** (~**356 t/mes**): **sostiene** el objetivo normal aun en falla.  
- **5 líneas** · Normal 75 % → **594 t/mes**: base para contratos de mayor volumen con **tolerancia a fallas**.  
  - **Contingencia con 1 línea fuera** (4 líneas, 75 %): **15,84 t/d** (~**475 t/mes**): mantiene el **extraordinario**.

> **Criterio recomendado (escalabilidad):** Prever **infraestructura y servicios** (piano de vapor, tableros, HVAC, logística) **dimensionados a 5 líneas**, instalando 3 iniciales. La **cuarta** línea funciona como **colchón** operativo y de **mantenimiento**; la **quinta** habilita contratos >550 t/mes con **resiliencia**.

---

## 6.3 Triggers de expansión (objetivos y umbrales)

**Se propone activar proyecto de ampliación** (ingeniería + compra de equipo) cuando se verifique **cualquiera** de los siguientes criterios durante **3 meses consecutivos**:

1. **Utilización media ≥ 85 %** (OEE 75 %) en **3 líneas** **o** colas semanales > **10 %** del throughput.  
2. **Demanda contratada o proyectada ≥ 400 t/mes** por 3–6 meses (con “colas” > 48 h en picos).  
3. **No conformidades por logística** (rechazos por ventana/tiempo de permanencia >30 min) ≥ **2 %** de movimientos.  
4. **Mantenimiento preventivo** no ejecutable sin pérdida de metas (horas MTTR+MTBF no alcanzadas).  
5. **Riesgos operativos** (picos de vapor, dB perimetrales, T vertido) recurrentes pese a mitigaciones.

**Secuencia recomendada de expansión:**  
- **Fase 1 (Base):** 3 líneas + servicios dimensionados a 5.  
- **Fase 2 (Trigger):** Incorporar **L4** (capacidad efectiva ≈ **475 t/mes** a 75 %).  
- **Fase 3 (Crecimiento):** Incorporar **L5** (≈ **594 t/mes** a 75 %) con verificación de **UTE**, **vapor** y **HVAC**.  
- **Fase 4 (Máxima):** Preparar obras para **L6–L7** si la proyección >800 t/mes (requerirá ajuste integral PMSA).

---

## 6.4 KPIs operativos y criterios de aceptación

**Desempeño**  
- **OEE planta** (meta normal **≥ 75 %**; extraordinario **= 100 %** limitado en tiempo).  
- **Throughput**: t/d y t/mes por línea y total (desvío ≤ **±5 %** vs. plan semanal).  
- **Tiempo de ciclo** (media/percentiles) y **utilización** por línea.

**Calidad / Esterilización**  
- **BI negativo 100 %** de los lotes; **IC conforme 100 %**.  
- **Ciclos aprobados / totales** ≥ **99,0 %** (fallidos con reproceso controlado).

**Ambiental / Servicios**  
- **T de vertido < 40 °C**: **100 % del tiempo**, con alarma ≥ **38 °C**.  
- **Ruido**: cumplimiento metas **`[META_DÍA_dB] / [META_NOCHE_dB]`** en línea de propiedad.  
- **kWh/t**, **kgv/t**, **m³/t**: línea base y **mejora interanual ≥ 3 %** (ISO 50001).

**Logística**  
- **Permanencia en playa ≤ 30 min** (P90); **cumplimiento de slots** ≥ **95 %**.  
- **Rechazos por documentación/envase** ≤ **1 %** de lotes.

**Seguridad / Confiabilidad**  
- **Disponibilidad de líneas** ≥ **95 %** mensual.  
- **Eventos críticos (paradas >1 h por línea)** ≤ **2/mes**.

> **Criterios de aceptación (capacidad):** Se considera **cumplido** el objetivo **360 t/mes** cuando **t/mes efectivo ≥ 360 t** con **OEE ≥ 75 %**, **BI/IC 100 % conformes**, **T<40 °C 100 %**, y **ruido** dentro de metas.

---

## 6.5 Riesgos operativos y mitigaciones

| Riesgo | Efecto | Mitigación de diseño | Mitigación operativa |
|---|---|---|---|
| **Falla de autoclave** | Caída de capacidad | **Mín. 3 líneas** + preinstalación para **L4** | Programar mantenimiento en ventana; **re-balance** de lotes |
| **Falla de caldera / vapor** | Parada de ciclo | **2×530 kgv/h (N+1)**; separación por válvulas | Arranques escalonados; priorizar recetas críticas |
| **Picos de demanda** | Colas/logística | **Slots 15 min**, **cuarta línea** como buffer | Extensión temporal de turnos; refuerzo de transporte |
| **Saturación de trituración** | Cuello de botella | Triturador por línea; bypass de contingencia | Mantenimiento preventivo + piezas críticas en stock |
| **Exceso T vertido** | No conformidad ambiental | **Intercambiador** + control continuo | Alarmas a 38 °C; paro y recirculación hasta <40 °C |
| **Ruido perimetral** | Reclamos/compliance | **Barreras/encapsulados** desde diseño | Ventanas horarias; monitoreo y acción correctiva |
| **Cortes UTE** | Paradas y pérdida de ciclo | **Grupos** dimensionados para **1 caldera + esenciales** | Pruebas de **black-start** y plan de prioridad de cargas |
| **Datos incompletos** | Auditoría fallida | Odoo on-prem + **hash/QR**, backups | Prueba mensual de restauración; auditorías ISO 19011 |

> **Nota de auditoría — reservas y stock crítico:** Mantener **lista de repuestos** (válvulas, juntas, bomba de vacío, sensores) y **SLA** con proveedores. Vincular a Cap. 17 (FAT/SAT y entregables).

---

## 6.6 Índice de la sección

- **6.1 Productividad por línea y por configuración**  
- **6.2 Cobertura operativa y contingencias**  
- **6.3 Triggers de expansión**  
- **6.4 KPIs y criterios de aceptación**  
- **6.5 Riesgos y mitigaciones**

> **Checklist de cierre (Cap. 6):**  
> ☐ Tablas de capacidad validadas · ☐ Escenario de contingencia con 1 línea fuera documentado · ☐ Triggers de expansión aprobados · ☐ KPIs en Odoo configurados · ☐ Stock crítico y SLA definidos.

# 7. Aspectos ambientales (ISO 14001 / ISO 50001) y diseño de control

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Alcance:** Gestión de aspectos/impactos ambientales prioritarios del proyecto **Polticor S.A.** (autoclave + trituración) e integración con el **Sistema de Gestión Ambiental (ISO 14001)** y el **Sistema de Gestión de la Energía (ISO 50001)**.  
> **Supuestos clave del proyecto:** 3 líneas (**esc. 5–7**), vapor **2×530 kgv/h (N+1)**, **templado < 40 °C** previo a descarga a colector, operación **24/7** con **desfase 15 min** entre líneas, **sin pre-triturado**.  
> **Referencias cruzadas:** Cap. 5 (proceso y límites), Cap. 6 (capacidad), Cap. 9–10 (memorias y servicios), Cap. 11–12 (HVAC/ruido), Cap. 15 (PMSA), Cap. 16 (matriz de cumplimiento).

---

## 7.1 Matriz de aspectos e impactos (identificación y control)

> **Criterio de significancia:** Severidad (S) × Ocurrencia (O) × Detección (D). Umbral de significancia: **≥ 12**.  
> **Leyenda:** S (1–5), O (1–5), D (1–5; 1 = fácil de detectar). **Medidas**: Prev. (prevención), Mit. (mitigación), Mon. (monitoreo).

| Aspecto | Impacto Potencial | S | O | D | **Signif.** | Medidas de control (diseño/operación) | Registro / Evidencia |
|---|---|:-:|:-:|:-:|:-:|---|---|
| **Consumo de energía (vapor/calderas eléctricas)** | Aumento huella energética | 3 | 4 | 2 | **24** | Secuenciación de líneas (**desfase 15 min**), recuperación de calor del **condensado** para precalentar agua, FV oficinas, ajuste de recetas por densidad | kWh/t, curva de demanda, reportes ISO 50001 |
| **Picos de potencia eléctrica** | Penalidades / estrés de red | 3 | 3 | 2 | **18** | Arranques escalonados, lógica de carga resistiva/calderas, gestión de demanda | Perfil 15-min, alarmas SCADA, OEE |
| **Generación de condensado** | Vertido térmico / incumplimiento T | 4 | 3 | 2 | **24** | **Intercambiador** de placas, **templado < 40 °C**, punto de muestreo, alarma a 38 °C y paro ≥ 40 °C | Planillas T/pH/SST/DQO/O&G, PMSA |
| **Calidad de efluentes** | Exceder límites (Dec. 253/79) | 4 | 2 | 2 | **16** | Separación de pluviales, control pH/SST/DQO/O&G, mantenimiento trampas/purgadores | Resultados laboratorio, cadena de custodia |
| **Aire interior en sala “sucia”** | Bioaerosoles / olores | 4 | 3 | 2 | **24** | **ΔP −15 Pa** (alarma −10↔−20), captación localizada, **MERV-13** general + **HEPA H13** en puntos críticos, limpieza y SIP/CIP de tolva | ΔP/Q registro continuo, UFC/m³, SOP limpieza |
| **Ruido en línea de propiedad** | Molestias / reclamos | 3 | 3 | 2 | **18** | Barreras perimetrales, encapsulados (triturador, casa de máquinas), gestión horaria logística, ≤10 km/h | dB(A) perimetral, mapa de ruido, PMSA |
| **Residuos secundarios (filtros, BI/IC, mantenimiento)** | Manejo y disposición inadecuada | 2 | 3 | 2 | 12 | Segregación, contenedores homologados, gestores autorizados, registros | Manifiestos, Odoo rss_trace |
| **Derrames accidentales** | Suelo / saneamiento | 4 | 1 | 2 | 8 | Cubetos y kits de contención, SOP de emergencia, capacitación | Actas de incidente, PGR |
| **Iluminación exterior** | Derrame lumínico | 2 | 2 | 2 | 8 | Luminarias apantalladas, horarios | Checklist y fotometrías |

> **Nota de auditoría — revisión anual:** Actualizar puntuaciones S/O/D con base en **desempeño real** y auditoría interna (**ISO 19011**). Vincular acciones de mejora a **objetivos y metas** del **Programa Ambiental**.

---

## 7.2 Efluentes líquidos: **templado < 40 °C**, parámetros y frecuencias

**Configuración:** Condensado de autoclaves y líneas de vapor a tanque → **intercambiador de placas** (recuperación de calor + templado) → **punto de muestreo (PME-01)** → **colector municipal** (Dec. **253/1979**).

**Parámetros y frecuencias (PMSA, ver Cap. 15):**

| Parámetro | Meta / Límite | Frecuencia | Método / Norma | Acción ante desvío |
|---|---|---:|---|---|
| **Temperatura (T)** | **< 40 °C** (alarma 38 °C) | **Continuo** (sensor) + **mensual** (verificación) | Termometría trazable | Recirculación inmediata; paro si ≥ 40 °C; notificación |
| **pH** | 6,0–9,0 *(ajustar a OSE)* | **Mensual** | Son. calibrado / laboratorio | Investigación causa, ajuste y re-muestreo |
| **Sólidos en suspensión (SST)** | *Según Dec. 253/79 / OSE* | **Mensual** | Laboratorio | Mejora operación, limpieza trampas |
| **DQO** | *Según OSE* | **Mensual** | Laboratorio | Optimizar purgas/descargas y mantenimiento |
| **Aceites y grasas (O&G)** | *Según OSE* | **Mensual** | Laboratorio | Verificar juntas y puntos de goteo |
| **Conductividad** | Línea base → meta anual | **Mensual** | Medidor calibrado | Ajuste en ablandamiento/RO si aplica |

> **Nota de auditoría — cadena de custodia:** Conservar **boletas**, **resultados firmados** y **archivos PDF con hash/QR** en Odoo. Incluir **checklist de muestreo** y **mapa de puntos** en `ANX-PMSA-EFL`.

---

## 7.3 HVAC, bioaerosoles y control de olores

**Objetivos de diseño (salas “sucias”):**  
- **ΔP objetivo:** **−15 Pa** (banda de alarma −10↔−20 Pa).  
- **Q de captación localizada:**  
  - **Descarga/recepción:** **≥ 4.000 m³/h** por punto (velocidad de cara ≥ 0,5 m/s).  
  - **Triturador/tolva:** **≥ 6.000 m³/h** (encapsulado con extracción dedicada).  
  - **Tasa de renovación**: **≥ 12 ACH** (ajustar por volumen y nº de líneas activas).  
- **Filtración:** **MERV-13** en impulsión general; **HEPA H13** en puntos críticos/retornos si se requiere.

**Plan de bioaerosoles/olores (PMSA):**

| Ítem | Indicador / Umbral | Frecuencia | Acción |
|---|---|---:|---|
| **Diferencial de presión (ΔP)** | −15 Pa (alarma −10↔−20) | **Continuo** + revisión **diaria** | Verificar fugas/sellos, ajustar caudales |
| **Caudal de extracción (Q)** | ≥ diseño por punto | **Mensual** (velocidades) | Balanceo y limpieza ductos/filtros |
| **UFC/m³ (bioaerosoles)** | Línea base + meta | **Mensual** *(quincenal** si alto riesgo)* | Intensificar limpieza/SIP; revisar captación |
| **Olor (episodios)** | 0 incidentes por mes | **Continuo** (registro de reclamos) | Ajustar extracción; carbón activado/biofiltro según evaluación |
| **Filtros MERV-13/HEPA** | ΔP filtros / vida útil | Según plan mantto | Reemplazo; registro y disposición |

> **Nota de auditoría — SOP:** Mantener **SOP de limpieza** (cintas/tolvas, SIP/CIP), **listas de chequeo** por turno y **calibraciones** de transductores ΔP/Q. Códigos `SOP-HVAC-ΔP`, `SOP-HVAC-FILTROS`, `SOP-HVAC-LIMPIEZA`.

---

## 7.4 Ruido: barreras, encapsulados y plan de monitoreo

**Estrategia de control (origen + transmisión + receptor):**  
- **Origen:** encapsulados acústicos (triturador, bombas, compresor, casa de máquinas), anclajes antivibratorios, **piso flotante** en equipos vibratorios.  
- **Transmisión:** **barreras perimetrales** 3–6 m (masa ≥ 20 kg/m², cara interna absorbente), ductos con **silenciadores** y revestimiento absorbente interno, tratamiento NRC ≥ 0,8 en salas ruidosas.  
- **Receptor (línea de propiedad):** metas **`[META_DÍA_dB]` / `[META_NOCHE_dB]`** (ajustables por IM).

**Monitoreo de ruido (PMSA):**

| Punto | Indicador | Frecuencia | Método / Equipo | Acción |
|---|---|---:|---|---|
| **Perímetro N/E/S/O** | dB(A) día/noche | **Trimestral** / ante cambios | IEC 61672 / ISO 1996 | Ajuste de barreras, horarios, encapsulados |
| **Interior – casa de máquinas** | dB(A) ocupacional | **Mensual** | Dosimetría | Programas SST / EPP |
| **Playa de descarga** | dB(A) en operación | **Mensual** | Spot checks | Gestión horaria, ≤10 km/h |

> **Nota de auditoría — línea base:** Levantar **línea base** preoperativa en 3–5 puntos perimetrales. Mapear en `ANX-RUIDO` y cruzar con Cap. 11–12.

---

## 7.5 ENMS (ISO 50001): kWh/t, picos y FV en oficinas

**Objetivos energéticos (anuales):**  
- **kWh/t**: establecer **línea base** en el primer trimestre y meta de **mejora ≥ 3 %** anual.  
- **Reducción de picos**: aplanar demanda con **desfase 15 min** y lógica de calderas; meta de **≤ P95** contractual.  
- **Recuperación de calor**: **≥ 60 %** del salto térmico del condensado usado para precalentar agua de alimentación (validar en Cap. 9).  
- **FV oficinas**: instalación para **offset diurno** de consumos de **oficinas/IT/HVAC liviano** (no fuente firme para vapor).

**KPIs y verificaciones:**

| KPI | Meta / Criterio | Medición | Responsable |
|---|---|---|---|
| **kWh/t (planta)** | Mejora ≥ 3 % anual | Medidores por tablero/caldera | Energía |
| **Pico 15-min** | ≤ contrato / sin penalidades | Registrador + facturas UTE | Energía |
| **kgv/t (vapor)** | Tendencia decreciente | Caudalímetro/estimación | Proceso |
| **% recuperación calor** | ≥ 60 % | ΔT/ΔH en ICX y balances | Proceso |
| **FV oficinas (kWh)** | Cumplir generación estimada | Inversor/medidor | Energía |

> **Nota de auditoría — Plan de Medición y Verificación (M&V):** Definir fronteras, instrumentos y **incertidumbre**. Vincular M&V a **auditorías internas** ISO 50001 y **revisiones gerenciales**.

---

## 7.6 Vínculo con el PMSA (Cap. 15) y acciones correctivas

**Parámetros del PMSA derivados de este capítulo:**  
- **Efluentes:** T continua + mensual (T, pH, SST, DQO, O&G).  
- **Aire interior:** ΔP/Q continuo + mensual (UFC/m³; **quincenal** si alto riesgo).  
- **Ruido:** perimetral trimestral; mensual en áreas internas críticas.  
- **Energía:** kWh/t mensual; pico 15-min con revisión semanal.  
- **Incidentes/quejas:** canalizado a **SLA** con análisis causal y plan de acción.

**Acciones correctivas estándar (ejemplos):**  
- **T vertido ≥ 40 °C:** recirculación, revisión de intercambiador y válvulas; reporte a OSE si aplica.  
- **ΔP fuera de banda:** verificación de fugas/sellos, aumento de extracción, mantenimiento de filtros.  
- **dB(A) > meta:** refuerzo de encapsulados, ajustes de horario, mantenimiento de ventiladores.  
- **kWh/t > P95:** recalibrar recetas, secuenciar arranques, revisar purgas y aislamiento térmico.

> **Nota de auditoría — trazabilidad:** Todas las **acciones** y **verificaciones** deben quedar registradas en Odoo (**rss_trace** / **Documentos**), con **responsable y fecha**. Los PDFs con **hash** se archivan ≥ 5 años.

---

## 7.7 Índice de la sección

- **7.1 Matriz de aspectos e impactos**  
- **7.2 Efluentes líquidos (templado < 40 °C)**  
- **7.3 HVAC, bioaerosoles y olores**  
- **7.4 Ruido: barreras y monitoreo**  
- **7.5 ENMS (ISO 50001): KPIs y objetivos**  
- **7.6 Vínculo con PMSA y acciones correctivas**

> **Checklist de cierre (Cap. 7):**  
> ☐ Matriz S/O/D validada · ☐ Tabla de efluentes con límites/métodos confirmados por OSE · ☐ Setpoints HVAC y plan de bioaerosoles activados · ☐ Plan de ruido y línea base definidos · ☐ KPIs ISO 50001 configurados.


# 8. Memoria de cálculo — capacidad, vapor, agua y electricidad

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Referencias:** ISO 14040/14044 (LCI/LCIA), ISO 17665-1 / EN 285 (esterilización a vapor), ISO 50001 (energía), ISO 9001/14001/45001/19011/27001/31000.  
> **Parámetros fijados:**  
> • Conversión **530 kgv/h ≈ 400 kW** ⇒ **0,7547 kW/(kgv/h)**.  
> • Perfil por línea (autoclave 165 kg/ciclo; ~45 min/ciclo): **promedio ≈ 172 kg/h**, **pico ≈ 300 kg/h**.  
> • **Desfase 15 min** entre líneas; operación **24/7**.  
> • Configuración base: **3 líneas** (escalable a **5–7**); vapor **2×530 kgv/h (N+1)**.

---

## 8.1 Supuestos y metodología

- **Intensidad de vapor por línea** se calcula a partir del perfil de ciclo (rampa–plateau–post‐vacío) promediado en régimen estacionario.  
- **Promedios de planta** consideran **desfase de 15 min** para aplanar picos.  
- **OEE** afecta horas efectivas, **no** la **intensidad** específica (*kgv/t; kWh/t; m³/t*), que permanece **invariante** en operación estable.  
- **Agua de alimentación** ≈ **1,0 L/kgv** + **blowdown** (**5–10 %**) según calidad/sistema (ablandamiento/RO).  
- **Demanda eléctrica** de calderas deriva de **0,7547 kW/(kgv/h)**; auxiliares se suman como **cargas medias**.

> **Nota de auditoría — validación de datos**  
> Confirmar **curvas reales** de T/P y **consumos de caldera** en **FAT/SAT** (Secc. 8.6). Ajustar m³/t y kWh/t con mediciones del **PMSA** (Cap. 15) durante el primer trimestre.

---

## 8.2 Balance de vapor (promedio / pico) y cobertura N+1

### 8.2.1 Por línea
- **Promedio:** 172 kgv/h → **129,81 kW**  
- **Pico:** 300 kgv/h → **226,41 kW**

### 8.2.2 Planta (3 / 5 / 7 líneas) con **desfase 15 min**

| Líneas | Vapor **prom.** (kgv/h) | Vapor **pico** (kgv/h)\* | Potencia **prom.** (kW) | Potencia **pico** (kW) |
|---:|---:|---:|---:|---:|
| 3 | **516** | **≈ 540** | **389,43** | **≈ 407,54** |
| 5 | **860** | **≈ 1.05–1.10×prom.** → **≈ 900–950** | **648,04** | **≈ 679–718** |
| 7 | **1.204** | **≥ 1.10×prom.** → **≈ 1.330** | **907,65** | **≈ 1.003** |

\*El **pico** refleja **solapes parciales** de etapas de alta demanda pese al desfase; para 3 líneas se observa ≈**540 kgv/h** (dos picos coincidentes). Para configuraciones ≥5, adoptar factor **1,05–1,15×promedio** salvo verificación dinámica.

**Cobertura con 2×530 kgv/h (N+1):**
- **Capacidad instalada de vapor:** **1.060 kgv/h**.  
- **3 líneas:** holgura **> 95 %** sobre promedio y **> 90 %** sobre pico → **OK**.  
- **5 líneas:** cubre **promedio (860)** y picos **hasta ~950** (**OK** con control de arranques y PRV**).  
- **7 líneas:** **excede** 1.060 kgv/h en promedio → requiere **upgrade** (p. ej., **+1×300 kgv/h** o **3×530 kgv/h** con operación 2 en servicio + 1 reserva).

> **Nota de auditoría — set de control**  
> Implementar **arranques escalonados**, **valvulería de seccionamiento**, **PRV** y monitoreo de **trampas** para estabilizar demanda.

---

## 8.3 Balance de agua (alimentación + blowdown)

**Relación base:** **1,0 L/kgv**. **Blowdown:** **+5 a 10 %**.

| Configuración | kgv/h (prom.) | **Alimentación** (m³/h) | **Con blowdown 10 %** (m³/h) |
|---|---:|---:|---:|
| **3 líneas** | 516 | 0,516 | **0,568** |
| **5 líneas** | 860 | 0,860 | **0,946** |
| **7 líneas** | 1.204 | 1,204 | **1,324** |

**Tanques de reserva recomendados:** ≥ **2 × 5 m³** (contingencias OSE y estabilidad térmica).  
**Intercambiador ICX:** recuperación de calor del **condensado** para **precalentar** agua de alimentación y garantizar **T vertido < 40 °C** (Secc. 8.6).

> **Nota de auditoría — calidad de agua**  
> Definir **ablandamiento/RO** según **conductividad** y **sílice** locales (impacto en purgas y vida útil).

---

## 8.4 Demanda eléctrica — instalado vs. demanda media

### 8.4.1 Calderas (proceso)
- **Potencia equivalente** = vapor (kgv/h) × **0,7547 kW/(kgv/h)**.  
- **3 líneas (prom.)** → **389,43 kW**; **pico** → **≈ 407,54 kW**.  
- **5 líneas (prom.)** → **648,04 kW**; **pico** → **≈ 679–718 kW**.

### 8.4.2 Auxiliares (valores guía, ajustar con hojas de datos)
- **Trituradores**: 3×30 CV (**≈ 66 kW** instalados). **Demanda media**: **5–7 kW/ línea** → **15–21 kW**.  
- **Bombas vacío / agua**: **6–12 kW** instalados; **media**: **3–6 kW**.  
- **Compresor + secador**: **7,5–11 kW** instalados; **media**: **3–5 kW**.  
- **HVAC/extracción** (captación localizada + renovación): **20–40 kW** instalados; **media**: **10–20 kW**.  
- **Sistemas/IT/iluminación-oficinas**: **3–8 kW** medios.

**Demanda media total estimada (3 líneas):**  
- **Boiler load prom.:** ~**390 kW**  
- **Auxiliares media:** **~35–50 kW**  
- **Total prom.:** **~425–440 kW** (pico breve: **~470–500 kW**)

> **Nota de auditoría — UTE**  
> Dimensionar **transformación** y **protecciones** con factor de simultaneidad. Confirmar **potencia contratada** y **curva 15-min** para evitar penalidades.

---

## 8.5 Indicadores específicos (kgv/t, m³/t, kWh/t)

> **Clave:** La **intensidad específica** es **independiente** del **OEE** en régimen estable (ambos —consumo y t— escalan con horas efectivas).

**Por línea (165 kg/ciclo; 45 min; 24 h):**
- **Throughput día (100 %):** **5,28 t/d**; (75 %): **3,96 t/d**.  
- **Vapor día (100 %):** **4.128 kgv/d**; (75 %): **3.096 kgv/d**.  
- **Energía día (100 %):** **≈ 3.115 kWh/d**; (75 %): **≈ 2.336 kWh/d**.

**Intensidades (válidas tanto a 75 % como a 100 %):**
- **kgv/t** = **≈ 782 kgv/t** (4.128 ÷ 5,28).  
- **m³/t (agua)** = **≈ 0,782 m³/t** (**+10 %** con blowdown ⇒ **≈ 0,860 m³/t**).  
- **kWh/t (caldera)** = **≈ 590 kWh/t** (3.115 ÷ 5,28).  
- **kWh/t (total, incluyendo auxiliares)** = **≈ `[590 + AUX_kWh_t]`**; con **auxiliares** de **~20–40 kWh/t** ⇒ **≈ 610–630 kWh/t** *(placeholder a validar en SAT/PMSA)*.

> **Nota de auditoría — M&V (ISO 50001)**  
> Establecer **línea base** trimestral de **kWh/t**, **kgv/t** y **m³/t**; metas de mejora **≥ 3 %** anual. Reporte mensual en Odoo (tablero **ENMS**).

---

## 8.6 Criterios **FAT/SAT** vinculados a mediciones y **T < 40 °C**

**FAT (fábrica):**
- Verificación de **enclavamientos** (puertas, presostatos, válvula de seguridad).  
- **Curvas T/P** nominales por receta; **exportación CSV/PDF**; precisión de sensores (certificados).  
- Simulación de **perfiles de vapor** y **modulación** de carga.

**SAT (sitio):**
- **Curvas T/P** con **carga test** y **agua local**; **BI/IC** por ≥3 tipos de carga (porosidad/densidad).  
- **Punto de muestreo (PME-01)**: demostrar **T < 40 °C** en continuo; **alarma** a **38 °C**; **paro** ≥ **40 °C** con **recirculación**.  
- **Caudal de vapor** y **potencia de calderas**: confirmar promedio/pico en 3/5 líneas con desfase 15 min.  
- **kWh/t** (boiler + auxiliares): levantar base de referencia (24–72 h).  
- **Ruido** en operación: medición en **línea de propiedad** (día/noche) vs. metas (placeholders Cap. 11).

**Criterios de aceptación (extracto):**
- **BI negativo** 100 %; **IC** conforme 100 %.  
- **Curvas T/P** dentro de tolerancias de receta (**±[ΔT] °C / ±[ΔP] bar**).  
- **T vertido** **< 40 °C** **100 % del tiempo** medido (registro continuo + actas de muestra).  
- **kWh/t** y **kgv/t** dentro de **±10 %** del cálculo de diseño (tras 72 h).  
- **Sin** alarmas críticas no resueltas; **datos** exportados y **hash** verificado.

> **Nota de auditoría — evidencia y control**  
> Archivar **protocolos FAT/SAT**, certificados de **calibración**, reportes **CSV/PDF** con **QR+hash**, y fotografías de **P&ID / PME-01**. Codificar `ANX-FAT`, `ANX-SAT`, `ANX-ISMS-BKP`.

---

## 8.7 Síntesis y trazabilidad a capítulos

- **Vapor/Agua:** Secciones **8.2–8.3** ↔ **Cap. 10** (piano, PRV, trampas, ICX) y **Cap. 15** (PMSA efluentes).  
- **Electricidad:** Sección **8.4** ↔ **Cap. 9** (tableros, demanda, grupos) y **UTE**.  
- **Indicadores:** Sección **8.5** ↔ **Cap. 16** (Matriz de cumplimiento) y **ISO 50001**.  
- **FAT/SAT:** Sección **8.6** ↔ **Cap. 17** (entregables) y **Cap. 14** (trazabilidad Odoo).

> **Checklist de cierre (Cap. 8):**  
> ☐ Confirmar **potencia UTE** y curva 15-min · ☐ Validar **ICX** y **PME-01** en sitio · ☐ Registrar **línea base** de **kWh/t, kgv/t, m³/t** · ☐ Protocolizar **alarmas** (38/40 °C) · ☐ Cerrar **FAT/SAT** con evidencias.


# 9. Servicios auxiliares y manejo de vapor/condensado

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Normas guía:** ISO 17665-1 / EN 285 (esterilizadores a vapor), NR-13 / ASME B31.1/B31.3 (tuberías) si necesario, ISO 50001 (energía), ISO 14001 (ambiental), ISO 27001/19011 (datos/auditoría), **NR-13** (referencia técnica vasos de presión y accesorios).  
> **Parámetros de diseño fijados:** 3 líneas (esc. 5–7); **2×530 kgv/h (N+1)**; perfil por línea **~172 kgv/h prom. / 300 kgv/h pico**; **templado de condensado < 40 °C** y **punto de muestreo**; **intercambiador** para **precalentar agua fría de alimentación** con calor del condensado (recuperación energética).

---

## Índice de la sección
- **9.1 Piano de vapor (arquitectura, PRV, separadores, purgadores, seguridad)**  
- **9.2 Recuperación de calor del condensado (balance térmico y esquema)**  
- **9.3 Retorno/descarga de condensado, deaeración y vertido < 40 °C**  
- **9.4 Instrumentación y control (loops críticos y alarmas)**  
- **9.5 Matriz de equipos (tags) e isométricos (placeholders)**  
- **9.6 MTO preliminar (materiales, diámetros, aislamiento)**  
- **9.7 FAT/SAT y certificaciones (válvulas/sensores)**

---

## 9.1 Piano de vapor (arquitectura, PRV, separadores, purgadores, seguridad)

**Esquema funcional (simplificado):**

flowchart TD

    %% === CALDERAS ===
    A[Caldera A 530] --> NRV[Válv. retención (NRV-01/02)]
    B[Caldera B 530] --> NRV

    NRV --> HDR[Colector principal 2" SCH80 (STM-HDR)]
    HDR --> SEP00[SEP-00<br/>Separador de vapor + purga]
    SEP00 --> PRV00[PRV-00<br/>Estación PRV general<br/>(by-pass + man/term.)]

    %% === DISTRIBUCIÓN A RISERS ===
    PRV00 -->|"Riser L1 1½\""| SEP01[SEP-01<br/>Separador L1]
    PRV00 -->|"Riser L2 1½\""| SEP02[SEP-02<br/>Separador L2]
    PRV00 -->|"Riser L3 1½\""| SEP03[SEP-03<br/>Separador L3]

    %% === PRV POR LÍNEA ===
    SEP01 --> PRV01[PRV-01]
    SEP02 --> PRV02[PRV-02]
    SEP03 --> PRV03[PRV-03]

    %% === TRAP Y RETORNO DE CONDENSADO ===
    PRV01 --> TRP01[TRP-01<br/>Trampa vapor → Ret. cond.]
    PRV02 --> TRP02[TRP-02<br/>Trampa vapor → Ret. cond.]
    PRV03 --> TRP03[TRP-03<br/>Trampa vapor → Ret. cond.]

    %% === AUTOCLAVES ===
    TRP01 --> L1[AUTOCLAVE L1]
    TRP02 --> L2[AUTOCLAVE L2]
    TRP03 --> L3[AUTOCLAVE L3]

    %% === ESTILO ===
    classDef boiler fill:#ffcc99,stroke:#b35900,stroke-width:1px;
    classDef device fill:#ccf2ff,stroke:#006680,stroke-width:1px;
    classDef trap fill:#e6ffe6,stroke:#267326,stroke-width:1px;
    classDef autoclave fill:#ffe6f2,stroke:#800040,stroke-width:1px;
    class A,B boiler;
    class NRV,HDR,SEP00,PRV00,SEP01,SEP02,SEP03,PRV01,PRV02,PRV03 device;
    class TRP01,TRP02,TRP03 trap;
    class L1,L2,L3 autoclave;


**Buenas prácticas obligatorias:**
- **Separadores de vapor (SEP-00…03)**: aguas arriba de cada PRV y antes de equipos críticos.  
- **Estaciones PRV** con: válvula de control, **by-pass manual**, válvula de seguridad aguas abajo, manómetro/termómetro y **filtro tipo “Y”** (strainer).  
- **Purgadores (TRP-xx)**: en drenes de bajantes, puntos bajos y salidas de equipos; incluir **by-pass y válvula de bloqueo**.  
- **Válvulas de seguridad (SRV-xx)**: calibradas por **entidad competente**, con **certificados** trazables; descarga a campana/área segura.  
- **Valvulería de seccionamiento** por tren y por equipo para mantenimiento sin parar planta.  
- **Aislamiento térmico** en líneas y accesorios (ver MTO).

> **Nota de auditoría — cumplimiento NR-13/ASME**  
> Adjuntar **prontuario** del vaso, **hojas de datos** y **certificados** (SRV, PRV, manómetros, presostatos). Ensayos de estanqueidad e hidrostáticos documentados.

---

## 9.2 Recuperación de calor del condensado (balance térmico y esquema)

**Objetivo:** recuperar el **calor sensible** del condensado para **precalentar** el agua fría de alimentación y **templar** el condensado a **< 40 °C** antes del vertido.

**Balance térmico (marcos de cálculo):**

- **Caudal de condensado medio (3 líneas):** `ṁ_cond ≈ 516 kg/h` (≈ generación de vapor promedio).  
- **Temperaturas de referencia:**  
  - Condensado a la entrada del intercambiador: `T_cond,in ≈ 90–95 °C` (tras separadores).  
  - Condensado a la salida (límite de vertido): `T_cond,out ≤ 38–40 °C` (control).  
  - Agua fría de red: `T_w,in ≈ [12–18] °C` (medir localmente).  
  - Agua precalentada objetivo: `T_w,out ≈ [45–60] °C` (limitado por pinch ΔT).

**Fórmulas:**

- **Energía recuperada:** `Q_rec = ṁ_cond · c_p · (T_cond,in − T_cond,out)`  
- **Elevación de agua fría:** `Q_rec = ṁ_w · c_p · (T_w,out − T_w,in)`

**Ejemplo numérico (orientativo):**  
Con `ṁ_cond = 516 kg/h`, `T_cond,in = 95 °C`, `T_cond,out = 38 °C`:  
`Q_rec ≈ 516 · 4,186 · (95−38) ≈ 123.000 kJ/h ≈ 34 kW`  
→ con `T_w,in = 15 °C` se pueden llevar **~0,5–0,6 m³/h** de agua a **~55–60 °C** (depende del pinch real).

**Arquitectura propuesta:**

flowchart LR

    %% === CIRCUITO DE CONDENSADO ===
    COND[RETORNO DE CONDENSADO] --> TKCOND[[TK-COND<br/>Tanque de condensado]]
    TKCOND --> PCOND[(BOMBA<br/>P-COND)]
    PCOND --> ICX[ICX-01<br/>Intercambiador de calor placas]

    %% Derivaciones desde el intercambiador
    ICX -->|"TCV controla<br/>T_cond,out ≤ 38–40 °C"| TCV[TCV<br/>Válvula de control de temperatura]
    ICX --> PME[PME-01<br/>Punto de muestreo]
    PME --> COLECTOR[COLECTOR<br/>Vertido / drenaje]

    %% === CIRCUITO DE AGUA FRÍA ===
    AF[AGUA FRÍA] --> FILTRO[FILTRO<br/>carbón / sedimentos]
    FILTRO --> ICX
    ICX --> AP[AGUA PRECALENTADA]
    AP --> TKFW[[TK-FW<br/>Feedwater (tanque de agua de alimentación)]]

    %% === ESTILO ===
    classDef tank fill:#e6f7ff,stroke:#0077b3,stroke-width:1px;
    classDef pump fill:#fff2cc,stroke:#b38f00,stroke-width:1px;
    classDef valve fill:#ffe6e6,stroke:#b30000,stroke-width:1px;
    classDef process fill:#f2f2f2,stroke:#666,stroke-width:1px;

    class TKCOND,TKFW tank;
    class PCOND pump;
    class TCV valve;
    class ICX,FILTRO,PME,COLECTOR process;


> **Meta energética:** **≥ 60 %** del ΔT disponible (condensado→<40 °C) transferido al tren de **agua de alimentación** (**verificar** en SAT con M&V de temperaturas y caudales).  
> **Control:** **TCV-ICX** modulante por **T_cond,out**; alarma a **38 °C** y **paro** de descarga si **≥ 40 °C** (recirculación temporal).

---

## 9.3 Retorno/descarga de condensado, deaeración y vertido < 40 °C

**Configuración base (compromiso ambiental):** **No retorno** de condensado al generador; **todo** condensado pasa por **ICX-01** para **templado < 40 °C** y se descarga a **colector**, con **PME-01** (muestreo) y registro de **T/pH/SST/DQO/O&G** (Cap. 7 y 15).

**Alternativa de mejora (a evaluar con DINACEA/OSE):** **Retorno parcial** a un **deaerador térmico (DA-01)** o **hot-well** para reducir consumo de agua/energía. Requiere **revisión del EsIA** y ajuste de compromisos de efluente.  
- Ventajas: menor **m³/t** y **kWh/t**; menor **blowdown**.  
- Condición: mantener **PME-01** para blowdown/derivaciones y cumplir **T<40 °C** en cada punto de vertido.

**Blowdown y derivaciones:**  
- **Purgas de caldera** (intermitentes/continuas): enfriamiento previo (**cooler de blowdown** o paso por **ICX-01**) antes del colector.  
- **Separador de “flash”** (si aplica): venteo a **campana** y condensado a **TK-COND**.

> **Nota de auditoría — PMSA/vertidos:** Documentar **diagrama de drenajes**, mapa de **puntos de muestreo** y **frecuencias**; registrar **alarmas** y **acciones** (recirculación, mantenimiento ICX, limpieza de intercambiador).

---

## 9.4 Instrumentación y control (loops críticos y alarmas)

| Loop / Tag | Variable | Setpoint / Límite | Acción de control | Alarma / Interlock |
|---|---|---|---|---|
| **PRV-00/01/02/03** | Presión vapor | `[P_set] bar(g)` | Válvula modulante + by-pass | Sobrepresión → **SRV** abre; paro de línea si P<`[P_min]` |
| **SEP-xx & TRP-xx** | Drenaje | N/A | Purgador termodinámico/termostático | Alarma por ΔT anómalo en retorno |
| **TCV-ICX-01** | **T_cond,out** | **38 °C** (parada ≥ 40 °C) | Modula agua fría al ICX | **Paro descarga** y recirculación |
| **FQI-STM-HDR** | Caudal vapor | `[kg/h]` | Registro ENMS | Pico > P95 → escalonar líneas |
| **ΔP-HVAC-SUCIA** | ΔP sala | −15 Pa | Control ventiladores | Alarma −10↔−20 Pa |
| **TT-PME-01** | **T vertido** | < 40 °C | Registro continuo | Alarma a 38 °C, evento si ≥ 40 °C |
| **Vibración TR-01** | mm/s RMS | `[umbral]` | Mantenimiento predictivo | Paro si > P99 |

> **Seguridad funcional:** enclavamientos **puerta-presión** en autoclaves; **LOW-LOW nivel** en tanques; **fail-close** en TCV-ICX; **UPS** para SCADA/registradores.

---

## 9.5 Matriz de equipos (tags) e isométricos (placeholders)

**Equipos principales:**

| Tag | Descripción | Servicio | Diám./Clase | Material |
|---|---|---|---|---|
| **STM-HDR** | Colector principal de vapor | Distribución | 2" SCH80 | ASTM A106 Gr.B + aislamiento |
| **PRV-00** | Estación PRV general | Reducción P | 2" | Acero/ANSI 300, con by-pass |
| **SEP-00** | Separador de vapor | Separación arrastres | 2" | Acero, drenaje a TRP-00 |
| **PRV-01/02/03** | Estaciones PRV por línea | L1–L3 | 1½" | ANSI 300, con strainer |
| **SEP-01/02/03** | Separadores por línea | L1–L3 | 1½" | Acero |
| **TRP-00..03** | Purgadores | Drenajes | ¾"–1" | Acero inoxidable |
| **ICX-01** | **Intercambiador de placas** | **Condensado↔Agua** | `[Q,kW]` | AISI-316 |
| **PME-01** | **Punto de muestreo efluente** | **T/pH/SST/DQO/O&G** | 1" | AISI-316, válvulas aguja |
| **TK-COND** | Tanque de condensado | Amortiguación | `[V,L]` | AISI-304/CS rev. |
| **TK-FW** | Tanque de alimentación | Feedwater | `[V,L]` | AISI-304, con level |
| **DA-01** | Deaerador (opcional) | Retorno parcial | `[Q,kg/h]` | CS rev., bandejas |
| **SRV-xx** | Válvulas de seguridad | Protección | `[set,bar]` | Con certificado |

**Isométricos (placeholders a emitir):**
- `ISO-STM-001` Colector y PRV-00/SEP-00/ramales.
- `ISO-STM-L1/L2/L3` Estaciones por línea y conexiones a autoclaves.
- `ISO-COND-001` Red de condensado a **TK-COND** e **ICX-01**.
- `ISO-EFL-001` Descarga **ICX-01 → PME-01 → colector**.

> **Nota de auditoría — planos y listas:** Vincular con **P&ID** `PID-STM-001` y **lista MTO**; control de versiones y firmas.

---

## 9.6 MTO preliminar (materiales, diámetros, aislamiento)

**Tuberías (estimación inicial):**

| Servicio | Diám. nominal | Long. estimada `[m]` | Especificación | Aislamiento |
|---|---|---:|---|---|
| Vapor principal | 2" SCH80 | `"[L1]"` | ASTM A106 Gr.B | 50 mm lana mineral + aluminio |
| Ramales a líneas | 1½" SCH80 | `"[L2]"` | ASTM A106 Gr.B | 40 mm lana mineral |
| Drenes / purgas | ¾"–1" | `"[L3]"` | ASTM A106 Gr.B | 25 mm |
| Condensado a ICX | 1" | `"[L4]"` | ASTM A106 Gr.B | 25 mm |
| Agua fría/alimentación | 1"–1½" | `"[L5]"` | AISI-304/PPR-FR | 19–25 mm |

**Válvulas/Accesorios (resumen):**  
- PRV: `"[N]"` unidades; SRV: `"[N]"` unidades; Strainers: `"[N]"`; Purgadores: `"[N]"`; Válvulas bola/paso: `"[N]"`.  
- **Instrumentación:** `TT` (temperatura), `PT` (presión), `FQI` (caudal), `LT` (nivel), `ΔP` filtros.

> **Nota de auditoría — materiales y corrosión:** Confirmar **compatibilidad** con efluente y **calidad del agua**; especificar **inoxidable** en puntos de muestreo (**PME-01**) y **ICX-01**.

---

## 9.7 FAT/SAT y certificaciones (válvulas/sensores)

**FAT (fabricante / skid de vapor):**
- Integridad mecánica; pruebas de **estanqueidad** (ISO 5208/EN 12266-1), **calibración** de **SRV** y **PRV** con trazabilidad; verificación de **instrumentos** (certificados).  
- Ensayo funcional de **TCV-ICX** y lectura de **TT-PME-01**.

**SAT (sitio):**
- Medición de **T_cond,out** en **ICX-01** (24–72 h): **cumplimiento < 40 °C 100 %** del tiempo (alarma 38 °C).  
- Confirmación de **picos** y **medias** de caudal de vapor vs. capítulo 8; verificación de **drenajes** y **purgadores** (ΔT).  
- **Muestreo** en **PME-01** con cadena de custodia (T/pH/SST/DQO/O&G).  
- **Pruebas de seguridad:** SRV abre al setpoint; enclavamientos; parada por **over-temp** en efluente.

> **Entrega de evidencias:** Protocolos **FAT/SAT** firmados, **certificados** (SRV/PRV/PT/TT), croquis **P&ID** actualizado **as-built**, **MTO** definitivo y plan de **mantenimiento** (repuestos críticos: juntas, purgadores, SRV).

---

## 9.8 Checklist de cierre (Cap. 9)

- ☐ PRV/SEP/TRP dimensionados y ubicados en **P&ID**  
- ☐ **ICX-01** seleccionado (placas, área, `Q_rec`) y **TCV** configurado  
- ☐ **PME-01** operativo; plan de muestreo y registro en Odoo  
- ☐ Aislamiento térmico y **apoyo** de tuberías definidos  
- ☐ **SRV** y **sensores** con certificados y fechas de recalibración  
- ☐ **Isométricos** y **MTO** emitidos con control de versiones  
- ☐ Interlocks (38/40 °C) y **black-start** probados con grupo electrógeno

---
# 10. HVAC, aire interior y control de olores

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Normas guía:** ISO 14001 (SGA), ISO 45001 (SST), ISO 50001 (energía), ISO 19011 (auditorías), ISO 14644/EN 1822 (filtración HEPA como referencia), IEC 61672/ISO 1996 (ruido).  
> **Alcance:** Salas de **recepción/descarga** y **trituración** (áreas “sucias”), esclusas, corredores adyacentes y extracción específica de fuentes.  
> **Supuestos fijados:** Operación **24/7**, **desfase 15 min** entre líneas, **sin pre-triturado**; **3 líneas** (esc. 5–7).

---

## 10.1 Objetivos de control y metas

- **Depresión (sala sucia):** **−15 Pa** respecto a adyacentes (**banda de alarma:** **−10 ↔ −20 Pa**).  
- **Captación localizada (por punto):**  
  - **Descarga/recepción:** **≥ 4.000 m³/h** por punto (**velocidad de cara ≥ 0,5 m/s**).  
  - **Triturador/tolva:** **≥ 6.000 m³/h** (**encapsulado** con extracción dedicada).  
- **Renovación total sala sucia:** **≥ 12 ACH** (ajustar por volumen y nº de líneas activas).  
- **Escalado por líneas activas:**  
  \[
  Q_{\text{total}} \approx 4.000 \times (\#\text{puntos descarga activos})\;+\;6.000 \times (\#\text{trituradores activos})
  \]
- **Filtración:** **MERV-13** general; **HEPA H13** en retornos/puntos críticos cuando la evaluación lo requiera.  
- **Olores/bioaerosoles:** eventos **0/mes** (meta), con respuesta y trazabilidad.  

> **Nota de auditoría (metas cuantitativas):** Registrar en **PMSA** (Cap. 15) los **setpoints**, **bandas de alarma** y **métodos de verificación** (anemometría, ΔP, PAO/DEHS en HEPA).

---

## 10.2 Estrategia de depresión y enclavamientos

- **Cascada de presiones (referencia):**  
  - Sala sucia **−15 Pa** ← Esclusa **−5 Pa** ← Corredor **0 Pa**.  
- **Sellos y arquitectura:** puertas con **burletes perimetrales** y **umbral automático**; esclusa con **cierres intertrabados** (no abre puerta B si A está abierta).  
- **Balance y control:** compuertas motorizadas y **VFD** en extractores para mantener ΔP objetivo; bypass de emergencia para sobrepresión.  
- **Prueba de humo:** ensayos trimestrales de trayectorias de flujo (registro fotográfico).

> **Nota de auditoría:** Planos **P&ID-HVAC** con puntos de control ΔP y rutas de aire. Registrar **certificados de calibración** de transductores de presión.

---

## 10.3 Captación localizada y caudales

| Punto | Requisito | Diseño base | Verificación |
|---|---|---|---|
| Descarga/recepción (por boca) | **≥ 4.000 m³/h** y **≥ 0,5 m/s** | Campana tipo “slot” con faldones; ducto con silenciamiento | Anemómetro/velocímetro, trimestral |
| Triturador/tolva | **≥ 6.000 m³/h** (encapsulado) | Envolvente con **ventanas de inspección** y micro-sellos | Ensayo de humo, mensual |
| Sala sucia (global) | **≥ 12 ACH** | Suma de captaciones + extracción general | Relevamiento de ACH, semestral |

**Dimensionamiento por líneas (ejemplo 3 líneas):** si hay **3 puntos de descarga activos** y **3 trituradores**,  
\[
Q_{\text{total}} \approx (3 \times 4.000) + (3 \times 6.000) = \mathbf{30.000\ m^3/h}
\]  
(ajustar por simultaneidad real y volumen de sala para cumplir **≥12 ACH**).

> **Nota de auditoría:** Dejar **margen 15–20 %** en ventiladores para variaciones de carga/filtros. Guardar **curvas ventilador–sistema**.

---

## 10.4 Filtración, etapas y mantenimiento

- **Impulsión general:** **Prefiltro G4/F7** → **MERV-13**.  
- **Retornos/puntos críticos:** cajas **HEPA H13** con puerto PAO/DEHS para prueba de **integridad** (si se adopta HEPA).  
- **ΔP filtros:** umbral de cambio por **ΔP_max** del fabricante o **año** calendario (lo que ocurra primero).  
- **Limpieza:** protocolo **SOP-HVAC-LIMPIEZA** (ductos, rejillas, cajas HEPA); registro en Odoo **rss_trace**.

| Elemento | ΔP nueva (Pa) | ΔP cambio (Pa) | Frecuencia máx. | Evidencia |
|---|---:|---:|---|---|
| Prefiltro G4/F7 | `[xx]` | `[yy]` | Trimestral | Hoja de vida |
| MERV-13 | `[xx]` | `[yy]` | Semestral | ΔP/fecha/lote |
| HEPA H13 (si aplica) | `[xx]` | `[yy]` | Anual | Test PAO/DEHS |

> **Nota de auditoría:** Conservar **lotes de filtros** y **certificados**. Fotografiar **placas** y registrar **horas** de operación.

---

## 10.5 Control de olores y bioaerosoles

- **Fuente:** cabina de descarga y zona de trituración.  
- **Medidas primarias:** **encapsulado**, captación **dirigida**, limpieza y **SIP/CIP** del triturador/tolvas.  
- **Pulmón/Tratamiento:**  
  - **Carbón activado** en línea de extracción (bajo caudal) o  
  - **Biofiltro** para líneas de mayor caudal (evaluación técnica–espacio).  
- **Monitoreo bioaerosoles:** **UFC/m³** mensuales (**quincenales** si alto riesgo), con **línea base** y metas de reducción.  
- **Gestión de episodios de olor:** libro de eventos (fecha, meteorología, operación, acción correctiva).

> **Nota de auditoría:** SOP **SOP-OLOR-INC** (gestión de incidentes y comunicación). Registrar **0 episodios/mes** como meta.

---

## 10.6 Umbrales de alarma y tiempos de respuesta

| Variable | Setpoint / Umbral | Alarma | Tiempo de respuesta | Acción |
|---|---|---|---|---|
| **ΔP sala sucia** | **−15 Pa** (objetivo) | **Aviso:** −10 Pa · **Crítica:** −8 Pa o < −20 Pa | **15 min** (aviso) · **5 min** (crítica) | Ajuste VFD/extractores; verificar fugas/puertas |
| **Q captación descarga** | **≥ 4.000 m³/h** | **Aviso:** −10 % · **Crítica:** −20 % | 30 min | Balanceo; limpieza filtros; revisar obstrucciones |
| **Q encapsulado triturador** | **≥ 6.000 m³/h** | Aviso: −10 % · Crítica: −20 % | 30 min | Inspección encapsulado y ducto |
| **UFC/m³** | Línea base + meta | **Crítica:** > P95 base | 24 h | Refuerzo limpieza; revisar HEPA/captación |
| **Olor (evento)** | 0/mes (meta) | 1 evento | Inmediata | Activar carbón/biofiltro; auditoría operativa |
| **ΔP HEPA** | Dentro de banda | **Crítica:** > ΔP_max | 2 h | Cambio de filtro; prueba PAO/DEHS (si aplica) |

> **Nota de auditoría:** Las **acciones y tiempos** se integran al **PMSA** (Cap. 15) con responsables (Operación, Mantenimiento, HSE) y **SLA**.

---

## 10.7 Monitoreo, registros y trazabilidad

- **Continuo:** ΔP sala (trend 1-min), estado VFD, alarmas; **T/HR** de sala; estado de puertas.  
- **Periódico:** **UFC/m³** (mensual/quin.), **velocidad de cara** (trimestral), **ACH** (semestral), **olor** (eventos).  
- **Registros:** Odoo **rss_trace** (checklist por turno, alarmas, mantenimiento), con **CSV/PDF** firmados (**QR + hash**, retención **≥ 5 años**).  
- **Reportes:** tablero mensual con **ΔP cumplidas (% tiempo)**, **Q dentro de banda**, **UFC**, **incidentes** y **acciones**.

> **Nota de auditoría:** Ensayos **humo**, **anemometría**, **PAO/DEHS** (HEPA) documentados. Adjuntar en `ANX-HVAC-VERIF`.

---

## 10.8 Energía y ruido de HVAC

- **Energía:** **VFD**, programación **nocturna** y **modulación** por demanda; KPI **kWh/t** de HVAC (en ENMS).  
- **Silenciamiento:** **silenciadores** en extractores, **revestimiento absorbente** en ductos, tratamiento **NRC ≥ 0,8** en sala; velocidades en ductos dentro de rangos **bajo ruido**.  
- **Ruido en línea de propiedad:** coherente con metas **`[META_DÍA_dB] / [META_NOCHE_dB]`** (Cap. 11 y 7.4).

> **Nota de auditoría:** Curvas de **IN/OUT** de silenciadores, mapas de ruido y verificación de **dBA** en puntos perimetrales.

---

## 10.9 FAT/SAT de HVAC y aceptación

- **FAT (fabricante de unidades/HEPA):** performance de ventiladores, **ΔP** filtros, certificaciones **HEPA** y ensayos de integridad (si aplica).  
- **SAT (sitio):**  
  - **ΔP sala**: ≥ **95 %** del tiempo en **−15 ±5 Pa** en 24–72 h.  
  - **Q captaciones**: ≥ **100 %** del diseño en medición de campo (tolerancia −0/+10 %).  
  - **ACH**: **≥ 12** (cálculo y medición).  
  - **HEPA**: test **PAO/DEHS** (si aplica) y registros.  
  - **Ensayo de humo** en cabina y encapsulado: captación completa.

> **Criterios de aceptación:** Todos los puntos **conformes** y **bitácoras** cargadas en Odoo; **acciones** ante desvíos cerradas.

---

## 10.10 Instrumentación y control (tags)

| Tag | Variable | Ubicación | Rango | Observación |
|---|---|---|---|---|
| **PT-ΔP-01** | ΔP sala sucia | Pared a corredor | ±50 Pa | Calibración anual |
| **FQI-EX-xx** | Caudal extracción | Ducto principal | `[0–30.000] m³/h` | Sensor pitot/ultrasónico |
| **VFD-EX-xx** | Velocidad extractor | Tablero | 0–100 % | Control ΔP/Q |
| **TT/HR-01** | T/HR sala | Sala sucia | — | Condiciones confort/condensación |
| **CNT-HEPA-xx** | Puerto PAO/DEHS | Caja HEPA | — | Ensayo integridad |
| **SW-DOOR-xx** | Estado puerta | Esclusa | — | Interlock puertas |

> **Nota de auditoría:** Listar **seriales** y **certificados**; incluir **plan de calibración** anual.

---

## 10.11 SOP y bitácoras

- **SOP-HVAC-ΔP:** ajuste VFD y verificación de sellos.  
- **SOP-HVAC-FILTROS:** cambio y disposición de filtros (trazabilidad del residuo).  
- **SOP-HVAC-LIMPIEZA:** cronograma de ductos/rejillas/cajas.  
- **SOP-OLOR-INC:** gestión de episodios de olor y comunicación.  
- **Bitácoras:** turnos (am/pm/noche) con checklist de ΔP, Q, puertas, alarmas; **firmas** Operador/Supervisor.

> **Nota de auditoría:** Todos los **SOP** con **control de versiones** y **firma** de responsable; PDFs con **QR+hash** en Odoo.

---

## 10.12 Checklist de cierre (Cap. 10)

- ☐ ΔP **−15 Pa** configurado con alarmas **−10 ↔ −20 Pa**  
- ☐ Q por puntos: **4.000/6.000 m³/h** verificado; **≥12 ACH**  
- ☐ Filtración **MERV-13** y **HEPA H13** (si aplica) con ΔP y pruebas definidas  
- ☐ Plan de **bioaerosoles**/**olores** implementado (UFC, eventos 0/mes)  
- ☐ **SOP**, **calibraciones** y **bitácoras** activos; integración Odoo (**hash/QR**)  
- ☐ FAT/SAT de HVAC ejecutado con evidencias y acciones cerradas

___
---
# 11. Ruido y vibraciones — Diseño + PMSA (plan de monitoreo y seguimiento)

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Marco normativo de referencia (Uruguay):**  
> • **Decreto 143/2012** (ruido) · **Decreto 281/016** (procedimientos/actualizaciones) · **Ley 17.852 (2004)** (convivencia/ruidos molestos).  
> **Normas técnicas de apoyo:** ISO **1996** (acústica ambiental), IEC **61672** (sonómetros), ISO **9613-2** (propagación), ISO **10816/20816** (vibraciones en máquinas), ISO **14001** (SGA), ISO **45001** (SST).

---

## 11.1 Inventario de fuentes y escenarios operativos

| Fuente | Descripción | Régimen | Observaciones / Riesgos |
|---|---|---|---|
| **Tránsito pesado** | Camiones ingreso/egreso, maniobras en playa | 24/7 (slots 15 min) | **Ralentí controlado** (prohibido >3 min), **≤10 km/h**, señalización |
| **Casa de máquinas** | Calderas eléctricas, bombas, compresores, ventiladores | Continuo | Encapsulados locales, **silenciadores** en ventilación |
| **Triturador** | Post-esterilización | Intermitente | **Encapsulado acústico** + extracción dedicada |
| **HVAC/extracción** | Captación localizada y ACH | Continuo | Silenciamiento de ductos, paneles absorbentes (NRC ≥ 0,8) |
| **Operaciones de descarga** | Golpeteo/impactos | Intermitente | Topes elásticos, pisos amortiguados, SOP de maniobra silenciosa |

> **Nota de auditoría — línea base:** Realizar **medición preoperativa** (día/noche) en 3–5 puntos perimetrales para fijar la situación **antes del montaje** (`ANX-RUIDO-LB`).

---

## 11.2 Criterios y metas en línea de propiedad (día/noche)

> Las metas se ajustarán a la **categoría IM** aplicable (zonificación `"[ZONIFICACIÓN_IM]"`). Hasta contar con la resolución municipal, se establecen **placeholders**:

| Categoría IM | Meta **día** `"[META_DÍA_dB]"` | Meta **noche** `"[META_NOCHE_dB]"` | Observaciones |
|---|---:|---:|---|
| Residencial / Sensible | `[META_DÍA_dB]` dB(A) | `[META_NOCHE_dB]` dB(A) | Aplicar **barreras** y **ventanas horarias** más restrictivas |
| Mixto | `[META_DÍA_dB]` dB(A) | `[META_NOCHE_dB]` dB(A) | Control de **ralentí** y secuenciación de maniobras |
| Industrial | `[META_DÍA_dB]` dB(A) | `[META_NOCHE_dB]` dB(A) | Cumplir aún con **picos** de carga/descarga |

**Criterio de cumplimiento:**  
- Emisión medida en **línea de propiedad**, **ponderación A**, **tiempo de integración** conforme Decreto 143/2012.  
- **No superar** la meta por **nivel continuo equivalente** (LAeq) y **evitar tonos emergentes** o impulsivos; si existen, aplicar **penalizaciones** conforme IM.

> **Nota de auditoría:** Al confirmar zonificación, **reemplazar placeholders** y **anexar** la tabla firmada en `ANX-IM-METAS`.

---

## 11.3 Diseño de mitigación (origen → transmisión → receptor)

**En el origen (equipos):**  
- **Encapsulados acústicos** en triturador, bombas, compresor y casa de máquinas (panel sándwich con núcleo mineral **≥ 60 kg/m³**; objetivo **Rw 45–50 dB**).  
- **Aisladores elastoméricos** y **piso flotante** en equipos vibratorios; frecuencia natural **< 0,7×** la de excitación.  
- **Mantenimiento preventivo** (alineación, balanceo, rodamientos) y checklists de ruido/vibración.

**En la transmisión (trayecto):**  
- **Barreras perimetrales** **3–6 m** (masa **≥20 kg/m²**, cara interna **absorbente**), pérdida por inserción objetivo **8–15 dB(A)**.  
- **Ductos** con **revestimiento absorbente** y **silenciadores** rectangulares en extractores.  
- Tratamiento interno de salas con **NRC ≥ 0,8** para reducir **RT60**.

**En el receptor (línea de propiedad):**  
- **Gestión horaria** de camiones (ventanas y limitación de simultaneidad).  
- **≤10 km/h**, pavimento silencioso, topes con recubrimiento elastomérico.  
- **Protocolo de ralentí**: apagado si permanencia > 3 min.

> **Plan B (si un equipo supera límites):** incorporar **caja de aislamiento acústico** a medida, revisando **ventilación** con **silenciadores** y tratamiento térmico.

---

## 11.4 Plan de medición perimetral y verificación (PMSA)

**Metodología:**  
- **Sonómetro clase 1** (IEC 61672) con **calibrador acústico**; **trípode** a 1,5 m; viento **< 5 m/s**; sin lluvia.  
- Puntos **N/E/S/O** (y receptores sensibles). Altura **1,5 m**; distancia ≥ 3,5 m de fachadas.  
- **Indicadores:** LAeq, LAmax, espectro en **1/3 de octava** para detectar **tonos**.  
- **Condiciones:** reportar meteorología, operación (líneas activas, camiones/h), incidencias.

**Frecuencia:**  
- **Trimestral** en perímetro (día/noche); **mensual** en **casa de máquinas** y **playa** para gestión operativa.  
- **Verificación post-montaje:** dentro de los **30 días** del arranque; luego al **cumplir 6 meses**.

**Criterios de conformidad:**  
- **LAeq(día/noche) ≤ Meta** por categoría IM.  
- Ausencia de **tonos** o **carácter impulsivo**; si existen, aplicar correcciones/penalizaciones y **mitigar**.  
- Gap máximo permitido entre **modelo** (ISO 9613-2) y **medición**: **±3 dB**; si >3 dB, **ajustar** barreras/encapsulados.

> **Nota de auditoría — evidencias:** Cargar **planillas**, **archivos de audio** (si procede), **espectros**, **fotos** de instrumentación y **calibraciones** en Odoo (`ANX-RUIDO-MED`).

---

## 11.5 Vibraciones (máquinas y ocupacional)

- **Criterio base** (ISO 10816/20816): **mm/s RMS** en rodamientos en banda `[10–1.000] Hz`; definir **umbrales** por clase de máquina:  
  - **Alerta:** `"[UMBRAL_ALERTA_mm/s]"` · **Crítica:** `"[UMBRAL_CRITICA_mm/s]"`.  
- **Medición** trimestral en triturador, bombas, compresor y ventiladores; **análisis espectral** para **desbalance/misalineación/solturas**.  
- **Acciones:** si > alerta → **balanceo/alineación**; si > crítica → **parada controlada** y **reparación**.  
- **Ocupacional:** evaluar vibración mano-brazo/plataformas si aplica (ISO 5349 / ISO 2631).

> **Nota de auditoría:** Registrar **tendencias** y **OTs** de mantenimiento; asociar a **KPIs de disponibilidad** (Cap. 6).

---

## 11.6 Programa operativo (ruido) y responsabilidades

| Actividad | Responsable | Frecuencia | Evidencia |
|---|---|---:|---|
| Auditoría de **ralentí** y velocidad | Logística/Seguridad | Semanal | Checklist con firmas |
| Revisión de **encapsulados** y **silenciadores** | Mantenimiento | Mensual | Informe con fotos |
| Medición **perimetral** día/noche | HSE/Consultor | Trimestral | Informe LAeq + espectros |
| Medición **interior** (casa de máquinas/playa) | HSE | Mensual | Spot checks + acciones |
| Revisión **barreras** (fisuras/sellos) | Mantenimiento | Trimestral | Parte de obra |
| **Modelo** ISO 9613-2 vs campo | Ingeniería/HSE | Semestral | Matriz dB (modelo↔medición) |

**KPIs:**  
- % tiempo **cumpliendo metas** en línea de propiedad; **nº de incidentes** por ruido; **dB(A)** interior en zonas críticas; **OTs** resueltas `< 7 días`.

---

## 11.7 Aceptación y acciones correctivas

**Criterios de aceptación del capítulo:**  
1) **Metas día/noche** configuradas (placeholders reemplazados al confirmar IM).  
2) **Barreras/encapsulados** construidos según especificación (masas, absorbentes, sellos).  
3) **PMSA** activo con mediciones **trimestrales** y **post-montaje**.  
4) **Plan de quejas** con SLA y trazabilidad (**0 quejas sin atender**).

**Acciones correctivas tipo:**  
- **Exceso perimetral:** elevar/engrosar barrera, aumentar absorción interna, ajustar horarios.  
- **Tonos/impulsivos:** cambiar **rpm**, poleas, **silenciadores** reactivos/absorbentes.  
- **Camiones:** redistribuir slots, señalética y **control** de tiempos.

> **Nota de auditoría — cierre:** Adjuntar **actas** de verificación, **mapas de ruido** y **as-built** de barreras/encapsulados (`ANX-RUIDO-ASB`). Integrar resultados a **Matriz de Cumplimiento** (Cap. 16) y **PMSA** (Cap. 15).

---

## 11.8 Checklist de cierre (Cap. 11)

- ☐ Metas **LAeq día/noche** definidas por categoría IM (placeholders → valores IM)  
- ☐ Barreras/encapsulados/silenciadores ejecutados y **verificados**  
- ☐ **PMSA** de ruido: metodología, puntos, frecuencia y responsables  
- ☐ **Línea base** y **post-montaje** medidos y archivados (Odoo, **QR + hash**)  
- ☐ Plan de **vibraciones** (umbrales, rutas, acciones) activo  
- ☐ SOPs y **bitácoras** con control de versiones y firmas

---
---
# 12. Logística de residuos y seguridad de descarga

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Alcance:** flujo logístico externo e interno, recepción y descarga de **RSS**, seguridad operativa/peatonal, control de tiempos y trazabilidad.  
> **Supuestos fijados:** **cabina de descarga con extracción dedicada**, **circuito unidireccional**, **slots de 15 min**, **permanencia en playa ≤ 30 min**, **pesaje con QR**, operación **24/7**.  
> **Referencias cruzadas:** Cap. 5 (proceso), Cap. 7 (ambiental), Cap. 8–9 (servicios), Cap. 10 (HVAC), Cap. 11 (ruido), Cap. 14 (trazabilidad), Cap. 15 (PMSA).

---

## Índice de la sección
- **12.1 Circuito logístico y trazabilidad (QR + pesaje)**  
- **12.2 Diseño de cabina de descarga (captación, limpieza, bioseguridad)**  
- **12.3 Gestión de tránsito pesado y seguridad peatonal**  
- **12.4 Procedimientos operativos, rechazos y contingencias**  
- **12.5 KPIs y tableros operativos**  
- **12.6 Señalética, perfiles viales y control de acceso (notas de auditoría)**  
- **12.7 Checklist de cierre (Cap. 12)**

---

## 12.1 Circuito logístico y trazabilidad (QR + pesaje)

**Objetivo:** asegurar **flujo seguro y trazable** desde ingreso a predio hasta expedición del residuo tratado, minimizando tiempos en playa y emisiones asociadas.

**Circuito unidireccional (esquema ASCII):**

flowchart LR
    VP[VÍA PÚBLICA] --> PORTON[Portón acceso]
    PORTON --> PRECHECK[Prechequeo (QR/agenda)]
    PRECHECK --> BASIN[Báscula de ingreso<br/>(PESO-IN)]
    BASIN --> ESP[Zona de espera señalizada]
    ESP --> CABINA[CABINA DE DESCARGA<br/>(extracción dedicada)]
    CABINA --> SUCIA[Sala sucia<br/>(ΔP -15 Pa)]

    %% Autoclaves en paralelo
    SUCIA --> AUT1[AUTOCLAVE L1]
    SUCIA --> AUT2[AUTOCLAVE L2]
    SUCIA --> AUT3[AUTOCLAVE L3]

    AUT1 --> TRIT[TRITURACIÓN]
    AUT2 --> TRIT
    AUT3 --> TRIT

    TRIT --> ACD[ACONDICIONAMIENTO / ESTIBA]
    ACD --> BASOUT[Báscula de egreso<br/>(PESO-OUT)]
    BASOUT --> SALIDA[Salida unidireccional]

    %% Estilos (opcionales)
    classDef autoclave fill:#ffe6f2,stroke:#800040,stroke-width:1px;
    classDef process fill:#f2f2f2,stroke:#666,stroke-width:1px;
    class AUT1,AUT2,AUT3 autoclave;
    class VP,PORTON,PRECHECK,BASIN,ESP,CABINA,SUCIA,TRIT,ACD,BASOUT,SALIDA process;


**Trazabilidad y control:**
- **Agenda con slots de 15 min** por vehículo y origen; geocercas opcionales (**ETA** en tablero).  
- **Identificación por QR/RFID** en contenedores/tarrinas y **conductor** (credencial).  
- **Pesaje en ingreso/egreso** (PESO-IN / PESO-OUT) vinculado a **lote** y **receta** en Odoo **rss_trace** (balance de masa).  
- **Control documental**: manifiesto digital, fotos de sello/precintos, temperatura ambiente, tiempo de permanencia.  
- **Política de permanencia:** **≤ 30 min** por camión en playa (P90).

> **Nota de auditoría (trazabilidad):** PDFs y CSV con **QR + hash** (Odoo) y retención **≥ 5 años**. Auditoría mensual de **balance de masa** (tolerancia `< 1 %`).

---

## 12.2 Diseño de cabina de descarga (captación, limpieza, bioseguridad)

**Función:** recinto **cerrado** para descarga, inspección visual, toma de muestra si aplica y transferencia a **sala sucia** con **control de olores/bioaerosoles**.

**Requisitos de ventilación y control (consistentes con Cap. 10):**
- **Extracción dedicada:** **≥ 4.000 m³/h por punto de descarga**; velocidad de cara **≥ 0,5 m/s**.  
- **Encapsulado local** (campanas tipo “slot” con faldones, deflectores).  
- **Depresión interna:** coherente con **−15 Pa** de sala sucia (cascada: cabina ≤ sala sucia).  
- **Filtración:** MERV-13 en impulsión; **opcional HEPA H13** en retorno crítico / línea de muestreo.  
- **Ruido:** silenciamiento en ductos y extractores; paneles absorbentes **NRC ≥ 0,8**.

**Diseño y operación:**
- **Piso antideslizante**, canaletas con rejillas, sumidero a **pretratamiento** (trampa sólidos), limpieza de superficies entre descargas.  
- **Puertas seccionales** con sensores y **interlock** (no abrir a la vez hacia sala sucia y exterior).  
- **Limpieza / CIP** de rampas y tolvas con agua templada; registro en Odoo (OT de limpieza).  
- **EPP** obligatorio: guantes resistentes, protección ocular, calzado de seguridad, RPA según evaluación.

> **Nota de auditoría (verificación):** Ensayo **humo** de campanas, medición **Q** y **ΔP** según plan; fotos y actas en `ANX-CAB-DESC`.

---

## 12.3 Gestión de tránsito pesado y seguridad peatonal

**Medidas de diseño:**
- **Circuito unidireccional** con **separación física** de peatones (barandas/cordones) y cruces señalizados.  
- **Velocidad ≤ 10 km/h**, **prohibición de marcha en vacío (ralentí) > 3 min**.  
- **Zona de espera** con capacidad acorde a picos (evita fila en vía pública).  
- **Iluminación apantallada**, sin deslumbramiento a vecinos; CCTV en puntos ciegos.  
- **Topes elásticos** y guías de rueda en cabina; **alarmas de marcha atrás** con señal **silenciosa direccional** (baja emisión a perímetro).

**Operación y seguridad:**
- **Briefing de seguridad** a conductores (inducción anual).  
- **Conos y balizamiento** según SOP; chalecos de alta visibilidad.  
- **Botón de emergencia** en cabina; plan de evacuación y ruta despejada.  
- **Ventanas horarias** para reducir picos y ruido nocturno (alineado a Cap. 11).

> **Nota de auditoría (perfiles viales):** Integrar croquis de **giros, radios y gálibos** en `ANX-VIAL-01`; validar con maniobras en vacío antes de operación.

---

## 12.4 Procedimientos operativos, rechazos y contingencias

**SOP-LOG-ING (ingreso):**
1. Verificación de agenda y **QR**.  
2. Chequeo de **sello/precintos** y estado de envases.  
3. **PESO-IN** y asignación de **bahía**.

**SOP-LOG-DESC (descarga):**
1. Ubicación en **cabina**; motor **OFF**; calzos colocados.  
2. Apertura controlada; captura local en campana; **inspección visual**.  
3. Transferencia a **sala sucia** (carros cerrados), registro fotográfico si corresponde.

**SOP-LOG-RECH (rechazo):**  
- **Causales:** embalaje inadecuado, derrame activo, **sospecha radioactiva** (portal gamma), mezcla no permitida.  
- **Acción:** cuarentena en área designada; notificación al generador; manifiesto con **observación**; recolección de contramuestra si procede.

**Contingencias:**
- **Derrame:** contención inmediata (kit) + limpieza; registro de incidente (PGR).  
- **Falla cabina/extracción:** detener descargas; priorizar lotes de menor riesgo; **reiniciar** cuando ΔP/Q dentro de banda.  
- **Congestión / cola > 30 min:** abrir **línea paralela** (si existe), reprogramar slots, ampliar ventana temporal.

> **Nota de auditoría (control de cambios):** Versionado de **SOP** y **formularios**; firmas de operador/supervisor; trazabilidad a lote.

---

## 12.5 KPIs y tableros operativos

| KPI | Definición | Meta | Fuente |
|---|---|---:|---|
| **Permanencia en playa (P90)** | min/camión (ingreso→egreso) | **≤ 30 min** | Odoo / básculas / CCTV |
| **Puntualidad de slots** | Arribos dentro de ±10 min | **≥ 95 %** | Agenda / geocercas |
| **Ocupación de bahías** | % tiempo activo | **≤ 85 %** (pico **≤ 95 %**) | SCADA / Odoo |
| **Rechazos** | % lotes rechazados | **≤ 1 %** | SOP-LOG-RECH |
| **Incidentes de seguridad** | Nº / mes | **0** | PGR / HSE |
| **Quejas por ruido/olor** | Nº / mes | **0** | Canal comunidad |

**Reportes:**
- **Diario:** permanencia, ocupación, puntualidad.  
- **Mensual:** rechazos, incidentes, quejas y acciones.  
- **Trimestral:** revisión de **slots** y capacidad (Cap. 6) y correlación con **ruido** (Cap. 11).

> **Nota de auditoría (ISMS):** Backups diarios + semanal **off-site**; PDFs con **QR + hash**; control de accesos.

---

## 12.6 Señalética, perfiles viales y control de acceso (notas de auditoría)

**Señalética mínima:**
- **Velocidad ≤ 10 km/h**, “**Motor apagado** durante descarga”, “**Prohibido fumar**”, “**EPP obligatorio**”, rutas de evacuación.  
- Marcación **horizontal** (flechas sentido único, líneas peatonales) y **vertical** (altura libre, cargas admisibles).

**Perfiles viales:**  
- Radios de giro, **gálibo** y **pendientes** validados para la flota prevista; pavimento **antideslizante**.  
- Ensayo de **maniobrabilidad** con vehículo tipo antes de apertura.

**Control de acceso:**  
- **Portón** con lector **QR/RFID**, **CCTV** y barrera; registro de **placa** y **conductor**; integración con agenda.  
- **Zona buffer** para evitar espera en vía pública.

> **Nota de auditoría:** Anexar **planos/croquis** firmados (`ANX-SEN-LOG`, `ANX-VIAL-01/02`) y **actas** de verificación de campo.

---

## 12.7 Checklist de cierre (Cap. 12)

- ☐ Circuito **unidireccional** implementado y señalizado  
- ☐ **Cabina de descarga** operativa (Q y ΔP verificados; limpieza y EPP)  
- ☐ **Permanencia ≤ 30 min** y **slots 15 min** activos  
- ☐ **Pesaje IN/OUT** integrado a **QR** y balance de masa  
- ☐ SOPs de ingreso/descarga/rechazos/derrames vigentes  
- ☐ KPIs y tableros en Odoo; backups y evidencia **QR + hash**  
- ☐ Perfiles viales y control de acceso verificados (actas/fotos)

---
---

# 13. SST (ISO 45001), PGR, HAZOP/What-If y emergencias

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Marcos de referencia:** **ISO 45001** (SST), **ISO 31000** (gestión de riesgos), **ISO 19011** (auditorías), **ISO 17665-1/EN 285** (esterilización a vapor), **NR13 - o ASME B31.1/B31.3** (piping), **IEC 61511** (seguridad funcional, referencia), **NR-13** (recipientes a presión, referencia técnica).  
> **Alcance:** Operación 24/7 de **3 líneas de autoclave** (esc. 5–7), **piano de vapor**, **cabina de descarga**, **trituración**, **HVAC** de salas sucias, **servicios** (eléctrico, aire, ICX, efluentes) y logística interna.

---

## 13.1 Identificación de peligros y controles (bow-tie resumido)

| Área/Equipo | Peligro principal | Consecuencia | Controles preventivos (antes) | Controles de mitigación (después) |
|---|---|---|---|---|
| **Calderas / piano de vapor** | **Sobrepresión / fuga de vapor** | Quemaduras, paro | SRV calibradas, PRV por tren, separadores, purgadores con by-pass, inspección NR-13, LOTO en mantenimiento | Pantallas térmicas, rutas de evacuación, ducha/lavaojos, EPP térmico, simulacro “fuga de vapor” |
| **Autoclaves** | **Atrapamiento / puerta / vacío** | Lesión grave | Enclavamientos puerta-presión, checklist pre-ciclo, BI/IC y curvas T/P, SOP de carga | Botón paro, ventilación de emergencia, primeros auxilios |
| **Triturador** | **Corte/atrapamiento** | Amputación, lesión | Guardas físicas, enclavamientos, llave de seguridad, SOP de limpieza con LOTO | Paro de emergencia, kit de contención, señalización |
| **Cabina de descarga** | **Derrame / bioaerosoles / olores** | Exposición biológica | Encapsulado con extracción dedicada, ΔP en cascada, EPP, contenedores conformes | Kit de derrames, desinfección, registro de incidente, refuerzo de extracción |
| **HVAC – sala sucia** | **Pérdida de depresión (ΔP)** | Migración de olores/bioaerosoles | ΔP objetivo −15 Pa (alarma −10↔−20), VFD, sellos de puerta, mantenimiento | Parada controlada de descarga, investigación de causa, restaurar setpoints |
| **Eléctrico / grupos** | **Corte / energización accidental** | Paro, choques | Tableros seccionados, protecciones, **LOTO**, UPS control, black-start documentado | Arranque escalonado, checklists de restablecimiento |
| **Efluentes / ICX** | **Vertido ≥ 40 °C** | Incumplimiento ambiental | TCV-ICX modulante, alarma 38 °C, paro ≥ 40 °C, PME-01 | Recirculación, aviso HSE, muestreo extraordinario |
| **Logística / tránsito** | **Impacto / atropello** | Lesiones | Circuito unidireccional, ≤10 km/h, balizamiento, inducción conductores | Investigación, rediseño de flujo, barreras |

> **Nota de auditoría:** Validar inventario de peligros con **inspección de línea** y entrevistas. Mantener **registro de hallazgos** en Odoo (no conformidades y acciones).

---

## 13.2 Matriz PGR (Plan de Gestión de Riesgos)

**Método:** Severidad (S 1–5) × Probabilidad (P 1–5) = **RPN**.  
**Criterios:** 1–5 (Bajo), 6–10 (Moderado), 12–15 (Alto), 16–25 (Crítico).

| Riesgo | S | P | **RPN** | Nivel | Acciones de control (propietario / plazo) |
|---|:--:|:--:|:--:|:--:|---|
| Sobrepresión en cabezal de vapor | 5 | 2 | **10** | Moderado | Calibración SRV semestral; prueba PRV; simulacro “fuga de vapor” (Mantto/HSE · 30 d) |
| Fuga de vapor por brida | 4 | 3 | **12** | Alto | Torqueado según MTO; inspección termográfica; stock de empaques (Mantto · 15 d) |
| Atrapamiento en triturador | 5 | 1 | **5** | Bajo | Guardianes certificados, enclavamientos, LOTO obligatorio (Mantto · continuo) |
| Pérdida de ΔP sala sucia | 4 | 3 | **12** | Alto | Mantenimiento de VFD y filtros; alarmas en tiempo real y respuesta < 5 min (HSE/Operación) |
| Vertido a ≥ 40 °C | 3 | 3 | **9** | Moderado | Interlock TCV-ICX; recirculación; auditoría de tendencias (HSE · 7 d) |
| Contacto biológico (descarga) | 4 | 2 | **8** | Moderado | EPP; SOP de cabina; capacitación trimestral (Operación · continuo) |
| Caída/persona-vehículo | 4 | 2 | **8** | Moderado | Segregación peatonal; topes; CCTV y señalética (Seguridad · 15 d) |
| Corte eléctrico prolongado | 3 | 2 | **6** | Moderado | Prueba de black-start trimestral; diésel suficiente 24 h (Eléctrica · 30 d) |

> **Nota de auditoría:** Revisar matriz cada **6 meses** o tras incidentes. Documentar **aceptación del riesgo** por Dirección cuando aplique.

---

## 13.3 HAZOP/What-If (resumen por nodo)

> **Guía:** ¿Qué pasa si… (más/menos presión, temperatura, flujo/ventilación, energía, contaminación)?

| Nodo | Desviación | Causas probables | Consecuencias | Salvaguardas | Recomendaciones |
|---|---|---|---|---|---|
| **N1: Cabezal de vapor / PRV-00** | **+Presión** | Falla PRV, válvula cerrada, purgador bloqueado | Activación SRV, fuga, quemaduras | SRV certificada, PRV con by-pass, manómetros | Prueba anual PRV/SRV; rutina de purgadores y drenajes |
| **N2: Autoclave** | **−Vacío / +Temp** | Bomba sin aceite, sensor fallido | Ciclo inválido, riesgo biológico | Enclavamientos, BI/IC, datalogger | Checklist pre-ciclo; stock de repuestos críticos |
| **N3: Triturador** | **Enclavamiento bypass** | Intervención indebida | Atrapamiento | Llave de seguridad, guardas | Auditoría de bypass; sellos inviolables |
| **N4: Cabina de descarga** | **−Q / −ΔP** | Obstrucción ducto, falla extractor | Olores/bioaerosoles | Alarma ΔP/Q, SOP de pausa | Limpieza ductos; aumento 15–20% capacidad |
| **N5: ICX-01 efluentes** | **T vertido > 40 °C** | Fallo TCV, agua fría insuficiente | Incumplimiento, reclamos | Interlock a 40 °C, recirculación | Bypass de emergencia; sensor redundante |
| **N6: Tablero general** | **Energía 0% / 100%** | Corte UTE / reconexión | Paro, daño equipos | UPS, secuencia black-start | Ensayo trimestral y bitácora |
| **N7: HVAC sala sucia** | **+Olores / +UFC/m³** | Filtros saturados, HEPA leak | Exposición | ΔP monitoreado, plan filtros | PAO/DEHS anual; SOP limpieza SIP/CIP |

> **Nota de auditoría:** Adjuntar **actas HAZOP** (`ANX-HAZOP`) con lista de acciones, responsables y fechas objetivo.

---

## 13.4 Plan de emergencias (roles, gatillos, tiempos objetivo)

**Estructura de respuesta (ICS simplificado):**
- **Líder de Emergencia (LE)**: `[Nombre/rol]`  
- **Seguridad y Evacuación**: coordina rutas/muster point  
- **Brigada contra incendio**: extinción inicial / hidrantes  
- **Primeros Auxilios**: botiquín / soporte básico de vida  
- **Cierre de servicios**: vapor, energía, aire, ICX  
- **Comunicaciones**: 911, autoridad, comunidad, registros

**Gatillos y tiempos objetivo (T=evento):**

| Escenario | Gatillo | T+5 min | T+15 min | Cierre |
|---|---|---|---|---|
| **Fuga de vapor** | Alarma SRV/PRV o visual | Evacuación parcial; cortar línea; EPP térmico | Enfriamiento área; verificación purgadores | Reapertura con permiso escrito |
| **Incendio clase A/B/C** | Detección / humo | Ataque inicial (extintor); 911 si > incipiente | Hidrantes / cortar energía local | Investigación causa / acta |
| **Derrame biológico** | Evento en cabina/sala | Contención; EPP; aislar zona | Limpieza y desinfección; residuos a contenedor | Revisión SOP / reinducción |
| **Pérdida de ΔP/Q** | Alarma crítica | Detener descarga; revisar puertas | Mantenimiento filtros/ventiladores | Registro y prueba de humo |
| **Corte eléctrico** | UTE out / Tablero | Ejecutar black-start | Validar cargas críticas (HVAC, ICX) | Informe de prueba |
| **Vertido ≥ 40 °C** | T ≥ 40 °C | Recirculación; paro de descarga | Diagnóstico TCV/suministro | Reporte HSE/oservaciones OSE |

**Rutas de evacuación y puntos de reunión:** ver plano `ANX-EMERG-RT`.  
**Medios y equipos:** extintores ABC/CO₂, hidrantes, mangueras, **duchas/lavaojos**, **kits de derrames**, botiquín, **detectores**.

> **Nota de auditoría:** Ensayos de **sirenas**, **radios** y **CCTV**; check de **fecha de carga** de extintores e **hidrantes presurizados**.

---

## 13.5 LOTO (Lockout-Tagout) — Procedimiento mínimo

1. **Notificar** a afectados y **detener** el equipo.  
2. **Aislar** todas las energías: eléctrica (seccionador), vapor (válvula), neumática (válvula + purga), potencial (bloqueos mecánicos).  
3. **Bloquear** con **candado** personal y **etiqueta** (nombre/fecha/OT).  
4. **Verificar** ausencia de energía (prueba a cero).  
5. **Trabajar** con permiso y EPP.  
6. **Retirar** herramientas, **reinstalar** guardas.  
7. **Retirar** candados por cada titular, **retirar etiquetas**, **informar** restablecimiento.

**Puntos típicos de aislamiento (por equipo):**  
- Autoclave: seccionador eléctrico, válvula de vapor de línea, bloqueo de puerta (llave).  
- Triturador: seccionador, enclavamiento mecánico, purga de neumática.  
- PRV/ICX: válvulas upstream/downstream, derivaciones.

> **Nota de auditoría:** Lista de **puntos LOTO** por tag y **mapa** de seccionadores (`ANX-LOTO-MAP`). Registro de **permisos de trabajo**.

---

## 13.6 Formación y competencias (matriz)

| Rol | Inducción SST | LOTO | Autoclave (SOP + BI/IC) | Derrames biológicos | Extinción inicial | Primeros auxilios | Black-start | Periodicidad |
|---|:--:|:--:|:--:|:--:|:--:|:--:|:--:|---|
| Operador línea | ✓ | ✓ | ✓ | ✓ | ✓ | — | — | Ingreso + anual |
| Supervisor | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | Ingreso + anual |
| Mantenimiento | ✓ | ✓ | — | — | ✓ | — | ✓ | Ingreso + anual |
| HSE | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | Ingreso + anual |
| Seguridad/Logística | ✓ | — | — | — | ✓ | — | — | Ingreso + anual |
| Conductores | ✓ | — | — | ✓ (cabina) | — | — | — | Ingreso + anual |

> **Nota de auditoría:** Registrar **asistencia**, **evaluaciones** y **vigencias** en Odoo. Mantener **SOP versionados** y firmados.

---

## 13.7 Simulacros semestrales (obligatorios)

**Plan mínimo (2/semestre, 4/año):**
1. **Incendio en casa de máquinas** (con humo frío).  
2. **Fuga de vapor** en riser L2 (sin presión real).  
3. **Derrame biológico** en cabina de descarga.  
4. **Black-start** con pérdida de UTE (arranque secuencial).

**Criterios de aceptación:**
- Evacuación < **3 min** a muster point.  
- **Roles** correctamente asignados; **comunicaciones** efectivas.  
- **Acciones** ejecutadas dentro de **T+5/T+15** según plan.  
- **Lecciones aprendidas** y acciones correctivas **cerradas** ≤ 30 días.

> **Nota de auditoría:** Actas de simulacro (`ANX-SIM-XX`), fotos, cronometraje, lista de asistencia.

---

## 13.8 KPIs y reporte SST

| KPI | Fórmula | Meta |
|---|---|---|
| **TRIFR** (Total Recordable Incident Frequency Rate) | (Incidentes registrables × 200.000) / horas trabajadas | ↓ trimestral |
| **Cumplimiento simulacros** | % simulacros ejecutados vs plan | **100 %** |
| **LOTO correcto** | % OTs con LOTO conforme | **100 %** |
| **Tiempo respuesta emergencias** | Promedio T+5/T+15 | ≤ objetivos |
| **Capacitación vigente** | % personal al día | **≥ 95 %** |

> **Nota de auditoría:** Revisión gerencial **trimestral** (ISO 45001) y **auditoría interna anual** (ISO 19011).

---

## 13.9 Notas de auditoría y evidencias

- **Listados** de EPP, extintores, hidrantes, duchas/lavaojos (códigos, ubicación, vencimientos).  
- **Certificados** de SRV/PRV, manómetros, detectores, sonómetros, calibradores.  
- **Permisos de trabajo**, **LOTO**, **investigaciones** de incidentes, **actas** de simulacros.  
- **Planos** de rutas de evacuación, puntos de reunión y seccionadores.  
- **Backups** de registros (Odoo): **CSV/PDF** con **QR+hash**, retención **≥ 5 años**.

---

## 13.10 Checklist de cierre (Cap. 13)

- ☐ Inventario de peligros validado en campo  
- ☐ Matriz **PGR** aprobada por Dirección y HSE  
- ☐ **HAZOP/What-If** con acciones asignadas y fechas  
- ☐ **Plan de emergencias** con roles, gatillos y tiempos objetivo  
- ☐ **LOTO** implantado y puntos de aislamiento mapeados  
- ☐ **Simulacros semestrales** planificados con criterios de aceptación  
- ☐ **Matriz de formación** actualizada; ≥ 95 % de cobertura  
- ☐ Registros y evidencias en Odoo con **QR+hash** (auditables)

# 14. Trazabilidad y control documental (Odoo **rss_trace**)

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Parámetros fijados:** **On-premise** con **backup diario incremental** + **semanal completo off-site (nube)**; **hash SHA-256** en reportes; **retención ≥ 5 años**.  
> **Normas guía:** ISO **9001** (control documental), ISO **14001** (SGA), ISO **45001** (SST), ISO **17665-1/EN 285** (esterilización a vapor), ISO **19011** (auditorías), ISO **27001** (ISMS), ISO **31000** (riesgos).

---

## Índice de la sección
- **14.1 Arquitectura de solución y alcance**
- **14.2 Modelo de datos mínimo (data model)**
- **14.3 Flujos y permisos (operador → supervisor → auditor)**
- **14.4 Integridad: esquema de **hash SHA-256** y **QR**
- **14.5 Exportaciones CSV/PDF, nomenclatura y retención**
- **14.6 Reglas de bloqueo, BI/IC y No Conformidades (NCR)**
- **14.7 Seguridad de la información (ISMS), backups y restauración**
- **14.8 Monitoreo, tableros y KPIs**
- **14.9 FAT/SAT de software y criterios de aceptación**
- **14.10 Notas de auditoría y checklist de cierre**

---

## 14.1 Arquitectura de solución y alcance

- **Plataforma:** Odoo **on-premise** (hypervisor local o bare-metal) con base de datos dedicada (PostgreSQL), servidor de archivos y **repositorio de adjuntos** (RAID con ECC).  
- **Segmentación de red:** VLAN **OT** (equipos/SCADA/autoclaves) ↔ VLAN **IT** (Odoo/usuarios) mediante **firewall** y listas de control (no acceso directo desde Internet).  
- **Sincronía horaria:** NTP corporativo (requisito para sellos de tiempo coherentes).  
- **Cobertura funcional mínima:** registro de **ciclos**, **recetas**, **BI/IC**, curvas **T/P** (CSV), **evidencias** (PDF/fotos), **muestreos ambientales**, **NCR**, **planes de mantenimiento** y **auditorías**.

> **Nota de auditoría:** Diagrama de red lógico y físico (`ANX-ISMS-RED`), con IPs, puertos, roles y **lista de activos** (CMDB).

---

## 14.2 Modelo de datos mínimo (data model)

**Entidades núcleo (módulo `rss_trace`):**

| Modelo | Campos clave (tipo) | Descripción / Reglas |
|---|---|---|
| **rss.cycle** | `id`, `fecha_inicio` (datetime), `fecha_fin` (datetime), `autoclave_id` (FK), `lote_id` (str), `masa_kg` (float), `receta_id` (FK), `T_max` (°C), `P_max` (bar), `curva_TP_csv` (adjunto), `operador_id` (FK), `supervisor_id` (FK), `resultado_BI` (bool), `resultado_IC` (enum), `hash_sha256` (hex), `qr_payload` (str), `estado` (enum: borrador/aprobado/anulado) | Registro **por ciclo**; al **aprobar** calcula **hash** y genera **PDF** con **QR**; bloqueo si BI/IC fallido. |
| **rss.receta** | `id`, `nombre`, `T_set` (°C), `tiempo_plateau_min` (int), `pre_vacios` (int), `post_vacios` (int), `criterios_aceptacion` (texto), `version` | Ventanas por tipo de carga; control de versiones. |
| **rss.autoclave** | `id`, `codigo`, `fabricante`, `serie`, `presion_trabajo` (bar), `temp_trabajo` (°C), `NR13_doc` (adjunto), `proximo_ensayo` (date), `ubicacion` | Metadatos del equipo; documentación regulatoria. |
| **rss.bi_ic** | `id`, `cycle_id` (FK), `tipo` (BI/IC), `lote_insumo` (str), `resultado` (bool/enum), `evidencia_pdf` (adjunto) | Evidencia de validación del ciclo. |
| **rss.efluente_muestreo** | `id`, `fecha`, `punto`, `caudal_Lh` (float), `T_C` (float), `pH` (float), `SST_mgL`, `DQO_mgL`, `AyG_mgL`, `cadena_custodia_pdf` (adj.) | Conexión al PMSA (Cap. 15); **PME-01**. |
| **rss.ruido_muestreo** | `id`, `fecha`, `punto`, `LAeq_dia`, `LAeq_noche`, `metodo`, `informe_pdf` | Metas Cap. 11; adjunta espectros. |
| **quality.ncr** | `id`, `origen` (ciclo/muestreo/SAT), `descripcion`, `severidad`, `accion_inmediata`, `accion_correctiva`, `responsable`, `fecha_cierre` | Integra con Quality Odoo; trazabilidad de desvíos. |

**Roles y permisos (RBAC mínimo):**

| Rol | Puede crear | Puede aprobar | Puede anular | Ver datos |
|---|---|---:|---:|---|
| **Operador** | Ciclos, BI/IC (borrador) | — | — | Propios |
| **Supervisor** | — | **Ciclos (si BI/IC ok)** | **Sí (con motivo)** | Área |
| **Mantenimiento** | OT, calibraciones | — | — | Equipos |
| **HSE/Ambiente** | Muestreos, PMSA | — | — | Global |
| **Auditor** | — | — | — | **Sólo lectura** (todo) |
| **Administrador** | Configuración | — | — | Todo |

> **Nota de auditoría:** Anexar **matriz RACI** por proceso (`ANX-RACI-TRACE`) y **bitácora de cambios de permisos**.

---

## 14.3 Flujos y permisos (operador → supervisor → auditor)

**Flujo operativo por ciclo:**

flowchart LR

  %% ==== OPERADOR ====
  subgraph OP["Operador"]
    OP0[Operador]
    CARGA[(Carga de datos<br/>+ adjunta CSV T/P + BI/IC)]
    BORR[Guarda (borrador)]
    OP0 --> CARGA --> BORR
  end

  %% ==== SISTEMA ====
  subgraph SYS["Sistema"]
    VALID[Validaciones automáticas<br/>(campos oblig., rangos, adjuntos)]
    HASH[Calcula hash]
    QR[Inserta QR]
    PDF[Genera PDF firmado]
  end

  %% ==== SUPERVISOR ====
  subgraph SUP["Supervisor"]
    SUP0[Supervisor]
    REV[Revisa evidencias]
    DEC{BI/IC = OK<br/>y curva válida?}
    APR[[Aprobar]]
  end

  %% ==== AUDITOR ====
  subgraph AUD["Auditor"]
    AUD0[Auditor]
    LECT[Consulta sólo lectura]
    CRUCE[Cruza contra PMSA y matrices]
  end

  %% ==== FLUJO PRINCIPAL ====
  BORR --> VALID
  VALID --> SUP0
  SUP0 --> REV --> DEC
  DEC -- "Sí" --> APR
  APR --> HASH --> QR --> PDF

  %% Auditoría (sólo lectura)
  AUD0 --> LECT --> CRUCE
  LECT -. lee .-> PDF

  %% Opción de correcciones si no cumple
  DEC -- "No (correcciones)" --> CARGA

  %% ==== ESTILO ====
  classDef system fill:#e6f7ff,stroke:#0077b3,stroke-width:1px;
  classDef decision fill:#fff2cc,stroke:#b38f00,stroke-width:1px;
  classDef approve fill:#e6ffe6,stroke:#267326,stroke-width:1px;

  class VALID,HASH,QR,PDF system;
  class DEC decision;
  class APR approve;


**Reglas:**
- **No se puede aprobar** un ciclo **sin** BI **negativo** y **IC conforme**.  
- Cambio de **receta** o **masa_kg** tras aprobación → obliga **anulación** y **nuevo ciclo**.  
- Toda anulación requiere **motivo** y genera **NCR** automática.

---

## 14.4 Integridad: esquema de **hash SHA-256** y **QR**

**Cadena canónica para hash (orden y separador `|`):**  
`cycle_id | fecha_inicio | fecha_fin | autoclave_id | lote_id | masa_kg | receta_id | T_max | P_max | nombre_archivo_curva | sha256(archivo_curva)`

- **Algoritmo:** `SHA-256` → **hex string** (64 caracteres).  
- **Al aprobar:** se persiste `hash_sha256` y se arma **`qr_payload`** con:  
  - `cycle_id`, `fecha_fin`, `receta`, `masa_kg`, **`hash_sha256`**, **firma supervisor** (nombre+matrícula), versión de documento.  
- **PDF del ciclo:** portada con **QR** (vCard o JSON compacto).  
- **Verificación:** utilitario interno re-calcula hash a partir del **CSV** y campos canónicos; debe **coincidir**.

> **Nota de auditoría (ISMS):** Guardar **función hash** como **código firmado**; registrar **checksum** de binarios y **evidencia** de pruebas (`ANX-ISMS-HASH`).

---

## 14.5 Exportaciones CSV/PDF, nomenclatura y retención

**CSV de ciclo (mínimo):**  
`cycle_id,fecha_inicio,fecha_fin,autoclave_id,lote_id,masa_kg,receta_id,T_max,P_max,sha256_curva,hash_registro,operador,supervisor,estado`

**PDF de ciclo (contenido mínimo):**
- Resumen del ciclo (cabecera), **curva T/P** (gráfico + tabla puntos clave), **BI/IC**, **QR** con `qr_payload`, **hash** visible, firmas Operador/Supervisor.

**Nomenclatura de archivos (repositorio adjuntos):**

ADJUNTAR AQUI LOS ARCHIVOS DEL PROYECTO


**Retención:** **≥ 5 años** (ciclos, BI/IC, PMSA, NCR, SAT/FAT).  
**Inmutabilidad lógica:** impedir sobrescritura de adjuntos aprobados (flag read-only).

> **Nota de auditoría:** Registrar **hash** del **PDF** y del **CSV** (sha256) en metadatos; control de **versiones** (semántico) y **trazabilidad** de cambios.

---

## 14.6 Reglas de bloqueo, BI/IC y No Conformidades (NCR)

- Si `resultado_BI = False` **o** `resultado_IC = "No Conforme"` → **bloquear aprobación**, crear **NCR** y **marcar ciclo** como **no aprobable**.  
- **Curva T/P** fuera de ventana de **receta** (por ejemplo, `T_set ± [ΔT] °C` o `tiempo_plateau < umbral`) → **NCR** automática.  
- **Eventos críticos** (alarma **T vertido ≥ 40 °C**, pérdida de **ΔP** en sala sucia, SRV activada) → **NCR ambiental/seguridad** asociada al período de producción.  
- **Liberación de lote**: sólo para **ciclos aprobados** y **sin NCR abiertas** asociadas al tramo temporal del lote.

> **Nota de auditoría:** Matriz `NCR ↔ Acción Correctiva ↔ Evidencia ↔ Fecha-Cierre`, con **responsables** y **plazos** (Cap. 16).

---

## 14.7 Seguridad de la información (ISMS), backups y restauración

**Controles ISO 27001 (extracto):**
- **Accesos:** autenticación con contraseñas robustas; **MFA** para Admin; **roles** restrictivos (RBAC).  
- **Cifrado:** **en tránsito** (TLS 1.2+) y **en reposo** (FS cifrado + claves custodiadas).  
- **Registro de auditoría:** login, creación/aprobación/anulación de ciclos, descargas de adjuntos, cambios de permisos.  
- **Hardening:** actualizaciones de seguridad, puertos mínimos, antivirus/EDR, anti-malware en adjuntos.  
- **Continuidad:**  
  - **Backups:** **diario incremental** + **semanal completo off-site (nube)**, con **cifrado** y **verificación** de integridad.  
  - **Prueba de restauración:** **mensual** (sandbox), con acta y tiempo medido (**RTO objetivo**: `"[≤ 4 h]"`; **RPO**: `"[≤ 24 h]"`).  
  - **Plan de black-start** coordinado con Cap. 13 (emergencias).

**Gestión de cambios:** cualquier cambio de esquema, reglas o vistas → **CR** con evaluación de impacto, ambiente de prueba y **aprobación** de HSE/Calidad/IT.

> **Nota de auditoría:** Anexar **procedimiento de backup/restore**, evidencias de **últimas 3 restauraciones** y **listado de copias** (`ANX-ISMS-BKP`).

---

## 14.8 Monitoreo, tableros y KPIs

**Tableros (Odoo/BI):**
- **Integridad documental:** % ciclos con **hash verificado**, % PDFs con **QR válido**, **tiempo medio** de aprobación.  
- **Calidad de ciclo:** % BI **negativo**, % IC **conforme**, nº **NCR** por causa.  
- **Ambiental (PMSA):** cumplimiento **T<40 °C** (% tiempo), efluentes dentro de límites, ruido LAeq (día/noche).  
- **Disponibilidad del sistema:** uptime Odoo/DB, tiempo de **restore** de la prueba mensual.

**KPIs sugeridos:**

| KPI | Meta |
|---|---|
| **Hash verificado** | **100 %** de los ciclos aprobados |
| **QR legible** (muestreo mensual) | **100 %** |
| **Aprobación < 24 h** | **≥ 95 %** de ciclos |
| **Fallo BI/IC** | **0 %** a la aprobación (bloqueado) |
| **Restore test exitoso** | **12/12** al año |

---

## 14.9 FAT/SAT de software y criterios de aceptación

**FAT (ambiente controlado):**
- Creación de **10 ciclos** de prueba con curvas sintéticas; verificación de **hash/QR** y exportaciones **CSV/PDF**.  
- Ensayo de **reglas de bloqueo** (BI fallido/IC no conforme).  
- Prueba de **roles** (intento de aprobación por Operador debe fallar).  
- Inyección de **eventos** (T vertido ≥ 40 °C) → **NCR** automática.

**SAT (sitio):**
- Integración con equipos (importación de CSV reales); **tiempo de generación** de PDF < **10 s** por ciclo.  
- **Muestreo**: lectura de **QR** en campo y verificación del **hash** con herramienta independiente.  
- **Backup en vivo** + **restore** en sandbox (último full) con **acta**.  
- **Carga de PMSA** (efluentes/ruido) y cruce en tableros.

**Criterios de aceptación (extracto):**
- **100 %** de ciclos de la muestra con **hash/QR válidos**.  
- **0** aprobaciones con **BI/IC no conformes**.  
- **T<40 °C** registrado y trazado al **PME-01**.  
- **Restore** completado en **≤ `[4 h]`**.

---

## 14.10 Notas de auditoría y checklist de cierre

**Notas de auditoría (evidencias obligatorias):**
- Procedimientos **SOP-TRACE-01/02** (creación/aprobación/anulación de ciclo), **SOP-EXPORT**, **SOP-BKP/RESTORE**.  
- **Actas** de FAT/SAT, **bitácoras** de auditoría (accesos, permisions), **certificados** de calibración de sensores (T/P).  
- **Ensayos** de lectura de **QR** y verificación de **hash** por muestreo.

**Checklist de cierre (Cap. 14):**
- ☐ Modelos `rss_trace` **instalados** y **probados**  
- ☐ **RBAC** aplicado; MFA para Admin; logs activos  
- ☐ **Hash SHA-256** y **QR** operativos; verificador externo disponible  
- ☐ Reglas de **bloqueo** (BI/IC/curva) en producción; **NCR** integradas  
- ☐ **Exportaciones CSV/PDF** con nomenclatura y **retención ≥ 5 años**  
- ☐ **Backups** (diario/semanal) cifrados + **restore mensual** documentado  
- ☐ Tableros **KPIs** en marcha; reportes mensuales a Dirección  
- ☐ FAT/SAT **conformes** y actas adjuntas (`ANX-FAT`, `ANX-SAT`)

---
---

# 15. Plan de Monitoreo y Seguimiento Ambiental (PMSA)

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Alcance:** Efluentes líquidos (descarga a colector), aire interior (sala sucia), olores/bioaerosoles, ruido perimetral, energía/agua, residuos y trazabilidad.  
> **Frecuencias fijadas:** **Mensual (general)** · **Quincenal** para **alto riesgo** (*bioaerosoles en sala sucia, **T** de vertido*, **ruido** si hay reclamos u obras).  
> **Integraciones:** Odoo **rss_trace** (CSV/PDF con **QR + hash**, retención **≥ 5 años**).  
> **Normas guía:** ISO **14001** (SGA), ISO **19011** (auditoría), ISO **27001** (ISMS), ISO **1996/IEC 61672** (ruido), ISO **9613-2** (propagación), **ISO 17665-1 / EN 285** (esterilización a vapor).

---

## 15.1 Tabla PMSA (parámetro → método → frecuencia → meta/umbral → acción → responsable → registro)

> **Nota:** Los límites legales concretos de vertidos/ruido se reemplazarán por resoluciones y decretos aplicables en **Cap. 3** (marco legal). Usar placeholders `"[LIM_xxx]"` hasta su confirmación.

| Eje | Parámetro | Método / Norma de referencia | Frecuencia | Meta / Umbral | Acción correctiva (SLA) | Responsable | Registro (Odoo) |
|---|---|---|---|---|---|---|---|
| **Efluentes** | **Temperatura de vertido** | Sonda PT100/termopozo en línea ICX | **Quincenal** (y continuo en SCADA) | **T < 40 °C** (crítico ≥ 40) | Recirculación + ajuste ICX; reporte HSE en **24 h**; investigación 72 h | Operación / HSE | `pmE01_Tvertido` (CSV + PDF) |
|  | pH | Electrodo calibrado (cadena custodia) | Mensual | `[LIM_pH_MIN–MAX]` | Neutralización/aislamiento de tramo; re-muestreo 24–48 h | HSE | `pmE01_pH` |
|  | SST | Método gravimétrico | Mensual | `[LIM_SST_mg/L]` | Optimizar trampa sólidos/limpieza; plan acción 7 días | HSE | `pmE01_SST` |
|  | DQO | Método estándar (dicromato) | Mensual | `[LIM_DQO_mg/L]` | Investigación fuentes internas; mejora limpieza | HSE | `pmE01_DQO` |
|  | Aceites y Grasas (AyG) | Extracción/gravimetría | Mensual | `[LIM_AyG_mg/L]` | Revisión separador; mantenimiento | HSE/Mantto | `pmE01_AyG` |
|  | Caudal | Medidor ultrasónico / canal Parshall | Mensual (perfil) | Balance masa ±`[x %]` | Verificación instrumentación | Operación | `pmE01_Q` |
| **Aire interior** | **ΔP sala sucia** | Transductor (log 1 min) | **Continuo** (revisión mensual) | −15 Pa (alarma: −10↔−20 Pa) | Ajuste VFD/puertas; RCA si fuera de banda >5% tiempo | Operación | `pmA01_DP` |
|  | **Q captación (descarga/triturador)** | Anemometría/volumetría | Trimestral (mensual si incidentes) | ≥ 4.000 / ≥ 6.000 m³/h | Limpieza filtros/ductos; balanceo | Mantto/HVAC | `pmA01_Q` |
|  | **Bioaerosoles (UFC/m³)** | Impactor/placa (cadena custodia) | **Mensual** (**Quincenal** en alto riesgo) | ≤ P95 de línea base | Limpieza reforzada, cambio filtros; informe 72 h | HSE | `pmA01_BIO` |
|  | Olores (eventos) | Registro de episodios (tabla olor) | Evento / Semanal | **0/mes** | Activar carbón/biofiltro; SOP-OLOR-INC | Operación/HSE | `pmA01_OLR` |
| **Ruido** | LAeq (día/noche) perimetral | Sonómetro Clase 1 + espectro 1/3 octava | **Mensual** (screening); **Trimestral** (completo) · **Quincenal** si reclamos/obras | `[META_DÍA_dB]` / `[META_NOCHE_dB]` | Ajuste horarios, elevar/engrosar barreras, encapsulados | HSE/Ing. | `pmR01_LAeq` |
| **Energía** | kWh/t (proceso total) | Medición eléctrica + producción | Mensual | ↓ tendencial vs base | Revisión OEE, rampas, recuperación calor | Energía/Operación | `pmEN_kWh_t` |
|  | kW pico / factor potencia | Analizador red | Mensual | `[META_kW_PICO]` / `[FP_MIN]` | Secuencia arranques, capacitores | Eléctrica | `pmEN_kW_FP` |
| **Agua** | m³/t (make-up caldera) | Caudalímetro / contadores | Mensual | `[META_m3_t]` | Optimizar blowdown/RO/recuperación | Mantto/Operación | `pmH2O_m3_t` |
| **Ciclos** | % ciclos aprobados | rss_trace (BI/IC + curva) | Mensual | **100 %** | Bloqueos activos; NCR automática | Calidad | `pmQ_ciclos` |
| **Incidentes** | Nº y cierre (SLA) | PGR / Odoo Quality | Mensual | Cierre ≤ 30 días | Comité SST/SGA | HSE/Calidad | `pmNCR_SLA` |

> **Nota de auditoría:** Adjuntar **planillas de campo**, **calibraciones** de instrumentos, fotografías de puntos de muestreo y **cadenas de custodia** (`ANX-PMSA-CAMP`).

---

## 15.2 Disparadores de muestreo extraordinario (adicional al calendario)

- **T vertido ≥ 40 °C** (alarma crítica) → muestreo **inmediato** + **quincenal** hasta 2 meses conforme.  
- **Reclamo vecinal por ruido/olor** → medición **en 48 h** + campaña **quincenal** mientras dure la obra/condición.  
- **ΔP sala sucia fuera de banda > 5 % del tiempo semanal** → **bioaerosoles quincenal** hasta estabilización.  
- **NCR ambiental** (efluente/ruido/olores) → campaña específica definida por HSE.  

> **Registro:** cada disparador genera **NCR** y **plan de acción** con responsable y fecha de cierre.

---

## 15.3 Protocolo de reclamos vecinales (SLA)

1. **Recepción** (canal público / portal / teléfono): *acuso de recibo en **≤ 24 h***.  
2. **Apertura** de **ticket** con **número** y **clasificación** (ruido/olor/tránsito/otros).  
3. **Investigación** preliminar (**≤ 72 h**): revisión de PMSA, cámaras, operación en horario del hecho.  
4. **Acción inmediata** (si aplica): ajuste operativo (horarios, captación, tránsito).  
5. **Medición** objetivo (ruido/olor) **en 48–72 h** según caso.  
6. **Respuesta formal** a la comunidad (**≤ 7 días**) con hallazgos y medidas.  
7. **Cierre** del ticket y publicación de resumen en tablero público (datos no personales).

> **Nota de auditoría:** Conservar **evidencias** (mediciones, fotos, logs) junto al ticket (`ANX-CRC-RECLAMOS`). Indicador **“0 quejas sin responder”**.

---

## 15.4 Publicación de indicadores (transparencia)

**Portal de transparencia (resumen mensual):**
- **Toneladas procesadas/día**, **T vertido (P95)** y **% tiempo T<40 °C**,  
- **LAeq** día/noche promedio perimetral,  
- **Bioaerosoles** (P95 mensual) en sala sucia,  
- **Consumo específico** (**kWh/t**, **m³/t**),  
- **Cumplimiento BI/IC** y **NCR** cerradas/abiertas.

**Formato:** gráfico y tabla; **CSV abierto**; versión y **hash** del reporte.  
**Privacidad:** sin datos personales; ubicación de puntos de monitoreo **generalizada** (no exacta) para seguridad.

---

## 15.5 SOP, responsabilidades y cadenas de custodia

- **SOP-PMSA-EFL**: muestreo de efluentes (botellas, preservación, T°, transporte, laboratorio).  
- **SOP-PMSA-AIRE**: ΔP, Q, bioaerosoles y HEPA (si aplica).  
- **SOP-PMSA-RUIDO**: metodología, alturas, tiempos de integración, espectros 1/3 octava, meteorología.  
- **SOP-OLOR-INC**: gestión de episodios de olor.  
- **SOP-ISMS-TRACE**: carga de resultados en Odoo (CSV/PDF), **hash**, **QR**, backups.  

**Roles:**
- **HSE/Ambiente:** programa, coordina laboratorio, valida informes.  
- **Operación:** apoyo a campo, checklists y datos de proceso.  
- **Mantenimiento:** instrumentación, calibraciones y correcciones.  
- **Calidad:** custodia de documentos, NCR y auditoría interna.  
- **TI/ISMS:** integridad, respaldo y restauración.

> **Nota de auditoría:** Versionado de SOP; **firmas**; **vigencia**. Subir **últimos 12 meses** de informes verificables.

---

## 15.6 Tablero y KPIs PMSA

| KPI | Fórmula | Meta |
|---|---|---|
| **Cumplimiento calendario PMSA** | campañas ejecutadas / planificadas | **100 %** |
| **% tiempo T<40 °C** | min. dentro de meta / min. totales | **≥ 99 %** |
| **LAeq conforme (día/noche)** | puntos conformes / total | **≥ 95 %** |
| **Bioaerosoles conformes** | campañas conformes / total | **≥ 95 %** |
| **Cierre de NCR** | cerradas ≤ 30 días / total | **≥ 90 %** |
| **Publicación mensual** | informes publicados / 12 | **12/12** |

---

## 15.7 Checklist de cierre (Cap. 15)

- ☐ Tabla PMSA cargada con **métodos, metas, SLA y responsables**  
- ☐ Disparadores de **campañas extraordinarias** definidos y probados  
- ☐ **Protocolo de reclamos vecinales** operativo (SLA 24–72 h–7 d)  
- ☐ **Publicación** de indicadores (CSV abierto + hash) activa  
- ☐ **SOP** y **cadenas de custodia** vigentes; **calibraciones** al día  
- ☐ KPIs en tablero; **backups** verificados; evidencia **QR + hash** en Odoo

---
---

# 16. Matriz de cumplimiento y compromisos

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Normas y referencias:** ISO **14040/14044**, **9001**, **14001**, **45001**, **50001**, **17665-1/EN 285**, **27001**, **19011**, **31000**; **Decreto 643/1992**, **253/1979**, **222/1982**, **143/2012**, **281/016**, **Ley 17.852 (2004)**; **NR-13** (referencia técnica).  
> **Alcance:** Requisitos regulatorios y corporativos aplicables al proyecto **Planta de Tratamiento de Residuos Hospitalarios – Polticor S.A.** (autoclave + trituración, 3 líneas iniciales; escalable 5–7).

---

## 16.1 Matriz requisito → evidencia → KPI → responsable → sección/anexo

> **Leyenda de estado:** 🟢 Cumplido · 🟡 En curso · 🔴 Pendiente · ⚪ No aplica  
> **Nota:** Cuando existan *placeholders* (p. ej., `[META_DÍA_dB]`, `[DECRETO_VERTIDOS]`) deberán sustituirse al cierre legal/técnico.

| Área / Requisito | Evidencia exigible | **KPI de control** | Dueño del control | Sección / Anexo | Estado |
|---|---|---|---|---|:--:|
| **Licenciamiento ambiental (DINACEA)** — **EsIA** + **Clasificación A** | EsIA completo, avisos, tasas, resolución | Hitos del Gantt cumplidos (**100 %**) | Dirección de Proyecto / Ambiental | Cap. 3 · `ANX-ESIA` | 🟡 |
| **RSS** — Gestión/Tratamiento (**Decr. 643/1992** y específicos RSS) | SOP recepción/descarga; ciclos con BI/IC; trazabilidad QR | % ciclos aprobados **100 %** | Operaciones / Calidad | Caps. 5, 12, 14 · `ANX-SOP-RSS` | 🟢 |
| **Vertidos** — **Decr. 253/1979** (+ **222/1982**) | Plano de puntos de muestreo; ICX; registros **T<40 °C**; informes mensuales | % tiempo **T<40 °C ≥ 99 %**; parámetros dentro de límite **≥ 95 %** | HSE / Mantto | Caps. 8–9, 15 · `ANX-PMSA-EFL` | 🟡 |
| **Ruido** — **Decr. 143/2012** / **281/016** | Línea base y campañas; metas IM `[META_DÍA_dB]/[META_NOCHE_dB]` | Puntos conformes **≥ 95 %**; 0 reclamos sin respuesta | HSE / Ingeniería | Caps. 11, 15 · `ANX-RUIDO-LB`, `ANX-IM-METAS` | 🟡 |
| **Esterilización** — **ISO 17665-1 / EN 285** | Recetas validadas; BI/IC; curvas T/P; FAT/SAT | BI negativo **100 %**; IC conforme **100 %** | Calidad / Operaciones | Caps. 8, 12, 14 · `ANX-QUAL-EST` | 🟢 |
| **Calidad** — **ISO 9001** | Procedimientos, control documental, NCR | Cierre NCR ≤ 30 días **≥ 90 %** | Calidad | Caps. 14, 16 · `ANX-QMS` | 🟡 |
| **Ambiental** — **ISO 14001** | Matriz de aspectos/impactos; PMSA; objetivos | Cumplimiento PMSA **100 %** | HSE | Caps. 7, 15 · `ANX-EMS` | 🟡 |
| **SST** — **ISO 45001** | PGR; matriz de riesgos; LOTO; simulacros | Simulacros ejecutados **100 %**; cobertura capacitación **≥ 95 %** | SST / HSE | Cap. 13 · `ANX-SST`, `ANX-LOTO-MAP`, `ANX-SIM-XX` | 🟢 |
| **Energía** — **ISO 50001** | ENMS; KPIs kWh/t; plan de eficiencia | Tendencia a la baja vs. línea base | Energía / Operaciones | Caps. 7, 8, 15 · `ANX-ENMS` | 🟡 |
| **ISMS** — **ISO 27001** & **Auditorías** — **ISO 19011** | Control de accesos; backups; pruebas de restauración | Restore mensual **12/12**; logs revisados **100 %** | TI / ISMS | Cap. 14 · `ANX-ISMS-BKP`, `ANX-ISMS-RED` | 🟢 |
| **Riesgos** — **ISO 31000** | Matriz PGR aprobada; revisión semestral | Revisiones en fecha **100 %** | Dirección / HSE | Caps. 13, 16 · `ANX-RISK` | 🟢 |
| **Recipientes a presión** — **NR-13** (ref.) + exigencias locales | Prontuario; SRV/PRV certificados; plan de inspección | Calibraciones al día **100 %** | Mantto / Proveedor | Caps. 3, 13 · `ANX-NR13` | 🟡 |
| **HVAC/bioaerosoles/olores** | ΔP −15 Pa; Q captación; bioaerosoles | ΔP dentro de banda **≥ 95 %**; 0 episodios olor | Mantto/HVAC / HSE | Cap. 10, 15 · `ANX-HVAC-VERIF` | 🟢 |
| **Logística** (tránsito, seguridad) | Circuito unidireccional; cabina; SOP | Permanencia P90 **≤ 30 min**; puntualidad **≥ 95 %** | Logística / Seguridad | Cap. 12 · `ANX-VIAL-01/02`, `ANX-CAB-DESC` | 🟢 |
| **Transparencia y comunidad** | Portal de indicadores; protocolo de reclamos | 0 quejas sin responder; 12/12 publicaciones | Dirección / HSE / TI | Cap. 15 · `ANX-CRC-RECLAMOS` | 🟡 |

> **Notas de auditoría (matriz):**  
> 1) Vincular cada KPI a un **tablero** y un **informe** (CSV/PDF con **QR + hash**).  
> 2) Mantener **evidencias trazables** (códigos de documento, versión, fecha, firma).  
> 3) Actualizar **estado** tras cada auditoría interna o hito del Gantt.

---

## 16.2 Plan de verificación — Auditorías internas (ISO 19011)

| Auditoría | Objeto | Alcance | Periodicidad | Equipo auditor | Evidencias |
|---|---|---|---|---|---|
| **A-01 Legal & Licenciamiento** | EsIA, compromisos DINACEA, permisos IM/OSE | Matriz legal, hitos, resoluciones | **Trimestral** | Legal / Ambiental (externo opc.) | Lista chequeo + acta |
| **A-02 Procesos de esterilización** | Recetas, ciclos, BI/IC, T/P | Muestra estadística por línea | **Mensual** | Calidad / Operaciones | Informe con trazas |
| **A-03 Efluentes** | ICX, T<40 °C, PMSA efluentes | Parámetros, cadena custodia | **Mensual** | HSE | Reporte laboratorio |
| **A-04 Ruido** | LAeq día/noche, medidas correctivas | Puntos perimetrales | **Trimestral** (quincenal si reclamos) | HSE / Acústica | Espectros 1/3 octava |
| **A-05 HVAC/Bioaerosoles** | ΔP, Q, HEPA (si aplica), UFC/m³ | Sala sucia/cabina | **Mensual** | HSE / Mantto | Ensayos humo/PAO |
| **A-06 SST & PGR** | LOTO, simulacros, permisos | Talleres y sala máquinas | **Trimestral** | SST / Auditor interno | Actas + fotos |
| **A-07 ISMS** | Backups, restore, accesos | Odoo/DB/adjuntos | **Mensual** (restore) | TI/ISMS | Log + acta restore |
| **A-08 ENMS** | kWh/t, picos, FP | Tablero energía | **Mensual** | Energía | Informe tendencia |
| **A-09 Proveedores críticos** | Calibraciones, SRV/PRV, BI/IC | Lista críticos | **Semestral** | Compras / Calidad | Certificados |

**Cierre de hallazgos:**  
- **Menor:** 30 días · **Mayor:** 15 días · **Crítico:** 72 h (plan inmediato).  
- **Seguimiento:** comité mensual de cumplimiento (Dirección, HSE, Calidad, Operaciones, TI).

---

## 16.3 Semáforo de brechas (diagnóstico y acciones)

| Ítem / Brecha | Impacto | Estado | Acción de cierre | Dueño | Plazo |
|---|---|:--:|---|---|---|
| **Metas IM de ruido** (`[META_DÍA_dB]/[META_NOCHE_dB]`) | Legal / Comunidad | 🔴 | Gestionar zonificación IM, fijar metas y actualizar Cap. 11/15 | HSE | `T0+15 d` |
| **Potencia UTE disponible** | Diseño eléctrico | 🟡 | Confirmación UTE; dimensionar trafo/tableros | Ingeniería Eléctrica | `T0+20 d` |
| **Superficies/coords. del ZIP** (si no cerradas) | Trazabilidad | 🟡 | Cargar datos definitivos y planos firmados | Dirección de Proyecto | `T0+10 d` |
| **Procedimientos comunitarios (portal)** | Transparencia | 🟡 | Publicación mensual con hash + CSV | TI / HSE | `T0+30 d` |
| **Certificados SRV/PRV iniciales** | Seguridad/proceso | 🟡 | Recepción y archivo en `ANX-NR13` | Mantto | `T0+7 d` |
| **ICX — validación térmica completa** | Vertidos | 🟡 | SAT con pruebas en sitio (T<40 °C) | HSE / Mantto | `T0+5 d` |

> **Nota:** `T0` = fecha de aprobación del presente capítulo por Dirección.

---

## 16.4 Plan de cierre (compromisos y responsables)

1. **Legal/IM:** cerrar metas de ruido y zonificación; **actualizar Cap. 11/15**.  
   - Responsable: **HSE** · Plazo: `T0+15 d` · Evidencia: `ANX-IM-METAS`.  
2. **Eléctrica/UTE:** confirmar potencia; **memoria eléctrica y protecciones**.  
   - Responsable: **Ing. Eléctrica** · Plazo: `T0+20 d` · Evidencia: `ANX-EL-MEM`.  
3. **Documental ZIP:** superficies y coordenadas definitivas en **Cap. 2**; **planos firmados**.  
   - Responsable: **Dirección de Proyecto** · Plazo: `T0+10 d` · Evidencia: `ANX-PLN-IMPL`.  
4. **NR-13/SRV-PRV:** recepción de certificados y **calibraciones**.  
   - Responsable: **Mantto** · Plazo: `T0+7 d` · Evidencia: `ANX-NR13`.  
5. **ICX/Vertidos:** completar **SAT ICX** con **T<40 °C** registrado.  
   - Responsable: **HSE/Mantto** · Plazo: `T0+5 d` · Evidencia: `pmE01_Tvertido`.  
6. **Transparencia/Portal:** publicar indicadores mensuales (**12/12**).  
   - Responsable: **TI/HSE** · Plazo: `T0+30 d` · Evidencia: `ANX-CRC-RECLAMOS`.

---

## 16.5 Gobernanza de compromisos (KPI + RACI)

**RACI resumido (extracto):**

| Tema | R (Responsable) | A (Aprueba) | C (Consulta) | I (Informa) |
|---|---|---|---|---|
| EsIA / Clasificación A | Ambiental | Dirección | Legal | Comunidad |
| Vertidos / ICX | HSE | Dirección | Mantto, Operación | OSE/IM |
| Ruido | HSE | Dirección | Acústica, Operación | Comunidad |
| Esterilización (17665/EN 285) | Calidad | Dirección | Operación | Auditor |
| ISMS (27001) | TI/ISMS | Dirección | Calidad | Todos |
| ENMS (50001) | Energía | Dirección | Operación | Auditor |

**KPIs de gobernanza (mensuales):**  
- % **compromisos** dentro de plazo (**≥ 90 %**).  
- % **hallazgos** cerrados ≤ 30 días (**≥ 90 %**).  
- **Semáforo**: ítems 🔴 **= 0**.

---

## 16.6 Notas de auditoría y checklist de cierre

**Notas de auditoría**
- Mantener **evidencias** por requisito con **código, versión y firma**.  
- Todas las tablas exportables a **CSV/PDF** con **QR + hash** (Cap. 14).  
- Integrar **bitácora de cambios** y **control de accesos** (ISMS).

**Checklist (Cap. 16)**
- ☐ Matriz requisito→evidencia→KPI→dueño **completa**  
- ☐ Plan de auditorías internas **aprobado** (ISO 19011)  
- ☐ Semáforo de brechas **actualizado** y con **plazos**  
- ☐ Compromisos asignados (**RACI**) y **KPIs** de gobernanza activos  
- ☐ Evidencias subidas a Odoo (CSV/PDF con **QR + hash**) y **backups verificados**

---
---

# 17. Cronograma, FAT/SAT, entregables y plan de cierre (Horizonte 180 días)

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Alcance:** Ruta de licenciamiento y montaje para **Planta RSS – Polticor S.A.** (3 líneas **autoclave 950×3000 mm; 165 kg/ciclo; ~45 min**; **2×530 kgv/h N+1**; escalable a 5–7).  
> **Premisas:** OEE **75 %** (normal) / **100 %** (extraordinario); **24/7**; efluente **templado < 40 °C** a colector; **Odoo on-prem** con **hash/QR** y **backup diario + semanal off-site**.  
> **Normas guía:** ISO **14040/14044**, **9001/14001/45001/50001**, **17665-1/EN 285**, **27001/19011/31000**; **Decretos 643/1992, 253/1979, 222/1982, 143/2012, 281/016**, **Ley 17.852**; **NR-13** (referencia técnica).

---

## 17.1 Gantt textual (180 días) con hitos y dependencias

> **Leyenda:** `D0` = fecha de inicio del programa. Duraciones indicativas; ajustar al cronograma contractual.  
> **Dependencias:** FS (finish-to-start), SS (start-to-start), FF (finish-to-finish).

| ID | Fase / Entregable | Janela temporal | Duración | Dependencias | Responsable |
|---|---|---|---:|---|---|
| G1 | **Kick-off**, plan maestro, matriz RACI | D0–D5 | 1 sem | — | Dirección de Proyecto |
| G2 | **EsIA** (redacción + anexos) | D0–D35 | 5 sem | G1 SS | Ambiental / Legal |
| G3 | **Ingreso EsIA** a DINACEA (Clasificación A) | D36 | 1 día | G2 FS | Ambiental |
| G4 | **Rondas de respuesta DINACEA** (RFI/RFQ) | D37–D90 | 8 sem | G3 SS | Ambiental / Ingeniería |
| G5 | **Trámite IM (uso del suelo/obra)** | D20–D70 | 8 sem | G1 SS | Ingeniería / IM |
| G6 | **Convenios OSE/UTE** (puntos/medidores/potencia) | D20–D75 | 9 sem | G1 SS; G5 SS | Ingeniería / Utilidades |
| G7 | **FAT** de equipos principales (autoclaves, calderas, ICX) | D40–D70 | 5 sem | G4 SS | Proveedor / QA |
| G8 | **Obra civil** (fundaciones, naves, drenajes) | D45–D115 | 10 sem | G5 SS | Contratista / Civil |
| G9 | **Montaje mecánico** (piano vapor, autoclaves, triturador) | D80–D140 | 9 sem | G7 FS; G8 SS | Mecánica |
| G10| **Montaje eléctrico & control** (tableros, instrumentación, SCADA) | D90–D150 | 9 sem | G8 SS | Eléctrica / Control |
| G11| **HVAC/extracción** (cabina y sala sucia) | D90–D145 | 8 sem | G8 SS | HVAC |
| G12| **Odoo on-prem** + `rss_trace` + ISMS | D60–D110 | 7 sem | G1 SS | TI/ISMS / Calidad |
| G13| **Líneas base**: ruido perimetral / PMSA de referencia | D95–D115 | 3 sem | G11 SS | HSE / Acústica |
| G14| **Pre-comisionado** (purgas, presión, secuencia black-start) | D130–D150 | 3 sem | G9, G10, G11 FS | Ingeniería /
Operaciones |
| G15| **SAT** (pruebas en sitio) | D151–D165 | 2 sem | G14 FS | QA / HSE / Proveedor |
| G16| **Cierre documental** (as-built, OMM, certificados) | D160–D175 | 2 sem | G15 SS | Calidad / Ingeniería |
| G17| **Resolución DINACEA** (prevista) | D150–D175 | 4 sem | G4 FS (envío completo) | Ambiental |
| G18| **Inicio de operación** (rampa controlada) | D176–D180 | 1 sem | G15, G16, G17 FS | Dirección / Operaciones |

**Camino crítico (referencial):** G2 → G3 → G4 → (G7||G8) → G9 → G14 → G15 → G16 → G17 → G18.  
**Hitos formales:** `H1` Ingreso EsIA (G3) · `H2` FAT conforme (G7) · `H3` Obra civil lista (G8) · `H4` Pre-comisionado OK (G14) · `H5` SAT conforme (G15) · `H6` Resolución DINACEA (G17) · `H7` Inicio operación (G18).

> **Nota de auditoría (dependencias):** documentar **actas de hito** y evidencia (fotos, protocolos, firmas). Cargar en Odoo con **QR+hash** y control de versiones.

---

## 17.2 FAT (Factory Acceptance Test) — Criterios y alcance

**Equipos:** autoclaves (3), calderas 530 kgv/h (N+1), ICX/intercambiador, trituradores, instrumentos críticos (PT100, manovacuómetros, caudalímetros).

**Pruebas mínimas FAT:**
- **Integridad mecánica**: pruebas de estanqueidad/hidrostática (proveedor) y certificados de materiales/accesorios (válvulas conforme **NBR ISO 14313. 
 o si necesario ASME B16.34 / ISO 4126 / NBR**).  
- **Seguridad funcional**: enclavamientos puerta-presión, PRV/SRV, presostatos y control de nivel.  
- **Ciclo sintético**: vacío/calor; exportación **CSV** de curva **T/P**; verificación de formato para `rss_trace`.  
- **Documental**: OMM, listas de repuestos críticos, certificaciones de calibración, prontuario **NR-13** (referencia), check-list de empaques/purgadores.

**Criterios de aceptación FAT (Go/No-Go):**
- 100 % de **enclavamientos** probados y conformes.  
- **CSV** con marcas de tiempo y variables requeridas por `rss_trace`.  
- Certificados y calibraciones **vigentes** (fechas y trazabilidad).

> **Salida FAT:** Acta firmada por proveedor y QA con **no conformidades** (si las hubiera) y plan de corrección previo al despacho.

---

## 17.3 SAT (Site Acceptance Test) — Criterios, métodos y formatos

**Áreas:** proceso (autoclaves + trituración), vapor/ICX, HVAC/cabina, eléctrico/control, trazabilidad Odoo, ambiental (ruido/efluentes).

**Batería de pruebas SAT:**

1) **Curvas T/P por receta y línea**  
   - 3 ciclos por autoclave (cargas representativas baja/media/alta densidad).  
   - **Aceptación**: cumplimiento ventana de receta; **BI negativo** y **IC conforme** en cada ciclo; exportaciones **CSV/PDF** con **hash** y **QR** generados por `rss_trace`.  

2) **Efluentes — ICX**  
   - Medición **continua** de **T** y muestreo **quincenal** según PMSA.  
   - **Aceptación**: **T vertido < 40 °C** (100 % del tiempo durante SAT); punto de muestreo con cadena de custodia y reporte de laboratorio sin anomalías.

3) **HVAC/cabina**  
   - Ensayo de **ΔP** (sala sucia −15 Pa, banda −10↔−20 Pa) y **Q captación** (≥ 4.000 m³/h en descarga; ≥ 6.000 m³/h en triturador).  
   - **Aceptación**: ΔP y Q dentro de banda; prueba de humo visual y registro fotográfico.

4) **Ruido perimetral**  
   - Medición **día/noche** con sonómetro clase 1; espectro 1/3 octava.  
   - **Aceptación**: **LAeq** ≤ metas `[META_DÍA_dB]/[META_NOCHE_dB]` o implementación inmediata de mitigaciones (barreras/encapsulados) y re-medición.

5) **Seguridad/energía**  
   - **Black-start**: arranque de grupos y secuencia de cargas (calderas/HVAC/ICX) sin disparos.  
   - **Aceptación**: tiempos dentro del plan, protecciones y selectividad correctas.

6) **Odoo `rss_trace` / ISMS**  
   - Ingesta de **CSV** reales → **hash SHA-256** y **QR** en PDF; reglas de **bloqueo** (BI/IC fallido) y **NCR** automática.  
   - **Backups**: verificación de **backup diario** y **restore mensual** (ejecutar un restore piloto durante SAT).  
   - **Aceptación**: 100 % de ciclos de la muestra con **hash/QR válidos**; **restore** exitoso ≤ `"[4 h]"`.

> **Registro SAT:** protocolos firmados, archivos **CSV/PDF** con **hash** y **photos** de evidencias. Cargar a Odoo con **retención ≥ 5 años**.

---

## 17.4 Entregables por fase (paquete documental)

| Fase | Entregables mínimos |
|---|---|
| **EsIA / Licencias** | EsIA completo, anexos legales, respuestas a DINACEA, oficios IM/OSE/UTE, matriz legal actualizada |
| **FAT** | Actas FAT, certificados (PRV/SRV/manómetros/caudalímetros), OMM, lista de repuestos, prontuario NR-13 (referencia) |
| **Obra/ Montaje** | Planos **as-built**, isométricos y MTO, pruebas de presión, checklists mecánicos/eléctricos/HVAC, matrices de soldadura |
| **Pre-comisionado** | Purgas y soplados, pruebas de estanqueidad, selectividad eléctrica, pruebas de ΔP/Q en HVAC, plan black-start |
| **SAT** | Protocolos T/P + BI/IC, PMSA de arranque, ruido perimetral, ICX T<40 °C, evidencias `rss_trace` (CSV/PDF con hash/QR), acta de cierre |
| **Cierre** | Manual de operación, SOP autorizados (LOTO, emergencias, PMSA), plan de mantenimiento, contratos de calibración, matriz de cumplimiento (Cap. 16) cerrada |

---

## 17.5 Hitos de aceptación y criterios Go/No-Go

| Hito | Criterio Go/No-Go | Evidencia |
|---|---|---|
| **H1 Ingreso EsIA** | Expediente admitido; tasas pagas | Acuse DINACEA |
| **H2 FAT Conforme** | 100 % enclavamientos y CSV exportables | Acta FAT + listados |
| **H3 Obra lista** | Civil al 100 %, accesos y utilidades operativas | Acta de pre-recepción |
| **H4 Pre-comisionado OK** | Purgas/PRV/ΔP/Q verificados | Checklists firmados |
| **H5 SAT Conforme** | Ítems 1–6 de §17.3 cumplidos | Acta SAT + anexos |
| **H6 Resolución DINACEA** | **Clasificación A** otorgada | Resolución |
| **H7 Inicio operación** | SOP vigentes, PMSA en marcha, ISMS activo | Acta de arranque |

---

## 17.6 Pruebas de restauración (Odoo/ISMS) — Plan y calendario

- **Backup**: **diario incremental** + **semanal completo off-site** (cifrado).  
- **Restore test**: **mensual** en sandbox con **RTO objetivo ≤ `[4 h]`** y validación de **integridad de hash/QR** en 5 ciclos de muestra.  
- **Criterio de aceptación**: **12/12** pruebas/año exitosas; actas y tiempos registrados.

> **Nota de auditoría:** anexar guías `SOP-BKP/RESTORE`, bitácoras, y lista de copias disponibles (`ANX-ISMS-BKP`).

---

## 17.7 Riesgos de cronograma y mitigaciones

| Riesgo | Impacto | Mitigación | Disparador / Plan B |
|---|---|---|---|
| Observaciones extensas de DINACEA | Demora en `H6` | Pre-respuestas tipo, mesa técnica quincenal | Reasignar redacción; fast-track de anexos |
| Potencia UTE no confirmada | Retraso G10/G14 | Gestión temprana; alternativa con generadores temporales | SAT parcial con cargas limitadas |
| Lead time de válvulas/sensores | Retraso G9/G14 | Stock mínimo crítico, **PO** anticipada | Reprogramar por frentes; swaps temporales |
| Ruido > metas | No conformidad `H5` | Barreras y encapsulados prefabricados | Re-medición 48–72 h |
| ΔP/Q HVAC fuera de banda | No conformidad `H5` | Sobredimensionar 15–20 %; filtros en stock | Ajuste VFD y limpieza inmediata |
| ICX no alcanza T<40 °C | No conformidad `H5` | Intercambiador mayor + recirculación | Bypass de emergencia y plan de obra menor |

---

## 17.8 Notas de auditoría y checklist de cierre (Cap. 17)

**Notas de auditoría**
- Mantener **matriz de dependencias** actualizada con **FS/SS/FF**.  
- Publicar **curva S** de progreso físico/financiero con evidencia fotográfica.  
- Todos los **hitos** deben tener **acta firmada** y **carga en Odoo** (CSV/PDF con **QR+hash**).

**Checklist**
- ☐ Gantt 180 días aprobado por Dirección (con camino crítico)  
- ☐ Plantillas de **acta de hito** y **protocolos FAT/SAT** cargadas  
- ☐ Calendario de **restore mensual** en ISMS (RTO ≤ `[4 h]`)  
- ☐ Plan de riesgos con **triggers** y **Plan B** por ítem  
- ☐ Entregables y criterios **Go/No-Go** definidos por fase

---
---

# 18. Relacionamiento comunitario y apertura de datos

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Alcance:** Canales de diálogo con comunidad, protocolo de reclamos con **SLA**, **comité comunitario trimestral**, y **portal de transparencia** con apertura de datos para investigación (universidades MERCOSUR/otros países).  
> **Normas guía:** ISO **14001** (comunicación y partes interesadas), ISO **9001** (control documental), ISO **19011** (auditorías), ISO **27001** (gobernanza de datos), ISO **31000** (riesgos).

---

## Índice de la sección
- **18.1 Canales de contacto y SLA de reclamos**
- **18.2 Comité comunitario trimestral**
- **18.3 Portal de transparencia: indicadores “casi en tiempo real”**
- **18.4 Especificación técnica de datos abiertos (formatos, integridad, versionado)**
- **18.5 Privacidad, anonimización y ética**
- **18.6 Gobernanza de datos y RACI**
- **18.7 Notas de auditoría y checklist de cierre**

---

## 18.1 Canales de contacto y SLA de reclamos

**Canales habilitados (señalizados con QR en accesos y barrio):**

| Canal | Dirección / Medio | Horario | SLA acuse | SLA respuesta | Observaciones |
|---|---|---|---|---|---|
| **Correo electrónico** | **info@polticor.com** (asunto: “Reclamo Comunidad”) | 24/7 | ≤ **24 h** | ≤ **7 días** con medidas | Respuesta trazable y auditable |
| **Teléfono** | **0800 1444\*** | Lun–Vie 08–18 h | Inmediato | ≤ **7 días** | Deriva a ticket interno |
| **Formulario web** | Link en **QR** (portal comunidad) | 24/7 | ≤ **24 h** | ≤ **7 días** | Permite adjuntar fotos/audio |
| **Presencial** | Portería Camino Oncativo 3154 | Lun–Vie 08–18 h | Inmediato | ≤ **7 días** | Acta firmada de recepción |

**Proceso resumido (trazable en Odoo/Calidad):**
1) **Registro** (ticket con Nº, categoría: ruido/olor/tránsito/otros).  
2) **Acuse** ≤ 24 h.  
3) **Investigación** ≤ 72 h (PMSA, CCTV, operación).  
4) **Medición** objetiva 48–72 h si aplica (ruido/olor).  
5) **Respuesta** formal ≤ 7 días (hallazgos y medidas).  
6) **Cierre** y **publicación** de resumen (datos no personales) en el portal.

> **Nota de auditoría:** Mantener **bitácora** de reclamos y **evidencias** (mediciones, fotos, logs) por ticket; indicador “**0 quejas sin responder**”.

---

## 18.2 Comité comunitario trimestral

**Objetivo:** Instancia de diálogo, revisión de indicadores y planes de mejora.

| Ítem | Detalle |
|---|---|
| **Periodicidad** | **Trimestral** (marzo, junio, septiembre, diciembre) |
| **Composición** | 2 representantes vecinales, 1 de la IM (invitado), 1 del MA/DINACEA (invitado), 1 de Polticor (Dirección), 1 HSE, 1 Operaciones |
| **Agenda tipo** | (i) Indicadores del trimestre, (ii) reclamos y respuestas, (iii) obras/ruidos programados, (iv) compromisos y plazos |
| **Minutas** | Publicación en portal (PDF con **hash**), compromisos con responsable/plazo |
| **Mecanismo de seguimiento** | Tablero público “Compromisos Comunidad” con estado 🟢🟡🔴 |

> **Nota de auditoría:** Actas firmadas y archivadas ≥ 5 años. Código de documento y versión.

---

## 18.3 Portal de transparencia: indicadores “casi en tiempo real”

**Frecuencias de actualización (objetivo):**
- **Tons/día (t/d):** actualización **diaria** (00:30) + parcial **cada hora**.  
- **Temperatura de vertido (T vertido):** **cada 15 min** (promedio móvil 15 min).  
- **Ruido perímetro (LAeq):** **cada 15 min** (puntos perimetrales).  
- **Cumplimiento BI/IC:** **cada hora** (acumulado del día y rolling 24 h).

**Indicadores publicados (resumen portal):**

| Código | Indicador | Definición | Meta | Unidad | Latencia | Fuente |
|---|---|---|---|---:|---|---|
| **I1** | **t/d procesadas** | Suma de **masa_kg** de **ciclos aprobados** por fecha | Transparencia (sin meta regulatoria) | t/d | ≤ 1 h | Odoo `rss_trace` |
| **I2** | **T vertido** | P95 y % tiempo **T < 40 °C** (rolling 24 h) | **T < 40 °C** | °C / % | 15 min | ICX / SCADA |
| **I3** | **LAeq perímetro** | LAeq día/noche por punto (rolling 15 min) | `[META_DÍA_dB]/[META_NOCHE_dB]` | dB(A) | 15 min | Red sonómetro Clase 1 |
| **I4** | **BI/IC conformidad** | % ciclos con **BI negativo** y **IC conforme** (día / rolling 24 h) | **100 %** | % | ≤ 1 h | Odoo `rss_trace` |

**Presentación:** gráfica + tabla + **CSV abierto**; cada reporte con **hash SHA-256** y **QR**.

> **Nota:** Se publican también **eventos** (trabajos ruidosos programados), con ventana horaria y medidas de mitigación.

---

## 18.4 Especificación técnica de datos abiertos (formatos, integridad, versionado)

**Formatos:** **CSV** y **JSON** (UTF-8).  
**Catálogo de datasets (mínimo):**
- `produccion_diaria.csv` → `fecha, toneladas, ciclos_aprobados, hash_fuente`  
- `efluente_T_15min.csv` → `timestamp, T_prom_15min, pct_t_bajo_40C_24h, estado`  
- `ruido_LAeq_15min.csv` → `timestamp, punto_id, LAeq_15, estado_meteo`  
- `calidad_ciclo_1h.csv` → `timestamp, ciclos_ok, ciclos_totales, pct_ok`

**Integridad:**  
- Cada archivo incluye **columna `hash_fuente`** (sha256 del CSV/PDF de origen cuando aplique).  
- Publicación con **manifiesto**: `dataset_id`, `versión` (semántica), `fecha_publicación`, `sha256`.

**Versionado y retención:**  
- Versiones **mensuales** (snapshot) + **rolling 90 días** para “casi tiempo real”.  
- Retención histórica **≥ 5 años** (almacenamiento frío).

**Disponibilidad:**  
- Portal web con navegación y **API** (rate-limit europeo estándar).  
- Términos de uso y **licencia** visibles (ver §18.5).

> **Nota de auditoría:** Probar verificación de **hash** con herramienta independiente y dejar instructivo público.

---

## 18.5 Privacidad, anonimización y ética

- **No** se publican **datos personales** ni información que identifique a personas, domicilios particulares o empresas clientes.  
- Los puntos de monitoreo se informan con **IDs** y ubicación **generalizada** (no coordenadas exactas).  
- **Política de anonimización**: remoción de campos sensibles, agregación temporal (15 min / día) y uso de **umbrales** para evitar reidentificación.  
- **Licencias de datos:**  
  - **Indicadores y gráficos:** **CC BY 4.0** (atribución requerida).  
  - **Datasets tabulares** (si se consideran bases de datos con derechos *sui generis*): **ODbL 1.0** o **CC BY 4.0** (definir en comité de datos).  
- **Derechos de terceros:** no se publica material protegido sin autorización.  
- **Canal de reporte** de hallazgos en datos (responsible disclosure): `"[correo_datos@polticor.com]"`.

> **Nota de auditoría:** Incluir en el portal la **política de privacidad** y el **DPIA** (evaluación de impacto de protección de datos) cuando aplique.

---

## 18.6 Gobernanza de datos y RACI

**Roles:**

| Rol | Responsabilidades | Persona/Área |
|---|---|---|
| **Data Owner** | Aprobación de datasets y licencias; prioridades de publicación | Dirección |
| **Data Steward** | Calidad de datos, diccionarios, versionado, catálogos | TI/ISMS |
| **Custodio Ambiental** | Valida I2 (T vertido) e I3 (ruido); PMSA y cadenas de custodia | HSE |
| **Custodio Operaciones** | Valida I1 (t/d) e I4 (BI/IC); consistencia con `rss_trace` | Operaciones/Calidad |
| **Comité de Datos** | Define cambios, evalúa riesgos y excepciones | Dirección + HSE + TI |

**RACI por indicador:**

| Indicador | R | A | C | I |
|---|---|---|---|---|
| I1 t/d | Operaciones | Dirección | Calidad | Comunidad |
| I2 T vertido | HSE | Dirección | Mantto | Comunidad / OSE |
| I3 LAeq | HSE | Dirección | Acústica | Comunidad / IM |
| I4 BI/IC | Calidad | Dirección | Operaciones | Comunidad |

**KPIs de gobernanza (mensuales):**
- **Publicaciones en fecha**: 12/12 al año.  
- **Integridad**: 100 % datasets con **hash** y **manifiesto**.  
- **Tickets** de reclamos respondidos en **≤ 7 días**: **100 %**.

---

## 18.7 Notas de auditoría y checklist de cierre

**Notas de auditoría**
- Verificar **SLA** de reclamos (acuse ≤ 24 h; respuesta ≤ 7 días).  
- Confirmar **actas** y **minutas** del **comité comunitario** (trimestral).  
- Validar que portal publique **I1–I4** con **CSV+JSON**, **hash** y licencia.  
- Revisar **catálogo de datos**, **diccionarios** y **manifiestos** de versiones.  
- Asegurar **backups** y **restore** conforme a Cap. 14 (ISMS).

**Checklist (Cap. 18)**
- ☐ Canales activos (mail/teléfono/QR/form) y señalización en sitio  
- ☐ Protocolo de reclamos operando con **SLA** y tablero de estado  
- ☐ Comité comunitario convocado y con minutas públicas  
- ☐ Portal de transparencia funcional con **I1–I4** y datasets descargables  
- ☐ Licencia de datos y política de privacidad publicadas  
- ☐ Gobernanza (RACI) definida; **Data Steward** asignado  
- ☐ Evidencias en Odoo con **QR + hash** y retención ≥ 5 años

---
---

# 19. Anexos, planimetría y control de versiones

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Objeto:** Estructura de **anexos técnicos y legales**, codificación, **control de versiones** y **checklist de completitud** previo al ingreso a **DINACEA**.  
> **Normas guía:** ISO **9001** (control documental), ISO **14001** (SGA), ISO **45001** (SST), ISO **50001** (energía), ISO **27001** (ISMS), ISO **19011** (auditorías), ISO **14040/14044** (metodología), ISO **17665-1/EN 285** (esterilización).

---

## 19.1 Estructura y codificación de anexos

> **Reglas de codificación:**  
> - **ANX-PLN-*** (planimetría/diseño) · **ANX-SOP-*** (procedimientos) · **ANX-LEG-*** (marco legal) · **ANX-ISMS-*** (seguridad de información).  
> - Otros prefijos complementarios: **ANX-PMSA-*** (monitoreo), **ANX-RUIDO-***, **ANX-QUAL-*** (calidad/esterilización), **ANX-NR13**, **ANX-ENMS**, **ANX-FAT/SAT**, **ANX-OMM**.  
> - Cada anexo con **código**, **título**, **versión**, **fecha**, **responsable**, **firma** (digital), **hash** y **QR** (ver Cap. 14).

### A) Planimetría y diseño (**ANX-PLN-***)
- **ANX-PLN-IMPL** — Implantación general: polígono del predio, coordenadas, retiros, cotas y accesos.  
- **ANX-PLN-ARQ** — Arquitectura: **plantas, cortes, fachadas** por nave/sector; superficies (predio/naves).  
- **ANX-PLN-VIAL** — Circulación: circuito **unidireccional**, playa de descarga, **slots 15 min**, señalética y velocidades (≤ 10 km/h).  
- **ANX-PLN-MEC** — **Piano de vapor**: isométricos, **PRV**, separadores, purgadores, **ICX** y **punto de muestreo**; **MTO**.  
- **ANX-PLN-EL** — Eléctrico: unifilares, selectividad, **puesta a tierra**, grupos y **black-start**; estimación de demanda (UTE).  
- **ANX-PLN-HVAC** — HVAC/Extracción: **ΔP** objetivo (−15 Pa), **Q** por punto (descarga/triturador), filtros **MERV-13/HEPA**, silenciadores.  
- **ANX-PLN-EFL** — Efluentes: drenajes, **ICX**, retorno de condensado, **templado < 40 °C**, puntos de muestreo.  
- **ANX-PLN-ACUST** — Acústica: ubicación de barreras/encapsulados y **puntos de medición** perimetral (día/noche).  
- **ANX-PLN-SEG** — Seguridad: rutas de evacuación, LOTO, hidrantes/extinción, duchas/lavaojos.  
- **ANX-PLN-CAB** — **Cabina de descarga**: captación localizada, ventilación y limpieza de contenedores.

### B) Procedimientos (SOP) (**ANX-SOP-***)
- **ANX-SOP-RSS-REC** — Recepción/descarga de RSS (QR, pesaje, portal gamma, criterios de rechazo).  
- **ANX-SOP-RSS-AUT** — Autoclave: operación, recetas, **BI/IC**, curva **T/P**, criterios de aceptación.  
- **ANX-SOP-TRIT** — Trituración: operación/limpieza, CIP/SIP si aplica.  
- **ANX-SOP-PMSA-EFL** — Muestreos de efluentes (pH, T, SST, DQO, AyG) y cadena de custodia.  
- **ANX-SOP-PMSA-AIRE** — ΔP, caudales, **bioaerosoles/olores** (métodos, frecuencias).  
- **ANX-SOP-PMSA-RUIDO** — Medición perimetral (metodología, espectros 1/3 de octava).  
- **ANX-SOP-EMER** — Emergencias: incendio, derrames, bioaerosoles, fallo de vacío/presión; roles y tiempos.  
- **ANX-SOP-LOTO** — Bloqueo y etiquetado (energías peligrosas).  
- **ANX-SOP-TRACE-01/02** — Odoo **rss_trace**: creación/aprobación de ciclos, **hash/QR**, exportación CSV/PDF.  
- **ANX-SOP-BKP-RESTORE** — Backups diarios/semanales y prueba de **restauración mensual** (ISMS).

### C) Marco legal y licenciamiento (**ANX-LEG-***)
- **ANX-LEG-ESIA** — EsIA completo, anexos y **matriz legal**.  
- **ANX-LEG-DINACEA** — Ingresos, oficios, **respuestas**, **resolución** de Clasificación A.  
- **ANX-LEG-IM** — Certificado de **uso del suelo** y permisos de obra/actividad.  
- **ANX-LEG-OSE-UTE** — Conexiones, **potencia UTE** (confirmación), condiciones de vertido a colector.  
- **ANX-LEG-IMPO** — Compendio: **Decreto 643/1992**, **253/1979**, **222/1982**, **143/2012**, **281/016**, **Ley 17.852** (texto vigente).

### D) Seguridad de la información (**ANX-ISMS-***)
- **ANX-ISMS-RED** — Arquitectura de red (OT/IT), firewall, NTP, control de accesos.  
- **ANX-ISMS-BKP** — Política de respaldo, bitácoras y **actas de restauración** (12/12).  
- **ANX-ISMS-HASH** — Especificación de **hash SHA-256** y validador externo.  
- **ANX-ISMS-ACL** — Matriz **RBAC**, listas de usuarios, auditoría de accesos.

### E) Otros anexos técnicos
- **ANX-QUAL-EST** — Validaciones de esterilización (BI/IC), curvas **T/P**, criterios **ISO 17665-1/EN 285**.  
- **ANX-NR13** — Prontuario de recipientes a presión, **PRV/SRV**, calibraciones y ensayos.  
- **ANX-PMSA-EFL/AIRE/RUIDO** — Reportes PMSA (mensual/quincenal) con cadena de custodia.  
- **ANX-RUIDO-LB/OP** — **Línea base** y campañas operativas (LAeq día/noche).  
- **ANX-ENMS** — Plan energético (kWh/t, picos, FP) y medidas de eficiencia (recuperación de calor).  
- **ANX-FAT / ANX-SAT** — Protocolos, actas y evidencias (CSV/PDF con **hash/QR**).  
- **ANX-OMM** — Manuales de operación/mantenimiento y lista de repuestos críticos.

> **Nota de auditoría:** Todo anexo deberá incluir **código**, **versión**, **fecha**, **responsable**, **firma** (digital), **hash** y **QR**; y estar **referenciado** en el cuerpo del documento (sección y tabla de evidencias).

---

## 19.2 Tabla de control de versiones (documento principal)

| Versión | Fecha | Responsable | Secciones afectadas | Descripción de cambios | Aprobación |
|---|---|---|---|---|---|
| **V0.1** | `"[AAAA-MM-DD]"` | `"[Nombre]"` | 1–5 | Borrador inicial: Portada, Metodológica, Índice, Marco legal preliminar | Dirección (borrador) |
| **V0.2** | `"[AAAA-MM-DD]"` | `"[Nombre]"` | 6–12 | Proceso y límites, capacidad, HVAC, ruido, logística | Dirección (borrador) |
| **V0.3** | `"[AAAA-MM-DD]"` | `"[Nombre]"` | 13–18 | SST/PGR, trazabilidad Odoo, PMSA, comunidad/datos | Dirección (borrador) |
| **V1.0** | `"[AAAA-MM-DD]"` | `"[Nombre]"` | Todo | Consolidado para **ingreso DINACEA** (con EsIA adjunto) | Dirección / Legal |
| **V1.1** | `"[AAAA-MM-DD]"` | `"[Nombre]"` | 3, 7, 11, 15 | Ajustes por observaciones DINACEA e IM | Dirección / Ambiental |
| **V2.0** | `"[AAAA-MM-DD]"` | `"[Nombre]"` | 8–10, 14, 17 | Inclusión de **as-built**, resultados **SAT** y cierre de brechas | Dirección / Operaciones |

### 19.2.1 Control de versiones por anexo (plantilla)
> Para cada anexo se mantiene una tabla equivalente con: **Versión**, **Fecha**, **Responsable**, **Cambios**, **Aprobación**.  
> **Ejemplo:** `ANX-PLN-MEC` v1.0 — agrega PRV serie XYZ y punto de muestreo ICX (Cap. 9).

---

## 19.3 Checklist de completitud (previo a ingreso DINACEA)

> **Marcar**: ☑ Cumple · ☐ Pendiente · ☐ N/A

### A) Integridad del documento
- ☐ **Portada** completa (proyecto, **RUT**, contactos, ubicación, objetivo **Clasificación A**).  
- ☐ **Declaración metodológica** ISO 14040/14044 (meta/alcance, LCI, LCIA, interpretación).  
- ☐ **Índice** (niveles 1–2) y paginación consistente.  
- ☐ **Justificación de español internacional neutro** (MERCOSUR).

### B) Marco legal y licenciamiento
- ☐ **EsIA** adjunto (ANX-LEG-ESIA) con matriz legal.  
- ☐ Referencias a **Decretos** 643/1992, 253/1979, 222/1982, 143/2012, 281/016 y **Ley 17.852**.  
- ☐ Trámites **IM**, **OSE**/**UTE** en curso con acuses (`ANX-LEG-IM`, `ANX-LEG-OSE-UTE`).

### C) Ingeniería y operación
- ☐ **Proceso y límites** (sin pre-triturado; **portal gamma**, básculas I/E).  
- ☐ **Memoria de cálculo** (vapor/agua/eléctrica) y **N+1** validado.  
- ☐ **Servicios auxiliares**: **piano**, **ICX** con **T<40 °C**, retorno de condensado.  
- ☐ **HVAC/extracción** con **ΔP −15 Pa** y caudales objetivo; ruidos mitigados.  
- ☐ **Logística**: circuito unidireccional, **cabina de descarga**, permanencia ≤ 30 min.

### D) Gestión ambiental y SST
- ☐ **Matriz de aspectos/impactos** (ISO 14001) y **PMSA** (ANX-PMSA-*).  
- ☐ **Ruido**: línea base y metas; plan de medición perimetral (ANX-RUIDO-LB/OP).  
- ☐ **SST** (ISO 45001): **PGR**, **LOTO**, **simulacros** (ANX-SOP-EMER/LOTO).  

### E) Trazabilidad y datos
- ☐ **Odoo on-prem** con `rss_trace`: **hash SHA-256**, **QR**, reglas de **bloqueo** BI/IC.  
- ☐ **Backups** diarios/semanales y **restore mensual** (ANX-ISMS-BKP).  
- ☐ **Portal de transparencia** definido (I1–I4) y política de **privacidad/licencias**.

### F) Planimetría y anexos
- ☐ **ANX-PLN-IMPL/ARQ/VIAL/MEC/EL/HVAC/EFL/ACUST/SEG/CAB** **completos** y firmados.  
- ☐ **ANX-FAT / ANX-SAT**: protocolos y formatos listos.  
- ☐ **ANX-NR13**: certificados PRV/SRV, calibraciones, prontuario.  
- ☐ **ANX-OMM**: manuales y **repuestos críticos**.

### G) Control documental
- ☐ Tablas de **control de versiones** (doc y anexos) actualizadas.  
- ☐ **Firmas** (digitales), **hash/QR** en PDFs y **códigos** de documento.  
- ☐ **Lista maestra** de documentos y **trazabilidad** secciones ↔ anexos.

> **Nota de auditoría (ingreso DINACEA):** Consolidar **acta de revisión final** con firma de Dirección, Ambiental, Ingeniería y Legal; generar **paquete de envío** con **índice de anexos**, **checksums** y **comprobante** de lectura.

---

## 19.4 Reglas de archivado y retención

- **Retención mínima:** **≥ 5 años** para documentos regulatorios, PMSA, FAT/SAT y SOP; **≥ 10 años** para prontuarios y certificados críticos (NR-13).  
- **Repositorio**: Odoo/Documentos con **nomenclatura estandarizada** y carpetas por **código de anexo**.  
- **Inmutabilidad lógica**: anexos **aprobados** en modo **solo lectura**; cambios solo por **nueva versión**.

---

## 19.5 Notas finales de auditoría
- Verificar concordancia entre **cuerpo del documento** y **anexos** (título, versión, fecha).  
- Chequear **coherencia numérica** (superficies, caudales, potencias) en planos y memorias.  
- Mantener **registro de control de cambios** y **trazabilidad** a decisiones (minutas).  
- Asegurar que todos los PDFs cuenten con **hash** y **QR** y que su verificación esté **documentada**.

---
---

# 20. Resumen ejecutivo para autoridades (DINACEA)

> **Control documental**  
> **Versión:** `V1.0` · **Fecha:** `"[AAAA-MM-DD]"` · **Responsable:** `"[Nombre, matrícula]"`  
> **Ámbito:** Solicitud de **Clasificación Ambiental A** con **EsIA adjunto** para la **Planta de Tratamiento de Residuos Hospitalarios – Polticor S.A.** (Camino Oncativo 3154, Padrón 60790, Montevideo).  
> **Metodología:** alineada a **ISO 14040/14044** (meta/alcance, LCI, LCIA, interpretación) e integrada con el EsIA. Gestión bajo **ISO 9001/14001/45001/50001/27001/19011/31000** y requisitos técnicos **ISO 17665-1 / EN 285**.  

---

## 20.1 Síntesis del proyecto
**Titular:** Polticor S.A. · **Tecnología:** desinfección por **autoclave de vapor** + **trituración** (sin pre-triturado).  
**Configuración inicial:** **3 líneas** (autoclave 950×3000 mm; **165 kg/ciclo**; ~**45 min/ciclo**), **escalable** a **5–7**.  
**Capacidad:** **360 t/mes** (régimen normal, OEE 75 %) y hasta **475 t/mes** (extraordinario, OEE 100 %).  
**Vapor de proceso:** **2 × 530 kgv/h (N+1)** con calderas **eléctricas modulares** (cero combustión).  
**Efluentes:** sistema interno con **intercambiador** (recuperación térmica) y **templado < 40 °C** antes de descarga a **colector** (punto de muestreo y trazabilidad).  
**Energía y respaldo:** secuenciación de cargas, **black-start** con grupos electrógenos, **FV** para oficinas y servicios auxiliares (offset diurno).  
**Logística y control de ingreso:** **portal gamma** en portón, básculas de **ingreso/egreso**, circuito unidireccional, **cabina de descarga** con extracción dedicada.  

> **Principio ambiental clave:** **cero combustión** en tratamiento; la única emisión normal es **vapor de agua** gestionado por extracción y condensación.  

---

## 20.2 Diseño de mitigaciones y desempeño ambiental
- **Efluentes líquidos:** **ICX** para **templado < 40 °C**; monitoreo de **T, pH, SST, DQO, AyG** con cadena de custodia; plan de **muestreo mensual** (quincenal para alto riesgo).  
- **Aire interior y bioaerosoles/olores:** **depresión** sala sucia (**ΔP = −15 Pa**), **captación localizada** (≥ 4.000 m³/h descarga; ≥ 6.000 m³/h triturador), filtración **MERV-13** y **HEPA** en puntos críticos; monitoreo **mensual/quincenal** de bioaerosoles.  
- **Ruido:** **barreras perimetrales** y **encapsulados** en fuentes; gestión horaria, velocidad **≤ 10 km/h** y control de ralentí; metas en línea de propiedad (**día/noche**) ajustables a zonificación IM.  
- **Energía (ISO 50001):** **ENMS** con indicadores **kWh/t** y picos; **recuperación de calor** del condensado para **precalentar** agua de alimentación; arranques escalonados para aplanar demanda.  
- **Resiliencia operativa:** filosofía **N+1** (vapor), rutas de contingencia, simulacros **semestrales** (incendio, derrames, falla de vacío/presión, corte eléctrico).  

---

## 20.3 Trazabilidad, transparencia y gobernanza de datos
- **Trazabilidad por lote/ciclo:** **Odoo on-prem** + módulo `rss_trace` (datos de ciclo, **BI/IC**, curvas **T/P**), **QR** y **hash SHA-256** en informes **CSV/PDF**, retención **≥ 5 años**.  
- **Portal de transparencia (datos abiertos):** publicación casi en tiempo real de **t/d procesadas**, **T de vertido**, **LAeq** perimetral y **conformidad BI/IC** (CSV/JSON con **hash** y licencia abierta).  
- **Comunidad:** **comité comunitario trimestral**, protocolo de **reclamos** con **SLA** (acuse ≤ 24 h; respuesta ≤ 7 días) y tablero de compromisos público.  

---

## 20.4 Cumplimiento regulatorio (marco de referencia)
- **EsIA + Clasificación A (DINACEA)** como ruta de licenciamiento.  
- Vertidos a colector: **Decretos 253/1979 y 222/1982** (parámetros y condiciones).  
- Gestión de RSS: **Decreto 643/1992** (aplicable según alcance).  
- **Ruido:** **Decreto 143/2012** y **281/016** (metodología/criterios, metas por zonificación IM).  
- **Recipientes a presión:** **NR-13** como **referencia técnica** (prontuarios, PRV/SRV, ensayos) en convergencia con exigencias locales.  

> **Notas de auditoría:** las referencias legales se consolidan en **ANX-LEG-IMPO**; cada requisito se vincula a una **evidencia** y **KPI** (ver Matriz de Cumplimiento, Cap. 16).

---

## 20.5 Compromisos medibles (extracto)

| Compromiso | Indicador / Meta | Frecuencia | Responsable |
|---|---|---|---|
| **Efluente templado** | **T vertido < 40 °C**; **≥ 99 %** del tiempo | Continuo (SCADA) + **Quincenal** (PMSA) | HSE / Mantto |
| **Conformidad de ciclos** | **100 %** con **BI negativo** e **IC conforme** | Diario (operación) + Mensual (auditoría) | Calidad / Operación |
| **Ruido perimetral** | LAeq **≤ meta día/noche** (IM) | Mensual (screening) / Trimestral (completo) | HSE / Acústica |
| **Bioaerosoles** | P95 **≤ línea base**; ΔP en banda **−10↔−20 Pa** | Mensual / Quincenal (alto riesgo) | HSE / HVAC |
| **Energía específica** | Tendencia **↓ kWh/t** (ENMS) | Mensual | Energía / Operación |
| **Trazabilidad documental** | **100 %** ciclos con **CSV/PDF + QR + hash** | Mensual | TI/ISMS / Calidad |
| **Backups/restore** | **12/12** restores mensuales exitosos | Mensual | TI/ISMS |
| **Comunidad** | **0** quejas sin responder; publicaciones **12/12** | Mensual | HSE / TI |

---

## 20.6 Cronograma de hitos (horizonte 180 días)

| Hito | Ventana | Criterio de aceptación |
|---|---|---|
| **Ingreso EsIA a DINACEA** | D+30–35 | Acuse y expediente admitido |
| **FAT equipos** (autoclaves, calderas, ICX) | D+40–70 | Enclavamientos OK; exportación **CSV** válida |
| **Obra civil lista** | D+115 | Acta de pre-recepción |
| **Pre-comisionado** (vapor/eléctrica/HVAC) | D+130–150 | Purgas/PRV; ΔP/Q en banda |
| **SAT** (sitio) | D+151–165 | **T/P + BI/IC**, **T vertido < 40 °C**, **LAeq** conforme; `rss_trace` operativo |
| **Resolución DINACEA** | D+150–175 | Clasificación **A** otorgada |
| **Inicio de operación** | D+176–180 | SOP vigentes; PMSA en marcha; ISMS validado |

> **Camino crítico resumido:** EsIA → FAT/Obra → Pre-comisionado → SAT → Resolución DINACEA → Arranque.

---

## 20.7 Conclusión para decisión
El proyecto **aplica mejores prácticas internacionales** (ISO 14040/14044; 9001/14001/45001/50001/27001/19011/31000) y **estándares técnicos** de esterilización (**ISO 17665-1 / EN 285**), con **cero combustión**, **emisiones limitadas a vapor de agua**, **efluentes templados < 40 °C**, **barreras acústicas**, **trazabilidad digital con QR y hash**, **recuperación de calor** e **indicadores públicos** en un **portal de transparencia**.  
Se garantizan **controles verificables**, **auditorías internas** y **gobernanza de datos**. Con estas salvaguardas, Polticor S.A. solicita la **Clasificación Ambiental A** para su planta de tratamiento de RSS en Montevideo.

> **Nota de auditoría (remisión):** Evidencias, SOP, planimetría, matrices y protocolos FAT/SAT detallados en **Anexos codificados (ANX-PLN-*, ANX-SOP-*, ANX-LEG-*, ANX-ISMS-*)** y capítulos 14–19 del documento.

