# ThermoGap — revisión crítica independiente

**Fecha:** 15 de octubre de 2026. **Revisor:** subagente crítico separado del autor del borrador; investigó competidores y revisó adversarialmente el informe y los casos. **Estado:** revisión hecha; hallazgos críticos preservados y correcciones aplicadas al informe. Esta revisión no equivale a validación experimental ni aprobación de ingeniería de proyecto.

## Hallazgos principales

### 1. Defecto físico crítico detectado y corregido — Caso B

**Borrador inicial:** COP=3, `Q_H = 100 kW`, `Q_L = 66,667 kW`, agua fuente 2 kg/s y `c_p = 4,18 kJ/(kg K)`, desde 45 °C. Por balance, la salida del agua es:

`45 − 66.667/(2×4.18) = 37.03 °C`.

El primer borrador imponía evaporación a 40 °C. La fuente habría quedado 2,97 K más fría que el refrigerante, produciendo cruce de temperatura; un intercambiador evaporador no puede transferir el calor exigido con approach positivo. El COP Carnot de 7,96, aunque correcto para reservorios abstractos a 40/85 °C, no correspondía a la fuente útil del caso.

**Corrección aplicada:** se impuso approach de 5 K como supuesto sintético en ambos lados: evaporación máxima 32,03 °C y condensación mínima 85 °C. COP Carnot recalculado = 6,76. COP=3 queda como supuesto hipotético no verificado; los 125,4 kW al enfriar de 45 a 30 °C son solo límite de entalpía, no disponibilidad real con ese approach. Para el duty actual, la fuente sale a 37,03 °C y aporta 66,67 kW. El balance es posible bajo los approaches supuestos, pero el equipo, COP, control y carga parcial son **NOT_VERIFIED**.

**Clasificación de crítica:** defecto original **CRÍTICO**; corrección incorporada; rendimiento de bomba de calor **NO VALIDADO**.

### 2. Caso C: no exceder el alcance del modelo

La tabla de energía y el calendario son consistentes: local con TES usa 964,7 kWh/ciclo para 880 kWh entregado; red central usa 1.015,5 kWh/ciclo, con 135,5 kWh de pérdidas asumidas. Caudales S1/S2/sinks son coherentes con deberes y `c_p` sintético; S2→B entrega 50 kW con salida de fuente 87,5 °C y terminales 30/67,5 K.

Sin embargo, una eficiencia agregada η de 0,85 y 5 % de pérdida de red no prueban temperatura de descarga, capacidad de almacenamiento, potencia de carga/descarga, estratificación, curva de pérdida `U×A`, duración ni approach durante el intercambio. Se corrigió la clasificación a **balances energéticos y calendario compatibles bajo eficiencias sintéticas**, con factibilidad térmica del TES/red **NOT_VERIFIED**. Los valores 0,85 y 0,95 son supuestos didácticos, no rendimientos de equipos representativos.

**Clasificación de crítica:** aritmética **VERIFIED**; TES/red físicos **NOT_VERIFIED**.

### 3. Caso A: balance y economía reproducidos; cargas auxiliares ficticias

Se reproduce: fuente 292,6 kW; sink 167,2 kW; salida caliente 70 °C al duty; terminales contracorriente 30/50 K; 1.003,2 MWhth/año; 1.114,7 MWhf/año desplazados con eficiencia asumida 90 %. Payback 1,68–5,04 años sobre CAPEX supuesto y neto de 59.480 €/año en tarifa media son aritméticamente correctos para los números sin redondear.

La bomba de 2 kW en A y bomba de 1 kW en B no se derivaron de un diseño hidráulico. La caída de presión, longitud de tubería, altura, viscosidad, eficiencia de bomba/ventilador y límites de equipos no se modelaron. El informe ya califica cargas, costes y pérdidas como sintéticos; debe permanecer explícito que esos kW no representan predicción ni cotización de un circuito instalado.

**Clasificación de crítica:** balance **ANALYTICALLY VERIFIED** para los supuestos; pérdidas/costes de instalación reales **NOT_VERIFIED**. En escenario alto el ahorro es 102.267 €/año con cifras sin redondear; recalcular solo con precisión homogénea (usar valores display 102.270 €/año si se multiplica el combustible redondeado 1.114,7 por 100 €/MWh).

### 4. Competidores y diferenciación

