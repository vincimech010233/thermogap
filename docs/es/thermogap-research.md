# ThermoGap — informe de investigación y decisión de desarrollo

**Fecha de corte:** 15 de octubre de 2026. **Ámbito:** revisión documental pública y tres casos completamente sintéticos. **Estado:** investigación terminada; desarrollo de MVP no justificado todavía. No se ha accedido a instalaciones industriales, datos operativos privados ni servicios externos autenticados.

## Resumen ejecutivo

**Decisión — RESEARCH FURTHER.** Hay una necesidad industrial fundada: el calor residual existe en gases de combustión, corrientes de proceso, refrigeración, aire comprimido y otros focos; su aprovechamiento puede reducir combustible cuando hay sumidero simultáneo compatible, transferencia practicable y ahorro superior al coste. Sin embargo, las capacidades propuestas como diferenciadoras ya están sustancialmente cubiertas por EMB3Rs, OpenPinch, Aspen Energy Analyzer y productos de integración/gestión energética. No hay evidencia de demanda pagadora o de una brecha funcional exclusiva para ThermoGap. Una prueba sintética sirve para comprobar balances y reglas, pero no establece rendimiento industrial ni tracción comercial.

La oportunidad más defendible para investigar no es “encontrar matches” en general. Es evaluar si un flujo de trabajo local, trazable y orientado a decisión puede aportar algo medible en incertidumbre de datos, explicación de inviabilidad y valor de la medición adicional, comparado con herramientas abiertas y comerciales. Esas ventajas siguen siendo **HYPOTHESIS**, no una afirmación de novedad.

### Aprendizaje transversal

- **LEARNING:** calor residual bruto no equivale a calor útil ni a ahorro energético. **EVIDENCE:** el máximo del Caso A cae de 292,6 kW disponibles en la fuente a 167,2 kW entregables, por el límite de demanda; en los otros casos, temperatura y horario limitan el uso. **IMPACT:** la selección de receptores y la coincidencia temporal son necesarias antes de reportar ahorro. **CONFIDENCE:** alta para los balances sintéticos; media para la aplicabilidad de mercado. **CARRY_FORWARD:** reportar separadamente fuente, calor transferido, calor entregado y energía comprada evitada. **UNRESOLVED:** datos de plantas reales y medición de carga parcial.
- **LEARNING:** matching, integración por periodos, bombas de calor, HEN y análisis tecnoeconómico ya aparecen en productos/proyectos identificables. **EVIDENCE:** documentación pública de EMB3Rs y OpenPinch. No se confirmó que OpenPinch modele despacho dinámico de TES. **IMPACT:** no es defendible atribuir originalidad a las categorías verificadas; el almacenamiento exige una comparación específica. **CONFIDENCE:** alta para funciones declaradas; media para calidad y límites en producción. **CARRY_FORWARD:** definir benchmark con casos y tareas comunes. **UNRESOLVED:** rendimiento comparado, despacho TES, adopción, soporte y condiciones comerciales.
- **LEARNING:** un elevador térmico puede servir al proceso y consumir electricidad sustancial; puede empeorar la cuenta económica. **EVIDENCE:** Caso B conserva el primer principio y da un escenario con ahorro operativo negativo. **IMPACT:** decidir por coste marginal y emisiones del suministro, no por el COP aislado ni el calor recuperado. **CONFIDENCE:** alta para ecuaciones y escenarios; baja para condiciones de compra reales. **CARRY_FORWARD:** mapas de rendimiento por temperaturas/carga y vectores separados de combustible y electricidad. **UNRESOLVED:** oferta de equipos, curvas a carga parcial e instalación para un caso concreto.

## A. Panorama científico e industrial

### Qué se entiende por calor residual

El informe JRC aclara la contabilidad europea de calor/frío residual y documenta fuentes, tecnologías y aplicaciones. El aprovechamiento in situ es una opción de eficiencia; la definición administrativa para ciertos objetivos de energía no debe confundirse con la definición termodinámica de calor disponible ni con un ahorro acreditado. La estimación DOE de que un 20–50 % de energía industrial puede perderse como calor es una cifra agregada de contexto —no una fracción recuperable universal ni potencial de ThermoGap—. La fuente subraya barreras como materiales y mantenimiento. [DOE, “Waste Heat Recovery Basics”](https://www.energy.gov/cmei/ito/waste-heat-recovery-basics) (página vigente, consultada 2026-10-15); [JRC, *Quantifying the role of waste heat in the EU energy system*](https://publications.jrc.ec.europa.eu/repository/handle/JRC126383) (2021; alcance de contabilidad y anexos sectoriales).

La oportunidad depende de cinco filtros acumulativos: (1) caudal y entalpía que se pueden retirar sin perjudicar producto o equipo; (2) temperatura útil tras diferencias mínimas de aproximación; (3) coincidencia temporal y continuidad; (4) intercambiabilidad segura y pérdidas/auxiliares; (5) coste de integración inferior al valor de energía efectivamente desplazada. La energía térmica es de baja calidad frente a electricidad: su exergía depende de la temperatura, y la generación eléctrica desde calor de baja temperatura puede tener límites de eficiencia severos.

### Fuentes y usos candidatos

La matriz es una guía de *screening*, no un catálogo de temperaturas universales. “Evidencia” enlaza evidencia sectorial o tecnológica y se señalan sus límites. Las temperaturas y deberes concretos se tienen que medir por planta.

| Fuente | Posible sumidero/uso | Tecnología de recuperación | Restricciones principales | Evaluación inicial |
|---|---|---|---|---|
| Hornos, calderas y gases de combustión | Aire de combustión/carga, agua de alimentación, procesos próximos, secado; vapor o red térmica solo si coincide el nivel | Recuperador, economizador, precalentador, regenerador; bomba de calor si nivel bajo | Corrosión/condensación por punto de rocío, ensuciamiento, emisiones, tiro/contrapresión, materiales, control del horno y producto | **Alta oportunidad potencial, no presumible**; el ahorro de combustible se prioriza dentro del proceso cuando no crea nueva demanda. DOE lista recuperación y precalentamiento como opciones; el caso siderúrgico IED advierte que ciertos gases pueden condensar y corroer. [DOE proceso térmico](https://www.energy.gov/cmei/ito/process-heating-systems); [JRC BREF hierro/acero](https://bureau-industrial-transformation.jrc.ec.europa.eu/sites/default/files/2019-11/IS_Adopted_03_2012.pdf) (2012). |
| Compresores de aire | Agua de proceso, lavado, agua de caldera, aire de reposición o calefacción | Recuperación de enfriador de aceite/aftercooler, conductos o intercambiador | La temperatura es normalmente moderada; no produce vapor directamente en el caso típico; la contrapresión y ventilación del compresor importan; exceso térmico estacional | **Buena intraplanta con demanda coincidente**. DOE reporta 80–93 % de entrada eléctrica convertida en calor y recuperación de 50–90 % disponible en diseños apropiados, como regla técnica del sourcebook, no garantía de proyecto. [DOE, *Improving Compressed Air System Performance*, Fact Sheet 9](https://www.energy.gov/sites/default/files/2016/03/f30/Improving%20Compressed%20Air%20Sourcebook%20version%203.pdf) (2016). |
| Refrigeración, condensadores y chillers | Lavado, agua caliente, calefacción, bomba de calor a proceso o distrito | Desuperheater, condensador de recuperación, bomba de calor | El calor rechazado varía con carga y temperaturas; no comprometer refrigeración; simultaneidad con demanda y diferencia de temperaturas | **Buena candidata en alimento/bebida y frío industrial** cuando existe carga térmica todo el año. El recurso es de baja temperatura sin elevación. |
| Secaderos/estufas y producto caliente | Aire de entrada, etapas previas, calentamiento de agua o secado en cascada | Recuperador gas-gas, bomba de calor, recirculación, almacenamiento | Humedad/partículas, contaminación, riesgo de incendio, humedad del producto y perfil por lote | **Hipótesis de ingeniería**; posibilidades y nivel térmico deben derivarse de humedad, temperaturas y operación de cada línea. |
| Química/petroquímica | Precalentamiento de alimentación, reboilers, vapor, precalentamiento de agua | Pinch/HEN, intercambiador, integración de bomba de calor, vapor de proceso | Seguridad de proceso, materiales y compatibilidad, múltiples presiones/fases, restricciones de operación y paradas | **Candidato de ingeniería especializada**, sin ranking de mercado en este estudio; integración y HEN son prácticas existentes. No sustituir simulador/ingeniero de proceso con screening automático. |
| Metal, acero, vidrio, cemento y cerámica | Carga/aire/combustión, secado, agua y calor de baja/mediana T; ORC solo caso adecuado | Recuperadores de gases/sólidos, almacenamiento, bomba de calor, ciclo de potencia | Temperaturas muy altas hacen atractivo recuperar internamente, pero polvo, escoria, operación discontinua, corrosión y materiales son duros; el calor de alta T puede tener valor de proceso más alto que usarlo en agua | **Candidato sectorial respaldado por materiales DOE/JRC**, pero no prueba de factibilidad por planta ni potencial económico. |
| Alimentos, bebidas, lácteos y pasteurización | Agua caliente, lavado/CIP, pasteurización, evaporación, secado y precalentamiento | Recuperador, bomba de calor, acumulación | Higiene, separación de circuitos, calidad de agua/producto, carga de limpieza por lotes, control de temperatura | **Candidato para investigación**, no mercado validado. Forman et al. ubica demanda alimentaria en rangos bajos/medios; IEA documenta aplicaciones de bomba de calor en alimentos/lácteos. |
| Papel y pulpa | Agua de proceso, aire, secado y vapor de menor nivel | Recuperación de condensado y gases, HEN, bombas de calor, almacenamiento | Grandes caudales y secado, humedad, ensuciamiento, producción continua y parada cara | **Candidato a estudio sectorial**, no cuantificado aquí ni validado con planta. |
| Textil y lavandería | Lavado, teñido, secado, agua de proceso | Recuperadores líquido-líquido, bombas de calor y almacenamiento | Química/contaminación, demanda por lote, temperatura de proceso y limpieza | **Hipótesis de ingeniería** condicionada; la evidencia recopilada aquí no cuantifica potencial por subproceso. |
| Agua residual industrial/municipal | Agua caliente de proceso, lavado, red de calor | Intercambiador sumergido/de canal, intercambiador aislado más bomba de calor | Sólidos, fouling, corrosión, higiene, variabilidad, permisos, limpieza y coste de bombeo | **Hipótesis de ingeniería:** fuente baja en temperatura puede alimentar una bomba de calor, pero aquí no se cuantifica disponibilidad; revisar sólidos, fouling, higiene y permisos. |
| Centros de datos/electrónica | Calefacción de baja T, agua caliente, red local; procesos con bomba de calor | Intercambiadores de líquido, bombas de calor, redes | Temperatura de refrigerante, renovación de demanda estacional, distancia/contratos y continuidad de servicio del centro | **Candidato para red/receptor cercano**; la IEA describe centros de datos como una fuente posible para grandes bombas de calor. Distancia, temperatura y comprador se tienen que validar. |
| ORC / ciclo de potencia | Generación eléctrica con rechazo que no encuentra calor de proceso | Ciclo Rankine orgánico/expansor adecuado | Temperatura, potencia, horas, coste, eficiencia neta, mantenimiento, agua/condensación y alternativa de uso directo | **No opción predeterminada**. Considerar tras descartar usos térmicos de mayor valor y con estudio de proveedor/modelo detallado. |
| Enfriamiento por absorción | Frío útil desde calor suficientemente caliente | Absorción | Temperatura de conducción, torre/rechazo, consumo auxiliar, horario de frío y costes del chiller existente | **Solo con demanda fría y balance integral**; calor disponible sin carga de frío no ayuda. |

**Transferencia entre emplazamientos:** elevar distancia agrega tubería/canalización, aislamiento, bombeo, pérdidas, permisos y derecho de paso, además de contratos de suministro, medición, precio y parada de dos empresas. La solución intraplanta suele ser el primer caso de menor complejidad. El JRC observó en su informe de 2021 que se comercializaban cantidades pequeñas de calor residual en Europa en ese momento; no inferir que no haya proyectos actuales. EMB3Rs demuestra que ya hay herramientas que modelan redes, GIS, pérdidas y modelos comerciales, así que “conectar instalaciones” no es un vacío funcional por sí solo.

### Temperaturas y estructura sectorial

Un estudio peer reviewed de potencial UE con base de consumo industrial de 2015 estimó 304 TWh/año de recurso técnicamente disponible; sus cálculos dependen de supuestos sectoriales y esa fecha de base, no son demanda disponible ni potencial económico actual. Reporta calor sobre todo a 100–200 °C y demandas mayormente por debajo de 100 °C en alimentos/textil, mientras metales/minerales requieren a menudo temperaturas mayores. La extrapolación por sectores y factores genéricos limitan su uso para priorizar una planta. [Forman et al., “Industrial waste heat: Estimation of the technically available resource in the EU per industrial sector, temperature level and country,” *Applied Thermal Engineering* (2018)](https://doi.org/10.1016/j.applthermaleng.2018.04.043).

La IEA/JRC sitúa bombas de calor industriales como opción madura principalmente para calor de baja y media temperatura; los saltos de temperatura y la relación de precios electricidad/combustible dominan desempeño y economía. La IEA explica que el COP depende de las temperaturas de evaporación/condensación, no simplemente de entrada/salida del agua, y revisa aplicaciones con fuentes industriales, aguas residuales y centros de datos. [JRC, *Heat pumps in the European Union — 2025 Status Report*](https://publications.jrc.ec.europa.eu/repository/handle/JRC144191); [IEA, *Renewables for Industry* (2025)](https://www.iea.org/reports/renewables-for-industry); [IEA, *Heat Pump Monitor 2026 — Key findings*](https://www.iea.org/reports/heat-pump-monitor-2026/key-findings); [IEA, *Heat pump development from lab to industry*](https://www.iea.org/articles/heat-pump-development-from-lab-to-industry) (proyecto piloto específico, no rendimiento generalizable).

## B. Matriz de oportunidades y priorización preliminar

| Prioridad para validar | Parejas candidatas | Por qué estudiar | Condición que debe pasar antes de llamarla oportunidad |
|---|---|---|---|
| 1 — Alimentación de agua / lavado / calor de proceso dentro de planta | Refrigeración o compresor → agua caliente/lavado | Flujos relativamente estables, baja complejidad inicial, demanda potencial diaria | Caudal y temperaturas medidas; carga de receptor simultánea; circuito separado; equipos y control compatibles; precio de combustible y electricidad |
| 2 — Recuperación a alimentación/aire de combustión | Horno/caldera → aire, carga o agua de alimentación | Uso dentro del mismo equipo puede desplazar combustible sin nueva red externa | Punto de rocío/corrosión, materiales, contrapresión, combustión y calidad del producto |
| 3 — Bomba de calor para proceso bajo-mediano | Refrigeración/efluente → pasteurización, CIP o secado | Fuente de baja T con sumidero estable y requerido más caliente | Temperatura real de evaporación/condensación, mapa del equipo a carga parcial, tarifa de electricidad, potencia y refrigerante |
| 4 — Agua residual/centro de datos a red térmica cercana | Fuente continua → edificios/proceso/distrito | Puede ser volumen estable y aprovechar calor local | Distancia, GIS, temperatura de red, perfil estacional, permisos, ownership, comprador y contrato |
| 5 — Varios procesos/almacenamiento | Fuente por lotes → demanda en periodo distinto | Un buffer puede resolver desajuste horario | Horas de carga/descarga, temperatura útil, capacidad, pérdidas, vida útil, espacio y coste del TES |
| 6 — ORC | Rechazo de media/alta T sin sumidero térmico | Potencia potencial cuando el calor no se puede vender/usar como calor | Benchmark de potencia neta tras auxiliares, temperatura/caudal, horas, CAPEX y alternativa térmica |

**Lectura de oportunidad comercial — HYPOTHESIS:** industria alimentaria, bebidas/lácteos, papel, química y procesos de lavado/secado reúnen una combinación plausible de fuentes térmicas y demandas bajas/medias; no hay análisis bottom-up de empresas o disposición a pagar en esta investigación. Metales/cemento tienen calor de gran calidad, pero la integración, polvo y continuidad elevan requisitos técnicos. El primer producto/servicio debería apuntar a auditores energéticos, integradores y equipos de energía de planta como usuarios expertos, no a una automatización que determine seguridad o ingeniería final.

## C. Competidores, herramientas y originalidad

| Producto/proyecto | Capacidades verificadas en fuentes públicas | Hueco/limitación que se puede afirmar con prudencia | Estado para ThermoGap |
|---|---|---|---|
| DOE MEASUR / PHAST | Suite gratuita/open source de más de 70 calculadoras y herramientas de evaluación de sistemas, incluida calefacción de proceso, vapor, aire comprimido, agua, motores y balances “what-if”; está orientada a mejoras por sistema. [MEASUR](https://www.energy.gov/cmei/ito/measur), [Process Heating](https://www.energy.gov/cmei/ito/process-heating-systems) (consultadas 2026-10-15). | El alcance declarado revisado no presenta el matching geográfico multisite/general como función principal. La página no permite concluir qué hace cada versión interna ni que no exista una función comparable. | No diferenciar por cálculos básicos ni auditoría aislada; usarlo como referencia para evaluación de equipos. |
| EMB3Rs | Plataforma H2020 para matching de calor/frío; TEO optimiza fuentes-sumideros bajo perfiles, costes, disponibilidad y restricciones, con opciones de almacenamiento térmico y operación temporal. Incluye GIS de redes/pérdidas y módulo de negocio NPV/LCOH/IRR. [Plataforma](https://www.emb3rs.eu/platform/), [repo TEO](https://github.com/Emb3rs-Project/p-teo), [manual TEO D3.4 (2022)](https://www.emb3rs.eu/wp-content/uploads/2022/11/D3.4_M38_submitted.pdf), [proyecto/casos](https://www.emb3rs.eu/about/), [Silva et al., *Energy Conversion and Management* 309, 118408 (2024)](https://doi.org/10.1016/j.enconman.2024.118408). | TEO documenta capacidad y operación temporal abstracta del almacenamiento; no se comprobó si representa estratificación/perfiles de temperatura del TES con fidelidad suficiente ni se ejecutó el caso ThermoGap. Disponibilidad y validación independiente actual tampoco medidas. | Refuta claims de matching y análisis temporal/económico genéricos (A, B, G) y cubre almacenamiento modelado a nivel de optimización (C). Candidato esencial de benchmark. |
| OpenPinch (open source, MIT) | Python para pinch, integración total-site, bombas de calor/refrigeración, exergía, cogeneración, síntesis HEN, análisis multiperiodo y perfiles por segmentos/cambio de fase. El repositorio consultado el 15-10-2026 indica Python ≥3.12; síntesis requiere extra IDAES/Pyomo y extensiones de solver. [Repositorio](https://github.com/waikato-ahuora-smart-energy-systems/OpenPinch), [flujos de decisión](https://openpinch.readthedocs.io/en/stable/examples/decision-workflows.html), [guía HEN](https://openpinch.readthedocs.io/en/stable/guides/heat-exchanger-network-synthesis.html). | Python 3.12.3 local cumple el requisito, pero OpenPinch no está instalado y no se ejecutó. Los extras/solver añaden preparación. No se midieron utilidad, rendimiento o soporte independiente. | Refuta que B, C y E sean novedosos como categorías. No demuestra cobertura suficiente de incertidumbre D, diagnóstico F ni valor de medición H. |
| OpenHENS | Proyecto open-source de optimización de síntesis de redes de intercambiadores; artículo reporta benchmark de problemas académicos. [Artículo](https://doi.org/10.1016/j.compchemeng.2025.109429), [repo](https://github.com/waikato-ahuora-smart-energy-systems/OpenHENS). | Síntesis HEN no equivale por sí misma a descubrimiento de datos, medición de incertidumbre o evaluación comercial a escala. | Competidor en diseño de red, no prueba de necesidad de reemplazarlo. |
| Aspen Energy Analyzer / Aspen HYSYS / Plus | Herramienta comercial de pinzado, targets de energía/capital, alternativas de retrofit HEN, análisis de costes y enlace a simulación; AspenTech presenta los resultados como capacidades del producto. [Producto](https://www.aspentech.com/en/products/engineering/aspen-energy-analyzer); [EDR](https://www.aspentech.com/en/products/engineering/aspen-exchanger-design-and-rating) (consultado 2026-10-15). | Coste/licencia, soporte de intercambio entre empresas y alcance exacto de tareas no medidos. Las afirmaciones de rendimiento son del proveedor. | Refuta claims pinch/HEN, alternativa y costeo en plantas de proceso. |
| TLK Energy Pinch Analysis Online | Entrada de streams, curvas compuestas, Grand Composite Curve y evaluación de integración de bombas de calor para planta industrial. [Herramienta](https://tlk-energy.de/en/tools/pinch-analysis-online) (consultada 2026-10-15). | El alcance público inspeccionado no afirma planificación multisite o modelos de incertidumbre. No se registró cuenta ni ejecutó análisis. | Refuta “curvas pinch” como novedad; posible alternativa de UX gratuita/comercial por determinar. |
| IDAES | Marco científico open-source de modelado/simulación/optimización de procesos, unidades de intercambiador y herramientas de diagnóstico; Linux compatible. [Software](https://idaes.org/software/), [docs](https://idaes-pse.readthedocs.io/en/stable/). | Plataforma de modelado extensible, no un flujo genérico llave-en-mano para identificar oportunidades en planta sin modelado. | Dependencia útil/alternativa base, no diferenciador. |
| Siemens SIMATIC Energy Manager / METRON | Adquisición y normalización de datos de energía/producción, KPIs, alertas, control, benchmarking, gestión empresarial multisite y análisis de eficiencia según afirmaciones de proveedores. [Siemens](https://www.siemens.com/en-us/energy-manager/), [METRON](https://www.metron.energy/solution/) (consultadas 2026-10-15). | Los folletos describen gestión de consumo y optimización general, no prueban screening termodinámico de transferencias heat-source/sink. Tampoco se auditó su alcance privado. | Competencia por presupuesto, canal de datos e integración. No competir con dashboards; considerar export/import e integración futura si MVP se justifica. |

### Claims A–H

| Diferenciador propuesto | Resultado de investigación |
|---|---|
| A. Varios focos y consumidores | **Ya existe** en EMB3Rs/OpenPinch y plataformas de proceso. Originalidad no sustentada. |
| B. Disponibilidad/demanda temporal | **Ya existe** en EMB3Rs y OpenPinch multiperiodo; el valor puede ser mejor UX o fuentes de datos, no el concepto. |
| C. Compatibilidad de temperatura | **Práctica establecida** por pinch, curvas compuestas, approach temperature y bomba de calor. |
| D. Incertidumbre de medición/predicción | **Gap potencial, NOT_VERIFIED.** No se ha comparado en profundidad; tendría que demostrar propagación transparente y decisión robusta que competidores no ofrezcan de modo suficiente. |
| E. Directo vs bomba de calor/almacenamiento | **Ya existe** en sistemas de integración/optimización; cuantificar fidelidad y alcance de modelos por benchmark. |
| F. Razón de inviabilidad | **Gap potencial, NOT_VERIFIED.** Explicar restricciones es útil, pero no se ha revisado cada producto ni sus diagnósticos. |
| G. CAPEX/OPEX/MRO/limitación financiera | **Ya existe** en tecnoeconomía de EMB3Rs, Aspen y otros. Costes de proveedor y de instalación siguen necesarios. |
| H. Valor de medir algo más | **Gap potencial, NOT_VERIFIED.** Puede ser diferenciador científico/comercial si prioriza el sensor/parámetro que cambia ranking/decisión y se valida con usuarios. |

**Conclusión de originalidad — VERIFIED en las funciones revisadas:** el matching multisource/sink, integración temporal, screening de bombas de calor y HEN/optimización no son categorías novedosas. La capacidad de almacenamiento térmico dinámico queda **NOT_VERIFIED** entre las herramientas comparadas. **HYPOTHESIS:** incertidumbre propagada, motivos de rechazo y valor de información podrían aportar a una preauditoría local; no se ha demostrado que falten en el mercado.

## D. Especificación física y termodinámica

### Datos de entrada mínimos

Cada corriente debe llevar: identificador, fuente/sumidero, fase y composición, caudal másico o volumétrico con densidad/unidad, presión, temperaturas de suministro/objetivo o curva entalpía-temperatura, perfil temporal, incertidumbre y origen de cada dato; restricciones de proceso, disponibilidad, ensuciamiento/corrosión, materiales, contaminación y reglas de seguridad. Para agua/hidrocarburos/mezclas con cambios de fase o (c_p(T)), usar paquete de propiedades acreditado o curva (h(T,p,x)), nunca una (c_p) fija por defecto. Registrar la versión y procedencia del método de propiedades.

### Balances y transferibilidad

Para una corriente monofásica sin reacción, en estado cuasiestacionario:

`Q_dot = m_dot × [h(T_in,p,x) − h(T_out,p,x)]`

Si `c_p` constante es una aproximación local explícita, `Q_dot ≈ m_dot × c_p × (T_in − T_out)`. Para cambio de fase, usar entalpía de entrada/salida y presión; no extrapolar calor sensible a través de la transición. Balance de intercambiador: `Q_dot_hot − Q_dot_cold − Q_dot_loss = 0`, dentro de tolerancia numérica e incertidumbre. Para flujo contracorriente, ambos terminales deben respetar `ΔT_min`, con perfil de temperaturas compatible; el pinch compuesto permite targets de sistema, pero no entrega diseño mecánico final.

El mínimo dinámico por sumidero `j` en periodo `t`:

`Q_ij,t ≤ min(Q_source,i,t_feasible, Q_sink,j,t_demand)`

`availability_i,t > 0`, `demand_j,t > 0`, y a lo largo de todo el intercambiador `T_hot(q) − T_cold(q) ≥ ΔT_min`.

La desigualdad de temperaturas se evalúa a lo largo del intercambiador, no solo en entradas. En red, sumar enlaces y pérdidas; en sistema cerrado incluir energía del fluido intermedio, bomba, intercambiadores y pérdidas. Intercambio indirecto/loop evita contaminación, pero añade approach térmico y bombas.

### Segunda ley y exergía

No hay transferencia espontánea desde frío hacia caliente; para elevación se requiere trabajo o fuente de alta temperatura. Para una bomba de calor ideal entre reservorios a `T_L` y `T_H` en kelvin, `COP_H,Carnot = T_H / (T_H − T_L)`; es un límite superior reversible, no predicción de equipo. El COP real depende del ciclo, refrigerante, temperaturas de refrigeración/condensación, intercambiadores, control y carga parcial. Balance del ciclo de bomba de calor: `Q_H = Q_L + W_comp` (más definición de auxiliares y pérdidas según la frontera). `Q_H` no se debe sumar como si fuera calor residual: `Q_L` procede de la fuente y `W` es electricidad adicional.

Para calor `Q` isoterma a `T`, exergía ideal relativa al ambiente `T_0`: `B_Q = Q × (1 − T_0/T)`. Corrientes con `T` variable requieren integrar `dB = (1 − T_0/T) dQ`; la exergía destruida debe ser no negativa en un proceso real. Calor a baja temperatura puede reducir combustible pero tiene baja exergía; no es electricidad equivalente.

### Pinch, almacenamiento y optimización

- **Pinch:** targets energéticos mínimos según `ΔT_min`; composite curves y grand composite curve guían niveles y utilidades. Contrastar con diseño de red porque el mínimo teórico puede exigir área/capital y restricciones de operación que lo vuelven inviable.
- **HEN:** modelos por etapas superestructurales y LP/MILP pueden optimizar ubicación, división de corrientes y servicios; MINLP o modelos detallados solo cuando el valor de la decisión compense complejidad. Para primer MVP, reducir a matching y balances con límites observables.
- **Tiempo:** periodos representativos con perfil de fuente y demanda; no promediar un pico con horas sin operación. Para lotes, respetar secuencia, almacenamiento y reserva de demanda. Modelar sensibilidad a calendario de parada.
- **TES:** balance de energía `E_(t+1) = E_t + η_c × Q_c,t × Δt − Q_d,t × Δt/η_d − U × A × (T − T_0) × Δt`, con límites de capacidad, temperaturas, potencia de carga/descarga y estado. Eficiencias y pérdidas no son constantes universales. Bloquear energía que no mantiene temperatura útil.
- **Cálculo:** usar SI internamente; validar dimensiones, estados físicos, caudales no negativos y bounds; preservar trazabilidad de entradas, decisiones y unidades.

### Propiedades, presión, seguridad y límites

Caída de presión cambia bombeo y puede afectar compresores, hornos y control; una estimación neta debe incluir potencia auxiliar. La compatibilidad de material, corrosión, erosión, sólidos, legionella/higiene, contaminación cruzada, inflamabilidad y clasificación de áreas exigen ingeniería apropiada. No incorporar safety assurance en MVP. Excluir de una recomendación automática equipos cuya operación segura/producto dependa de una curva no medida o dato fuera de límites.

### Validación propuesta y estado real

| Tipo de validación | Estado al cierre |
|---|---|
| ANALYTICALLY VERIFIED | **Parcial para los balances algebraicos sintéticos A–C**, a mano y por cálculo aritmético independiente; no para modelos de propiedades reales ni curvas complejas. |
| NUMERICALLY TESTED | **Parcial:** aritmética reproducida con Python estándar, sin solver ni modelo de proceso. No equivale a test de software. |
| EXTERNALLY BENCHMARKED | **No realizado.** Hay que comparar targets contra OpenPinch, Aspen/EMB3Rs si accesible y problemas académicos de referencia. |
| EXPERIMENTALLY VALIDATED | **No.** No hay instrumentación ni datos experimentales. |
| UNVALIDATED | Intercambiadores con `c_p(T)`/cambio de fase, caída de presión, mapas de heat pump, TES dinámico, incertidumbre de negocio, costes, emisiones de ciclo de vida y red entre instalaciones. |

Pruebas futuras: análisis dimensional y unit tests; comprobación de `Q_source = Q_sink + Q_loss`; benchmark analítico de dos corrientes y límites de Carnot; límite `ΔT_min → 0`, fuente insuficiente, sin coincidencia, unidades incompatibles, fase ambigua y disponibilidad cero; estabilidad del solver frente a discretización y periodos; reconciliación de datos con incertidumbre; intervalos Monte Carlo/sensibilidad con distribuciones medidas, no arbitrarias; benchmark independiente publicado y error cuantificado. No se ejecutó implementación, solver ni test suite.

## E. Tres casos sintéticos reproducibles

Los datos son didácticos y **no describen instalaciones reales**. Todas las tasas, horarios, eficiencia de caldera, costes y pérdidas abajo son entradas sintéticas asumidas para mostrar cálculo. No son cifras típicas recomendadas. Propiedad de agua: (c_p=4.18\,kJ/(kg\,K)) como aproximación constante de ejemplo en rango moderado; la app final requeriría (h(T,p,x)). Las unidades y operaciones pueden reproducirse con las ecuaciones de D y la tabla de entradas en `case-inputs.csv`.

### Caso A — Reuso directo

**Proceso:** agua caliente residual compatible de operación A pre-calienta agua de proceso B antes de lavado. Supuesto indirecto con intercambiador, `ΔT_min = 10 K`, sin evaporación, 6.000 h/año, caldera sustituida con eficiencia 90 %, bomba adicional 2 kW. Fuente: 2 kg/s, 90→55 °C disponibles en el límite teórico; consumidor: 1 kg/s, 20→60 °C.

| Magnitud | Resultado reproducible | Clasificación |
|---|---:|---|
| Potencial de fuente (2×4.18×(90-55)) | 292,6 kW | **MODEL PREDICTION** condicionado a inputs sintéticos |
| Demanda útil (1×4.18×(60-20)) | 167,2 kW | **MODEL PREDICTION** |
| Máximo por el binomio fuente-demanda | 167,2 kW | **MODEL PREDICTION**; la demanda limita |
| Salida fuente al duty entregado | 70,0 °C | **MODEL PREDICTION** (caída 20 K a 2 kg/s) |
| Diferencias terminales contracorriente | 90−60=30 K; 70−20=50 K | **MODEL PREDICTION**; ambas superan 10 K |
| Calor útil anual | 1.003,2 MWhth | **MODEL PREDICTION** (sin pérdidas de red asumidas) |
| Caldera desplazada | 1.114,7 MWh de combustible/año | **MODEL PREDICTION**; divide calor útil por 0,90 |
| Electricidad adicional | 12 MWh/año | **ENGINEERING ASSUMPTION**: bomba 2 kW×6.000 h |
| Balance de calor | Sin cambio de fase: 167,2 kW extraídos/entregados | **ANALYTICALLY VERIFIED** para estas ecuaciones; no prueba de equipo |

**Tecnología:** intercambiador líquido-líquido y bomba con bypass/control; si fuente está contaminada, intercambiador doble pared o circuito intermedio con coste/approach adicional. Revisar ensuciamiento, materiales, agua sanitaria/higiene y caída de presión. La bomba sintética de 2 kW no se deriva de una hidráulica; no representa potencia de diseño.

**Economía ilustrativa, no cotización:** mantenimiento 5.000 €/año; CAPEX instalado 100.000–300.000 €; precios de combustible sintéticos 30/60/100 €/MWh y electricidad 0,10/0,20/0,35 €/kWh. A 60 €/MWh combustible y 0,20 €/kWh electricidad: ahorro bruto de combustible 66.880 €/año, electricidad 2.400 €, mantenimiento 5.000 €, neto simple 59.480 €/año; payback simple 1,68–5,04 años sobre CAPEX supuesto. En combinación baja 30 €/MWhf y 0,10 €/kWhe da 27.240 €/año neto; combinación 100 €/MWhf y 0,35 €/kWhe da 102.267 €/año neto. No se incluyen impuestos, paradas, financiación, deterioro, coste de oportunidad, válvulas/red, vida útil ni incertidumbre estadística; por eso no se reportan NPV/IRR.

**Clasificación:** **FACTIBLE TERMODINÁMICAMENTE EN EL EJEMPLO; NO VALIDADO EN PLANTA.** Un intercambio útil directo es físicamente posible bajo los supuestos; la utilidad económica real depende de integración y costes.

**LEARNING:** la demanda recorta el potencial de fuente a 57 %. **EVIDENCE:** 167,2/292,6=0,572. **IMPACT:** identificar sumideros útiles es tan importante como medir el residuo. **CONFIDENCE:** alta aritmética, baja representatividad. **CARRY_FORWARD:** distinguir calor disponible y matchable. **UNRESOLVED:** variabilidad real de flujo/temperaturas, fouling, CAPEX y precio contrato.

### Caso B — Elevación térmica con bomba de calor

**Proceso:** agua residual caliente de proceso a 45 °C para un circuito de agua de limpieza a 80 °C; sumidero 100 kW. Caudal de fuente supuesto 2 kg/s. Bomba de calor entrega 100 kW con COP de escenario =3,0; auxiliar 1 kW; 6.000 h/año. El balance requiere `Q_L = 66.67 kW`, por lo que la fuente sale a `45 − 66.67/(2×4.18) = 37.03 °C`. Se supone un approach mínimo de 5 K en evaporador y condensador: para este balance, temperatura evaporante `≤32.03 °C` y condensación `≥85 °C`. Con 32.03/85 °C, COP Carnot de calefacción `358.15 / (358.15 − 305.18) = 6.76`, por encima del COP escenario 3. La fuente podría liberar hasta 125.4 kW enfriándose de 45 a 30 °C por entalpía, pero ese techo no está disponible con evaporación a 32 °C y approach de 5 K; el límite operativo de este ejemplo es aproximadamente 66.7 kW. COP=3 es un **supuesto no verificado**, no una curva de fabricante ni un rendimiento conservador demostrado. Se requiere un mapa real antes de declarar equipo factible. [IEA Renewables for Industry, fig. 2.3](https://www.iea.org/reports/renewables-for-industry) (2025, revisión de fuentes); [IEA heat pumps monitor 2026](https://www.iea.org/reports/heat-pump-monitor-2026/key-findings).

| Magnitud | Resultado | Clasificación |
|---|---:|---|
| Calor del evaporador (`Q_L = Q_H × (1 − 1/COP)`) | 66,67 kW; 400 MWh/año | **MODEL PREDICTION** |
| Compresor (`W = Q_H/COP`) | 33,33 kW; 200 MWh/año | **MODEL PREDICTION** |
| Salida (`Q_H = Q_L + W`) | 100 kW; 600 MWhth/año | **ANALYTICALLY VERIFIED** por conservación de energía |
| Bomba adicional | 6 MWh/año | **ENGINEERING ASSUMPTION**: 1 kW×6.000 h; no procede de diseño hidráulico |
| Electricidad total | 206 MWh/año | **MODEL PREDICTION** condicionado a COP auxiliar fijo |
| Fuente máxima | 125,4 kW | **MODEL PREDICTION**; suficiente para el `Q_L` supuesto |
| Combustible evitado en caldera 90 % | 666,7 MWhf/año | **MODEL PREDICTION** |
| Límite de COP ideal | 6,76 | **ANALYTICALLY VERIFIED** para 32,03/85 °C reservorios; el approach de 5 K es un supuesto |

**Economía sensible a la relación de precios:** ignorando mantenimiento y CAPEX, condición de ahorro operacional: `p_e/p_f < COP/η_boiler = 3.33` en unidades de energía compatibles, con `p_e` en €/MWhe y `p_f` en €/MWhf. A 60 €/MWhf y 0,20 €/kWhe (200 €/MWhe), el combustible evitado vale 40.000 €/año frente a 41.200 € electricidad adicional: **−1.200 €/año**, antes de mantenimiento/CAPEX. A 100 €/MWhf y 0,10 €/kWhe el saldo operativo es +46.067 €/año antes de esos costes. A 30 €/MWhf y 0,10 €/kWhe es −600 €/año. Esos precios son escenarios sintéticos, no pronóstico de tarifa.

**Clasificación:** **BALANCE TERMODINÁMICO POSIBLE BAJO APPROACHES Y COP SINTÉTICOS; EQUIPO REAL NO VERIFICADO; ECONOMÍA CONDICIONAL.** Los 1 kW de auxiliares son arbitrarios, no de un diseño hidráulico ni de un dimensionamiento del equipo. La conclusión cambia con COP, horas, precios, emisiones de red, temperatura de máquina y caudal. Una máquina ofertada con mapa de rendimiento tendría que confirmar calor útil, potencia, refrigerante, carga parcial, control y fiabilidad.

**LEARNING:** la elevación puede desplazar combustible y aun así no ahorrar dinero. **EVIDENCE:** escenarios con saldo −1.200 € y −600 € al año antes de CAPEX; COP queda por debajo del límite Carnot corregido. **IMPACT:** un ranking por kWh de calor recuperado produciría una recomendación engañosa. **CONFIDENCE:** alta en balance/aritmética; baja en COP real y escenarios de compra. **CARRY_FORWARD:** calcular coste y emisiones por portador energético y verificar el approach en ambos intercambiadores. **UNRESOLVED:** curva COP del fabricante, factores de emisión, mantenimiento, CAPEX y operación de planta.

### Caso C — Dos fuentes, dos sumideros y tiempos distintos

**Calendario sintético de 24 h repetido 300 días/año:** fuente S1, 100 kW, 100→75 °C, 0,957 kg/s, durante 00–08; sumidero A, 60 kW, 20→60 °C, 0,359 kg/s, durante 16–24. Fuente S2, 80 kW disponible a 100→80 °C, 0,957 kg/s, durante 08–16; sumidero B, demanda 50 kW, 20→70 °C, 0,239 kg/s, durante 08–16. Con 50 kW de S2, su salida calculada es 87,5 °C, dando terminales 30 K y 67,5 K: compatible con `ΔT_min = 10 K`. Ciclo de 300 días representa horas de parada agregadas. Se asume que S1 y S2 tienen energía suficiente a su temperatura y que no hay restricciones de producción. Almacén agrega eficiencia de ciclo 0,85 y red centralizada agrega 5 % de pérdida; bombas agregadas 1 kW en solución local con almacenamiento o 2 kW en red centralizada, encendidas 24 h. Todos son **supuestos sintéticos**, no rendimientos de producto.

| Configuración | Fuente útil requerida por ciclo | Calor entregado | Auxiliar/pérdidas | Resultado |
|---|---:|---:|---|---|
| Sin recuperación | 0 | 0 | Ninguno | Referencia: las dos demandas siguen usando calefacción original |
| Solo intercambiadores directos intraplanta, sin storage | S2: 400 kWh ciclo | 400 kWh (a B) | No se consideran pérdidas de HX local | A no coincide temporalmente; S1 no se cuenta como útil |
| Recuperación directa + TES local para S1→A | S1: 480/0,85=564,7 kWh; S2: 400 kWh | 880 kWh | TES pierde 84,7 kWh/ciclo; auxiliares 1 kW×24h =24 kWh/ciclo | Satisface ambas demandas en el modelo; carga TES 70,6 kW durante 8h, menor que fuente 100 kW |
| Loop central + TES, 5 % de pérdida de red | A: 480/(0,85×0,95)=594,4 kWh; B:400/0,95=421,1 kWh | 880 kWh | 135,5 kWh/ciclo en pérdidas combinadas; auxiliares 48 kWh/ciclo | Satisface ambas, pero consume 51,3 kWh/ciclo más de fuente que la integración local con storage |

Todas las temperaturas fueron escogidas para que los suministros puedan servir directamente (con `ΔT_min = 10 K`): no se modeló perfil espacial de storage ni se verificó temperatura de descarga al final. La variante sin storage a A no tiene coincidencia y se debe rechazar; si alguien conecta agua a 70 °C directamente a un receptor que requiere salida a 80 °C sin bomba, esa transferencia también se debe rechazar por temperatura. Storage no crea energía: solo cambia cuándo se entrega y añade pérdidas.

| Métrica anual de la configuración local con TES | Valor calculado |
|---|---:|
| Calor útil en sinks | 264 MWhth/año |
| Calor captado de S1+S2 | 289,4 MWhth/año |
| Pérdida térmica en TES | 25,4 MWhth/año |
| Electricidad auxiliar (1 kW continuo) | 7,2 MWhe/año |
| Combustible de caldera desplazado a eficiencia 90 % | 293,3 MWhf/año |

En red central, calor captado = 304,6 MWh/año y pérdida combinada =40,6 MWh/año; electricidad auxiliar =14,4 MWhe/año. No se valora CAPEX del almacenamiento, piping, HX, bombas, mantenimiento, espacio ni contrato. El coste incremental `ΔC` de centralización puede ser negativo o positivo según distancias y sharing; no se puede concluir económicamente. La alternativa “sin recuperación” constituye el negativo de economía: si un TES, línea y auxiliares cuestan más que el valor de los 264 MWh/año, la opción es racionalmente rechazada.

**Clasificación:** **INCOMPATIBLE SIN ALMACENAMIENTO; BALANCES ENERGÉTICOS Y CALENDARIO COMPATIBLES CON TES/RED BAJO EFICIENCIAS SINTÉTICAS; FACTIBILIDAD TÉRMICA DEL TES/RED NOT_VERIFIED; ECONOMÍA DESCONOCIDA.** **Negativos de control:** no solapamiento horario sin TES, y requisito de salida más caliente que una fuente directa. No se modelan perfil de temperatura dentro del almacenamiento, potencia de descarga, curva de pérdidas, capacidad, envejecimiento, demanda estacional, variación de propiedades, coste o seguridad.

**LEARNING:** desplazar temporalmente calor aumenta cobertura en el balance, pero la configuración central agrega pérdidas y su factibilidad física no quedó probada. **EVIDENCE:** la recuperación local usa 964,7 kWh/ciclo para 880 kWh útil; red central usa 1.015,5 kWh/ciclo. **IMPACT:** la red compartida debe compararse con integración local y cero recuperación, no solo con TES. **CONFIDENCE:** alta aritmética; baja factibilidad del TES. **CARRY_FORWARD:** hacer despacho temporal con límites de potencia, energía y temperatura y mostrar la base sin recuperación. **UNRESOLVED:** capacidad, estratificación, temperaturas de descarga, pérdidas, tasas y coste de línea.

### Reproducibilidad y límites de cálculo

Los tres casos se pueden rehacer manualmente desde `case-inputs.csv`. Las operaciones se reprodujeron con Python estándar, no con paquete termodinámico ni solver. No hay curvas de propiedades ni condiciones transitorias, por tanto estos casos verifican conservación aritmética para entradas sintéticas, no validación científica amplia. Los decimales se redondean al mostrar; no se deben exportar estos valores como ahorro de una planta.

## F. Tecnoeconomía y emisiones

Definiciones que el sistema debe conservar separadas:

1. (Q_{available}): calor retirado de corriente sin afectar operación.
2. (Q_{transferred}): calor a través de intercambiadores, después de límite de fuente/sumidero.
3. `Q_delivered`: calor recibido por proceso tras pérdidas.
4. `E_fuel,avoided = Q_delivered / η_baseline` solo si el receptor realmente desplaza la caldera/horno que se modela.
5. `E_electric,added`: compresor, bombeo, ventiladores, torres, controles y respaldo.
6. Ahorro de factura neto de combustible/electricidad, tarifas y mantenimiento; evitar doble contabilización de heat pump.
7. Emisiones evitadas `= E_fuel,avoided × EF_fuel − E_electric,added × EF_grid`, con límites, periodo, electricidad horaria y factores documentados. Factores no investigados/asignados aquí.

**Modelo:**

- `CAPEX = equipment + installation + controls + tie-ins + engineering + contingency`, con cotizaciones o rangos explícitos por tecnología/país y año. No inferir precio solo por potencia.
- `OPEX_t = maintenance_t + electricity_t + backup_t + water/chemicals_t + cleaning_t`.
- `Savings_t = avoided_fuel_cost_t + avoided_other_supply_t − incremental_electricity_t − OPEX_t`.
- `NPV = −CAPEX + Σ_t [Savings_t/(1+r)^t]`. Declinar NPV si vida útil, tasa, perfil de ahorro o coste de recambio no tienen base verificable; correr sensibilidades.
- Payback simple `CAPEX/Savings_annual` solo para ahorro anual positivo estable, claramente rotulado. IRR se justifica cuando hay flujos/inversión definidos y puede tener varias/no solutions; no reportarlo con la plantilla sintética.

Sensibilidades mínimas: caudal y temperaturas con errores de instrumentos; horas/carga/turnaround; `ΔT_min`, pérdidas/fouling; COP por par de temperaturas y carga; precios horarios fuel/elec; CAPEX de tie-in; tasa de descuento, mantenimiento, tasa de emisión y precio carbono. Para la primera herramienta, intervalos por escenarios es más honesto que probabilidades no sustentadas.

## G. Especificación de MVP si futura investigación justifica el paso

**No implementado.** Borrador de alcance para decidir, no comprometer arquitectura de producción.

- **Objetivo:** screening reproducible de oportunidad intraplanta para un asesor/ingeniero; tabla de fuentes y sinks, decisión de temperatura/horas, balances, alternativas y razones de rechazo, con incertidumbre de inputs y evidencia/fuente asignada.
- **Entradas:** CSV/JSON tabular en SI; (m), (h(T))/propiedades, composición/fase, temperaturas/presión, horarios por periodos, demanda mínima/máxima, restricciones, energía de referencia, tarifas/carbono seleccionables, coste ingresado por usuario y fuente de valor.
- **Salidas:** matches físicamente posibles y no; motivos de rechazo y datos faltantes priorizados; calor disponible/transferido/entregado; auxiliar y energía final evitada por portador; escenarios energéticos/financieros con bandas y trazabilidad; informe no certificante.
- **Motor:** Python 3, unidades verificadas (Pint o equivalente), biblioteca de propiedades configurable solo tras confirmar licencia/API; NumPy/SciPy para screening. No solver avanzado/CFD inicial; matriz de matches pequeña y determinista. OpenPinch/IDAES se comparan antes de escoger dependencias. El sistema debe poder trabajar offline y por CPU.
- **Módulos:** importación/validación; normalización y calidad; propiedades; filtros de temperatura/hora/seguridad; balances y matching; alternativas direct/HP/storage; escenarios financieros; reporte. Cálculo separado de gráficos/visualización.
- **Pruebas:** benchmarks analíticos; conversión de unidades; cero caudal; temperatura imposible; suma de energía; consistencia temporal; bounds COP vs Carnot; pérdidas TES; sensibilidad extrema; comparación con casos OpenPinch y al menos un resultado publicado. Incorporar tests deterministas y reproducirlos tras crítica si se autoriza desarrollo.
- **Límites:** no ingeniería de detalle/HX rating, selección final de equipo, recomendación de seguridad, control de planta, acceso a PLC, data cloud ni garantía de ahorro. No usar datos sensibles sin consentimiento y plan de datos.
- **Equipo y entorno observado:** `lscpu/free/python3` muestran Linux x86-64, Intel i7-6700HQ, 4 núcleos/8 hilos y 15 GiB visibles de 16 GiB; CPU-first satisface el alcance de cálculo pequeño sin GPU. Python actual 3.12.3 y NumPy 2.5.0 importan; SciPy, Pint, CoolProp y Pyomo no están instalados/importables. No se instalaron dependencias. OpenPinch declara Python ≥3.12, así que el runtime satisface su requisito; **la herramienta no está instalada ni ejecutada**. Sus funciones de síntesis requieren extras/solver. ManimGX requiere Python ≥3.13; es incompatible con el runtime activo sin entorno separado, aunque sus docs declaran Linux y render Vulkan CPU vía lavapipe. Licencia propia MIT y wheel nativo compuesto que declara GPL-3.0-or-later por x264; requiere revisión antes de redistribuir. No se instaló ni probó. La visualización debe permanecer separada del motor numérico. [Repositorio ManimGX](https://github.com/academa-labs/manimgx), [licencia/guía](https://manimgx.academa.ai/developer-guide/project-management/), [PyPI 0.1.1](https://pypi.org/project/manimgx/0.1.1/) (consultados 2026-10-15).

**Gates antes de PROCEED TO MVP:** (1) benchmark con EMB3Rs/OpenPinch/OpenHENS y al menos 5 ejemplos; (2) identificar una diferencia medible; (3) confirmación de dos usuarios técnicos de que un flujo local de preauditoría resuelve una decisión no atendida; (4) revisar compatibilidad, licencias y datos; (5) validar una hoja de datos con un ingeniero independiente. Esta investigación no cerró ninguno de los gates de mercado.

## H. Revisión crítica independiente

La revisión independiente se realizó mediante un subagente con encargo de buscar competidores y evidencia primaria por separado y criticar los claims del borrador. El informe de hallazgos y correcciones se guarda en `critical-review.es.md`.

**Correcciones principales aplicadas antes del cierre:**

1. Se retiró cualquier implicación de originalidad para matching multisource/multisink, integración temporal, bomba de calor, HEN y optimización económica. El soporte de despacho TES en OpenPinch no quedó demostrado y se marca como comparación abierta.
2. **Rectificación posterior:** la comprobación inicial registró por error Python ≥3.14.2 para OpenPinch. La página oficial vigente consultada de nuevo indica ≥3.12; Python local 3.12.3 cumple. Se mantiene que no se instaló ni ejecutó y que los flujos HEN requieren extras/solver. La evidencia inicial se conserva en el registro operativo, con esta corrección explícita.
3. En bomba de calor, la primera revisión adversarial detectó cruce de temperatura en evaporador del borrador (40 °C de evaporación frente a fuente que cae a 37 °C). Se corrigió a evaporación ≤32,03 °C para un approach supuesto de 5 K, se recalculó Carnot a 6,76 y se mantuvo COP=3 como **no verificado**.
4. Calor bruto no se acredita como calor recuperable; la matriz menciona fouling/corrosión, materiales, presión, higiene, contaminación y calendario.
5. CAPEX/OPEX se aíslan como hipótesis explícitas de Caso A; no se citan como coste de industria. No hay NPV ni IRR falsamente precisados.

**Defectos y riesgos todavía abiertos:**

- No se verificó utilidad, disponibilidad, licencias o precisión de la instancia pública EMB3Rs ni se ejecutó OpenPinch. Los claims de software son capacidades declaradas/publicadas.
- Los tres ejemplos son deliberadamente simples; no representan dos fases, fugas, condensación, intercambiadores reales, caída de presión o control.
- La prueba de economía no incluye impuestos, carbon price, estacionalidad ni contratos de electricidad. Ni siquiera el “payback” sintético debe confundirse con oferta real.
- No existe benchmark externo ni medición empírica; los aciertos físicos solo se refieren a las ecuaciones definidas.
- La supuesta brecha en incertidumbre/valor de información/razones de inviabilidad sigue **NOT_VERIFIED**.
- Cliente, precio, canal, disposición a pagar y ahorro de tiempo del consultor no han sido investigados con usuarios. Mercado y comercialización no verificados.
- Riesgos de operación segura, proceso, contaminación e ingeniería de detalle permanecen fuera del alcance.

### LEARNING de la crítica

**LEARNING:** un cálculo de COP puede respetar primer principio y aún violar approach térmico. **EVIDENCE:** revisión independiente detectó evaporación inicial a 40 °C mientras la corriente fuente bajaba a 37,03 °C; el informe recalculó con approach de 5 K. **IMPACT:** la viabilidad de la bomba de calor debe revisarse en cada punto del intercambiador. **CONFIDENCE:** alta; consecuencia directa de balance térmico. **CARRY_FORWARD:** modelar perfiles fuente/refrigerante/sumidero con approach en ambos lados. **UNRESOLVED:** COP/máquina real y si un proveedor cumple las temperaturas a carga parcial.

**LEARNING:** la mayoría de los diferenciales candidatos colisiona con software existente. **EVIDENCE:** lectura primaria independiente de EMB3Rs y OpenPinch y corrección del borrador. **IMPACT:** cambiar la investigación siguiente de “construir matcher” a “probar brecha frente a competidores”. **CONFIDENCE:** alta en solapamiento funcional publicado. **CARRY_FORWARD:** comparar las mismas corrientes, perfiles, costes y decisiones entre productos. **UNRESOLVED:** comportamiento real, uso industrial vigente, licencias y calidad comparativa.

## I. Mercado, clientes, financiación y alianzas

### Clientes y socios potenciales (sin contacto)

Los primeros usuarios potenciales serían consultores/auditores de eficiencia, ingeniería de proceso, responsables energéticos de plantas alimentarias, químicas y de papel, ESCOs e integradores de bombas de calor/intercambiadores. Como socios de validación candidatos —no colaboradores confirmados—: centros tecnológicos, universidades, IEA HPT TCP, NREL/ORNL, DOE MEASUR y proyectos europeos/locales de calor residual. No se contactó a ninguna entidad. Necesidad y willingness-to-pay **NOT_VERIFIED**.

### Financiación estadounidense; elegibilidad desde España

- **DOE SBIR/STTR:** subvención/contrato competitivo de I+D, con fase de feasibility y posteriores. La página DOE vigente a fecha del informe limita participación a pequeña empresa con fines de lucro de EE.UU. que cumpla SBA; SBA exige lugar de negocio en EE.UU., operación principal/contribución significativa económica estadounidense, mayoría directa (>50 %) de ownership/control elegible y trabajo de I+D en EE.UU. para la elegibilidad ordinaria. Una residencia del fundador en España no determina por sí sola nacionalidad, ownership, lugar de negocio, actividad o worksite. **Inferencia conservadora:** si ThermoGap se funda y opera exclusivamente desde España, SBIR/STTR no es ruta elegible. Cualquier estructura mixta debe verificarla con el NOFO/agency y legal antes de considerar aplicación. [DOE SBIR/STTR](https://www.energy.gov/technologycommercialization/doe-small-business-innovation-research-sbir-and-small-business); [SBA/SBIR eligibility FAQ](https://www.sbir.gov/faq/eligibility-requirements). |
- El DOE FY26 SBIR/STTR *Genesis Mission* inspeccionado cerró a solicitantes el **10 de septiembre de 2026** y su tema es IA para Genesis Mission, por lo cual está cerrado y no parece encajar directamente con screening de calor industrial. [Hub del solicitation](https://sbir-sttr.connectwerx.org/portfolio-items/fy26genesismission/) (fecha; el aviso oficial del DOE describe sus topic areas [aquí](https://www.energy.gov/technologycommercialization/doe-small-business-innovation-research-sbir-and-small-business-technology-transfer-sttr)). |
- **DOE ITO/NOFOs, prizes y lab calls:** son subvenciones/ayuda no dilutiva o fondos de colaboración, pero cada anuncio define elegibilidad geográfica, partner, cost share y topic. La página ITO inspeccionada lista programas históricos y no mostró una convocatoria industrial abierta apta para ThermoGap al 15-10-2026. La FOA Industrial Efficiency and Decarbonization de hasta $104M corresponde a convocatoria histórica cerrada; no es dinero solicitables hoy. Revisar la tabla oficial antes de decidir; no presentar aplicación. [ITO funding opportunities](https://www.energy.gov/cmei/ito/ito-funding-opportunities); [IED FOA](https://www.energy.gov/cmei/ito/industrial-efficiency-and-decarbonization-funding-opportunity-announcement). |
- **Procurement:** MEASUR, auditorías o servicios de análisis podrían comprarse a través de licitaciones/contratos, no son grants. No se identificó oportunidad de adquisición abierta para este software. |
- **Aceleradoras/equity:** aceleración/inversión no es subvención ni procurement; no se verificó programa estadounidense que sea apto y relevante para una fundadora/equipo residente en España a esta fecha. No se recomendó uno sin convocatoria elegible validada. |

## Registro de evidencia

Fecha de acceso para páginas dinámicas: **2026-10-15**, salvo fecha de publicación indicada. “Limitación” separa lo que el documento no demuestra. Las fuentes citadas en secciones son fuente primaria oficial, repositorio del proyecto, informe público o trabajo revisado por pares; las cifras de productos siguen siendo declaraciones del propietario cuando no hay evaluación independiente.

| Fuente | Título y fecha | Relevancia y limitación |
|---|---|---|
| [DOE](https://www.energy.gov/cmei/ito/waste-heat-recovery-basics) | Waste Heat Recovery Basics; publicado hace ~3 años, actualizado/enlace de recursos 2025 | Contexto de pérdidas y barreras; fracción agregada no significa recuperabilidad de planta. |
| [DOE](https://www.energy.gov/cmei/ito/process-heating-systems) | Process Heating Systems; portal vigente | Herramientas PHAST/MEASUR y recuperación en hornos; página de navegación, no un estudio comparativo del software. |
| [DOE](https://www.energy.gov/cmei/ito/measur) | MEASUR; portal vigente, consultado 2026 | Alcance y software libre/opensource; capacidad según descripción DOE, no benchmark independiente. |
| [DOE](https://www.energy.gov/cmei/ito/finding-efficiencies-process-heat) | Finding Efficiencies in Process Heat; portal vigente | Importancia de calor y opciones de ITO; cifras nacionales históricas para 2018. |
| [DOE sourcebook](https://www.energy.gov/sites/default/files/2016/03/f30/Improving%20Compressed%20Air%20Sourcebook%20version%203.pdf) | Improving Compressed Air System Performance, 3rd ed.; 2016 | Recuperación de compresores; valores tipificados, no garantía de equipos. |
| [JRC](https://publications.jrc.ec.europa.eu/repository/handle/JRC126383) | Quantifying the role of waste heat in the EU energy system; 2021 | Definición/contabilidad y revisión de potenciales; no describe mercado actual. |
| [Forman et al.](https://doi.org/10.1016/j.applthermaleng.2018.04.043) | Industrial waste heat: technically available resource in EU; 2018 | Estima potencial por temperatura/sector con datos 2015; resultado modelado, factores sectoriales. |
| [JRC](https://publications.jrc.ec.europa.eu/repository/handle/JRC144191) | Heat Pumps in EU 2025 Status Report; 2025 | Tendencias y barreras de bombas de calor; estadísticas no son desempeño de un sitio. |
| [IEA](https://www.iea.org/reports/renewables-for-industry) | Renewables for Industry; 2025 | Aplicaciones y relación COP/lift; sus casos no garantizan el COP de Caso B. |
| [IEA](https://www.iea.org/reports/heat-pump-monitor-2026/key-findings) | Heat Pump Monitor 2026, key findings; 2026 | Estado actual de bombas de calor industriales y barreras; cobertura global e industrial agregada. |
| [IEA HPT TCP/IEA](https://www.iea.org/articles/heat-pump-development-from-lab-to-industry) | Heat pump development from lab to industry; proyecto observado 2016–2019 | Ejemplo piloto 20/300 kW y aplicación hasta 115°C; caso tecnológico particular. |
| [EMB3Rs](https://www.emb3rs.eu/platform/) | Plataforma y módulos; proyecto Horizon 2020 GA 847121, sitio consultado 2026 | Confirma matching, GIS, optimización technoeconómica y casos; no prueba desempeño comercial actual. |
| [EMB3Rs TEO repo](https://github.com/Emb3rs-Project/p-teo), [manual D3.4](https://www.emb3rs.eu/wp-content/uploads/2022/11/D3.4_M38_submitted.pdf) | Código y manual público, entregable fechado 26-10-2022 | Documenta perfiles temporales y capacidad/operación de almacenamiento; no demuestra estratificación del TES de ThermoGap ni validación industrial. |
| [EMB3Rs](https://www.emb3rs.eu/about/) | About/objetivos y 7 case studies; proyecto 2019–2022 | Contradice novedad de matching; resultados de demostración no reanalizados aquí. |
| [Silva et al.](https://doi.org/10.1016/j.enconman.2024.118408) | EMB3Rs: A game-changer tool to support waste heat recovery and reuse; *Energy Conversion and Management*, 309, article 118408 (2024) | Evaluación académica de la plataforma; casos/estimaciones del estudio, no ensayo independiente de rendimiento productivo. |
| [OpenPinch](https://github.com/waikato-ahuora-smart-energy-systems/OpenPinch) | Repo y documentación consultados 2026-10-15; README actual declara Python ≥3.12 | Capacidades, licencia y extras; compatible por requisito con Python 3.12.3, pero no instalado ni ejecutado. |
| [OpenPinch workflows](https://openpinch.readthedocs.io/en/stable/examples/decision-workflows.html) | Decision workflows; docs actuales | Enumera multiperiod, HPR/HEN; no demuestra calidad de resultados en instalaciones. |
| [OpenPinch HEN](https://openpinch.readthedocs.io/en/stable/guides/heat-exchanger-network-synthesis.html) | HEN synthesis guide; docs 0.6.x | Requiere extras IDAES/solver para síntesis; no se ejecutó. |
| [OpenHENS paper](https://doi.org/10.1016/j.compchemeng.2025.109429) | HENS unchained; 2025 | Sintetizador open source y benchmark de 13 problemas; alcance HEN académico. |
| [AspenTech](https://www.aspentech.com/en/products/engineering/aspen-energy-analyzer) | Aspen Energy Analyzer; portal vigente 2026 | Capacidad de HEN/retrofit declarada por fabricante; no se inspeccionó licencia ni software. |
| [TLK Energy](https://tlk-energy.de/en/tools/pinch-analysis-online) | Pinch Analysis Online; servicio consultado 2026 | Curvas, streams y heat-pump integration declaradas; no se ejecutó cuenta/prueba. |
| [IDAES](https://idaes.org/software/) | IDAES Integrated Platform; docs vigentes | Marco abierto Linux/macOS/Windows; extensible y especializado, no flujo de descubrimiento industrial out-of-box. |
| [Siemens](https://www.siemens.com/en-us/energy-manager/) | SIMATIC Energy Manager; oferta actual consultada 2026 | Monitorización/analítica planta y multisite; claims del proveedor, no matcher térmico demostrado. |
| [METRON](https://www.metron.energy/solution/) | Energy Management Solution; oferta actual consultada 2026 | Gestión/optimización de rendimiento de energía; claims de proveedor, no benchmark independiente. |
| [ManimGX](https://github.com/academa-labs/manimgx) | Repo y documentación consultada 2026 | Python ≥3.13/Linux CPU lavapipe y licencia compuesta; no instalado ni probado. |
| [SBA/SBIR](https://www.sbir.gov/faq/eligibility-requirements) | Eligibility requirements FAQ; estado consultado 2026-10-15 | Regla de small business y requisito de ubicación/operación EEUU; el caso individual depende de facts, control y NOFO. |
| [DOE](https://www.energy.gov/technologycommercialization/doe-small-business-innovation-research-sbir-and-small-business-technology-transfer-sttr) | DOE SBIR/STTR; actualización consultada 2026 | Programa y convocatoria FY26; tema Genesis no necesariamente compatible con el producto. |
| [DOE ITO](https://www.energy.gov/cmei/ito/ito-funding-opportunities) | ITO Funding Opportunities; vista dinámica actual | Lista de oportunidades; snapshot observado sin llamada industrial abierta adecuada. |

## Registro LEARN y decisión

| Aprendizaje | Evidencia | Impacto | Confianza | Carry forward | No resuelto |
|---|---|---|---|---|---|
| Oportunidad industrial depende de temperatura útil + tiempo + instalación. | Fuentes DOE/JRC/IEA y Caso C. | El filtro temporal y de seguridad debe preceder a la economía. | Alta física, media aplicación. | Modelar periodos y perfiles. | Frecuencia de medición que requiere planta. |
| Matching/HEN/multiperiodo no es vacío de producto. | EMB3Rs/OpenPinch/Aspen y competidores. | Evita invertir en un clone genérico. | Alta funciones declaradas. | Benchmark entre tareas comunes. | Calidad/uso actual/licencias. |
| Un salto térmico no genera calor gratis. | Primera ley, COP y Caso B. | Economía y emisiones pueden ir contra recuperación térmica. | Alta balance; baja inputs de campo. | Mostrar (Q_L,W,Q_H) y energía de respaldo por separado. | Mapa de rendimiento real. |
| TES puede resolver incompatibilidad horaria con penalización. | Balance Caso C y ecuación TES. | Almacenamiento debe optimizarse con despacho y temperatura. | Alta aritmética; baja costes. | Estado/capacidad/pérdidas explícitas. | Tecnología/coste/degradación. |
| Brechas de incertidumbre/VOI son candidatas, no acreditadas. | Revisión adversarial y limitado alcance revisado de competidores. | Investigar valor diferencial antes de implementar. | Media-baja. | Comparar feedback y outputs de 3 herramientas. | Presencia/valor comercial. |
| Ayuda DOE no es ruta inmediata confirmada para un residente en España. | SBA/DOE y convocatorias inspeccionadas. | No construir plan de caja sobre una subvención incierta. | Alta para reglas generales; baja caso individual. | Consultar convocatorias actuales solo si aparece encaje. | Ciudadanía, entidad, control, ubicación y NOFO futuro. |

## Decisión final

### Comparación directa de los tres casos con herramientas existentes

**Alcance:** comparación documental de capacidades públicas frente a los mismos inputs sintéticos de `case-inputs.csv`. No se ejecutó ningún competidor, así que no hay resultados numéricos comparables entre programas. OpenPinch declara Python ≥3.12 (compatible por versión con Python local 3.12.3), flujos de bombas de calor y multiperiodo; la síntesis HEN requiere extras/solver. EMB3Rs publica análisis source–sink, perfiles y evaluación tecnoeconómica, pero el acceso a la plataforma no se verificó. [OpenPinch](https://github.com/waikato-ahuora-smart-energy-systems/OpenPinch), [flujos de OpenPinch](https://openpinch.readthedocs.io/en/stable/examples/decision-workflows.html), [plataforma EMB3Rs](https://www.emb3rs.eu/platform/).

| Caso ThermoGap | Resultado del modelo sintético | Comparación funcional documentada | Resultado de ejecutar otro producto |
|---|---|---|---|
| **A — reuso directo** | 292,6 kW disponibles, pero solo 167,2 kW caben en la demanda; el approach supuesto se respeta. | OpenPinch cubre targeting/pinch e integración directa; EMB3Rs declara matching de fuentes y sumideros. Es una función ya atendida. | **NOT_VERIFIED:** ningún programa ejecutó estos inputs. |
| **B — bomba de calor** | 100 kWth entregados requieren 33,33 kWe al COP sintético 3; el caso de precio elegido da −€1.200/año antes de CAPEX/O&M. COP y precio son supuestos, no cotizaciones. | OpenPinch documenta screening de bombas de calor y mapa de rendimiento; EMB3Rs publica evaluación de tecnologías y economía. Mismos cálculos serían posibles en principio, pero requieren datos/curvas y configuración. | **NOT_VERIFIED:** no se contrastaron COP, selección ni economía con software. |
| **C — horarios y almacenamiento** | Sin TES, S1→A se rechaza por falta de coincidencia; con TES agregado se cubren 880 kWh/ciclo, pero temperatura y despacho del almacenamiento ThermoGap quedan **NOT_VERIFIED**. | EMB3Rs TEO documenta optimización de almacenamiento con operación temporal, capacidad y restricciones de carga/descarga; OpenPinch documenta periodos multiperiodo, pero no se encontró evidencia de TES dinámico. La documentación de EMB3Rs no prueba estratificación ni valida este caso concreto. | **NOT_VERIFIED:** ningún software corrió el calendario. La función de despacho TEO está documentada, pero sus resultados para este caso no se compararon. |

**Conclusión comparativa:** el modelo ThermoGap reproduce reglas y balances simples, pero no se ha demostrado que supere a competidores en resultados ni cobertura. En A y B las categorías funcionales ya existen. En C EMB3Rs documenta despacho temporal y dimensionamiento de TES; queda por contrastar la fidelidad termodinámica de temperatura/estratificación frente al almacenamiento concreto. No hay evidencia de que esto cree una brecha comercial. La ventaja potencial de ThermoGap sigue siendo **HYPOTHESIS**.

**LEARNING:** hacer los mismos inputs no basta para probar una ventaja si no se ejecuta el mismo benchmark. **EVIDENCE:** OpenPinch documenta targeting, heat-pump y análisis multiperiodo; EMB3Rs TEO documenta perfiles y almacenamiento temporal, pero ninguna herramienta ejecutó aquí el CSV ThermoGap. **IMPACT:** no presentar la revisión como benchmark de rendimiento. **CONFIDENCE:** alta sobre la limitación; media-alta sobre capacidades declaradas. **CARRY_FORWARD:** introducir el mismo CSV, unidades, periodos, límites y escenarios económicos en cada herramienta; registrar resultados, rechazos y datos faltantes. **UNRESOLVED:** error relativo, fidelidad termodinámica del TES, esfuerzo de modelado y calidad de resultados comparados.

### RESEARCH FURTHER

**Razón:** oportunidad física y relevancia industrial respaldadas; escenarios muestran que existe utilidad posible bajo compatibilidad, pero no demuestran escala o rentabilidad. La afirmación de producto original queda refutada en la mayoría de los diferenciales planteados; sobreviven posibles gaps de incertidumbre, rechazo explicable y valor de información, sin evidencia suficiente de que estén vacantes o sean valiosos para compradores. Un MVP de matcher general duplicaría herramientas existentes.

**Siguiente paso único:** ejecutar un benchmark comparativo de los tres casos sintéticos de este informe más casos publicados seleccionados con trazabilidad en EMB3Rs, OpenPinch y, donde haya acceso lícito, OpenHENS o Aspen, midiendo resultados, horas de ingeniería, incertidumbre y explicación de inviabilidad; mantenerlo local/aislado y no empezar producto hasta identificar una diferencia repetible.

## Estado operativo

**DONE:** revisión documental con fuentes oficiales, técnicas, peer-reviewed y de productos; matrices de fuentes, receptores y competidores; especificación física/validación; tres casos sintéticos con aritmética reproducida; revisión crítica independiente; decisión RESEARCH FURTHER. No se instaló software, se contactó con nadie ni se usaron datos industriales.

**MISSING:** benchmark práctico ejecutado contra productos; modelo de propiedades con (c_p(T))/fases; costes con cotizaciones; factores de emisiones; datos y entrevistas autorizadas; validación experimental; estado jurídico/financiero individual. OpenPinch cumple el requisito de versión de Python local, pero no está instalado ni ejecutado.

**CRITICAL FINDINGS:** (1) el matchmaking, multiperiodo y HEN ya están en competidores; (2) pequeños cambios en temperatura/horario/COP pueden destruir valor físico o económico; (3) el mercado pagador y la ventaja de incertidumbre/explicabilidad no están demostrados.

**NEXT ACTION:** realizar el benchmark comparativo descrito arriba antes de autorizar MVP.

## Complemento posterior — rutas a productos comerciales

La investigación posterior confirma que el calor puede habilitar producción comercial: caso documentado de fundición de aluminio que vende calor para secar malta; centro de datos que aporta calor para cultivos hidropónicos; y estudio de Madrid que modela recuperación de calor en secado de subproductos alimentarios. Los grados de prueba difieren: implementaciones documentadas, caso institucional y estudio tecnoeconómico, respectivamente. Aún no hay márgenes auditados comparables.

Esta extensión **no cambia la decisión RESEARCH FURTHER**. EMB3Rs y SymbiosisMatch ya cubren screening/matching y parte del análisis económico; ThermoGap tendría que demostrar que conecta mejor la fuente térmica con insumo secundario, producto/oferta, comprador y margen incremental, con rechazo físico y comercial transparente. El seguimiento, fuentes, crítica y límites están en [rutas comerciales de calor residual](commercial-product-routes.es.md).