- **EMB3Rs — VERIFIED por documentación pública y paper revisado por pares:** matching intra/externo, múltiples fuentes y sinks, disponibilidad/load profiles, GIS, pérdidas/costes de red, optimización tecnoeconómica, NPV/LCOH/IRR. Fuentes: [plataforma](https://www.emb3rs.eu/platform/), [paper 2024](https://doi.org/10.1016/j.enconman.2024.118408), [casos](https://www.emb3rs.eu/about/). No se probó su instancia actual.
- **OpenPinch — VERIFIED por repo/docs (revisado 2026-10-15):** multiperiod, integración de heat pump/refrigeration, piecewise properties, targeting y HEN synthesis. [Repo](https://github.com/waikato-ahuora-smart-energy-systems/OpenPinch), [decision workflows](https://openpinch.readthedocs.io/en/stable/examples/decision-workflows.html), [HEN](https://openpinch.readthedocs.io/en/stable/guides/heat-exchanger-network-synthesis.html). La versión vigente declara Python ≥3.12, no ≥3.14.2 como decía la revisión inicial; el runtime local 3.12.3 cumple, pero no se instaló ni ejecutó. HEN requiere extras/solver.
- **OpenHENS — VERIFIED como trabajo publicado:** 13 benchmarks académicos; 7 resultados dentro de 2 % del total annualized cost reportado. [Paper](https://doi.org/10.1016/j.compchemeng.2025.109429), [repo](https://github.com/waikato-ahuora-smart-energy-systems/OpenHENS). No se ejecutó.
- La revisión del informe mantiene A/B/C/E/G como categorías ya cubiertas. No atribuir a OpenPinch funciones no demostradas de incertidumbre (D), diagnóstico explicable de infeasibilidad (F) o valor de información (H); siguen gaps potenciales **NOT_VERIFIED**.
- La capacidad pública demuestra solapamiento funcional, no equivalencia de calidad, adopción o soporte comercial. Sería excesivo llamar original al sistema solo por el nombre o una combinación de funciones.

### 5. Fuentes industriales, financiación y alcance

- Fuentes de calor residual y potencial sectorial están citadas por DOE/JRC/IEA; los receptores concretos de secado, química/papel/textil y aguas residuales se reclasificaron como candidatos o hipótesis de ingeniería cuando no había dato sectorial específico. No usar la matriz como cuantificación comercial.
- **Funding EEUU — snapshot VERIFIED a 2026-10-15:** [SBA FAQ](https://www.sbir.gov/faq/eligibility-requirements) requiere lugar de negocio, contribución/operación en EE.UU., ownership/control elegible y trabajo I+D en EE.UU. La inferencia “fundada y operada exclusivamente desde España probablemente no califica SBIR/STTR” está debidamente condicional; ciudadanía, control y estructura de una entidad concreta no se conocen. DOE FY26 Genesis cerró el 10-sep-2026 y no parece encajar directamente con ThermoGap; ITO actual no mostró convocatoria adecuada abierta al corte. Este estado expira y debe revisarse antes de aplicar.
- El informe no ejecutó benchmarks, herramientas, instalaciones o tests. “VERIFIED” para casos se limita a aritmética/supuesto. **EXTERNALLY BENCHMARKED** y **EXPERIMENTALLY VALIDATED** siguen **NOT_VERIFIED**.
- Se cambió el siguiente paso de cinco casos indefinidos a los tres casos sintéticos publicados más datasets/casos publicados que se seleccionen con referencias antes del benchmark.

## Conclusión del revisor

**Disposición: RESEARCH FURTHER.** Un MVP general de matching duplicaría capacidades publicadas; no hay evidencia de demanda o diferencia de rendimiento. La decisión podría cambiar si el benchmark muestra ventaja repetible en datos incompletos, incertidumbre y motivos de inviabilidad, y si usuarios técnicos confirman que esa ventaja cambia una decisión.

## Revisión adversarial de la comparación documental

La comparación añadida al informe es documental, no una prueba cruzada: OpenPinch documenta targeting directo, screening de bombas de calor y análisis multiperiodo; eso respalda solapamiento funcional en A/B y periodos de C, pero no equivale a ejecutar `case-inputs.csv`. No atribuir a OpenPinch despacho TES porque las fuentes revisadas no lo establecen. **Corrección crítica:** EMB3Rs TEO sí documenta optimización de almacenamiento térmico con operación temporal, capacidades y límites de carga/descarga; el manual D3.4 explica la función y parámetros. Debe reconocerse en la tabla, distinguiéndolo de estratificación/perfiles de temperatura y validación del TES sintético concreto, que no se han verificado. [Repo TEO](https://github.com/Emb3rs-Project/p-teo), [manual D3.4](https://www.emb3rs.eu/wp-content/uploads/2022/11/D3.4_M38_submitted.pdf). EMB3Rs no se ejecutó aquí. La diferencia comercial sugerida sigue **HYPOTHESIS**. **NOT_VERIFIED:** precisión comparada, fidelidad termodinámica del TES, esfuerzo de modelado y ventaja de ThermoGap.

**Tres riesgos principales:** (1) errores de approach/COP producen un falso positivo termodinámico, demostrado por el fallo original B; (2) los perfiles TES y costos pueden crear una falsa economía; (3) la diferenciación y compra siguen sin verificarse frente a competidores directos.
