# ThermoGap — rutas realistas para aprovechar calor residual

**Fecha:** 15 de octubre de 2026  
**Alcance:** revisión documental para Estados Unidos, Europa y Canadá. No usa datos de una planta real concreta.

## Resumen sencillo

El calor residual puede ayudar a fabricar productos o prestar servicios. Pero el calor por sí solo no fabrica nada. Hace falta una planta, materia prima, equipos, compradores y un suministro de calor compatible.

Las rutas más realistas son:

1. Usar el calor en la misma fábrica para reducir combustible comprado.
2. Elevar su temperatura con una bomba de calor y alimentar un proceso que ya existe.
3. Vender calor a una fábrica, edificio o red cercana con demanda estable.
4. Usarlo para secar un producto o subproducto que ya tenga comprador.

Otras rutas pueden servir en ciertos sitios: producir frío, cultivar alimentos, recuperar agua, guardar calor o generar electricidad. No son buenas por defecto.

El Departamento de Energía de EE. UU. estima que entre el 20 % y el 50 % de la energía industrial de entrada puede salir como calor residual. Es una estimación general. No significa que esa fracción pueda recuperarse con beneficio en una planta concreta. El propio DOE cita barreras como materiales, corrosión y mantenimiento. [DOE, Waste Heat Recovery Basics](https://www.energy.gov/cmei/ito/waste-heat-recovery-basics)

## Mapa de opciones

| Ruta | Qué puede producir o mejorar | Cuándo puede funcionar | Motivo común para descartarla | Prioridad inicial de cribado* |
|---|---|---|---|---|
| Reuso dentro de la misma fábrica | Agua caliente, agua de lavado, aire de combustión, alimentación de caldera, material precalentado o aire de secado | Hay una demanda cercana y simultánea, y el calor tiene temperatura suficiente | Horarios distintos, suciedad, corrosión, caída de presión o poco espacio | Muy alta |
| Bomba de calor industrial | Agua caliente, aire caliente, secado o vapor de proceso | Hay calor residual estable y electricidad competitiva; la temperatura requerida es alcanzable | Mucha elevación de temperatura, electricidad cara, pocas horas o proceso difícil de integrar | Alta, según el caso |
| Venta de calor a otra planta | Calor o vapor como servicio; ayuda a fabricar malta, papel, alimentos, químicos u otros productos existentes | Comprador cercano, consumo estable, tubería viable, respaldo y contrato | Distancia, parada de una de las plantas, falta de comprador o coste de red | Alta si hay comprador firme |
| Calefacción de edificios o red local | Calefacción y agua caliente | Hay edificios cercanos con consumo durante la temporada útil | Red cara, verano sin demanda, respaldo insuficiente o baja densidad de edificios | Alta en lugares con red y demanda; menor en otros |
| Secado de alimento, madera, papel, biomasa o lodo | Producto seco o subproducto más fácil de transportar o vender | Existe materia prima disponible y un comprador; temperatura y calidad son adecuadas | Coste de preparación, contaminación, normas, estacionalidad o producto sin mercado | Media-alta; validar comprador primero |
| Calor para cultivo protegido, hidroponía o acuicultura | Verduras, plantas, peces u otros productos | Hay calor templado estable, agua, espacio y mercado local | El calor no es el coste principal; producción, iluminación, personal, agua y ventas pueden dominar | Media-baja, sitio específico |
| Refrigeración por absorción | Agua fría para cámaras, proceso o climatización | Hay una fuente de calor suficientemente caliente y demanda de frío coincidente | Calor de baja temperatura, falta de torre de refrigeración, carga pequeña o consumo eléctrico auxiliar | Media-baja |
| Almacenamiento térmico | Calor desplazado a otra hora o, en algunos diseños, transportado | Hay desajuste temporal y el valor del calor justifica tanque, batería térmica o logística | Pérdidas, coste, poco espacio, potencia insuficiente o demasiados ciclos | Complementaria |
| Recuperar agua de gases de escape industriales | Agua de proceso; a veces nutrientes recuperados | Hay vapor/agua residual adecuada, tratamiento viable y el agua tiene valor local | Contaminantes, corrosión, calidad, permisos o escala insuficiente | Nicho o demostración |
| Recuperar condensado o tratar agua de proceso | Agua reutilizada en la instalación | El sistema de agua y la calidad requerida permiten reutilizarla | Contaminación, calidad insuficiente o coste de tratamiento | Tecnología madura en aplicaciones adecuadas |
| Electricidad | Electricidad neta de un ciclo de vapor u ORC | Mucho calor, temperatura y horas; no hay mejor uso térmico; cotización favorable | Baja eficiencia neta, auxiliares, condensación, mantenimiento o instalación pequeña | Baja salvo fuentes grandes y estables |
| Nuevos procesos químicos | Combustibles, materiales u otros productos | El calor alcanza el nivel requerido y existe materia prima, reactor, permisos y cliente | El proceso puede requerir más energía y capital que el valor del calor | No priorizar sin estudio industrial específico |

**ORC** significa ciclo Rankine orgánico. Es una máquina que puede producir electricidad con calor.  
**Absorción** significa producir frío usando calor en lugar de depender solo de un compresor eléctrico.

\* Estas prioridades son una **heurística de cribado**, no un ranking de rentabilidad. No se compararon tarifas, ayudas, cotizaciones, demanda ni sitios concretos en los tres mercados. El orden puede cambiar por temperatura, horarios, distancia, inversión, precio de energía y respaldo disponible.

## De dónde puede venir el calor

| Fuente industrial | Usos realistas a investigar | Límites importantes |
|---|---|---|
| Hornos, fundiciones, acero, cemento y vidrio | Precalentar carga o aire, generar vapor, secar, alimentar otra planta, calefacción local; electricidad solo con condiciones fuertes | Temperaturas altas ayudan, pero gases sucios, polvo, corrosión, seguridad y cambios de producción complican la recuperación |
| Calderas, motores y turbinas | Agua caliente, vapor, precalentamiento de alimentación, calefacción y generación eléctrica | No contar el calor ya aprovechado por economizador, cogeneración u otros equipos |
| Compresores | Calentar agua, aire de proceso o espacios; bomba de calor para demandas más calientes | Puede haber poco calor útil, temperatura baja o demanda fuera del horario de compresión |
| Refrigeración y cámaras frías | Agua caliente para lavado, procesos o edificios; a veces bomba de calor | El calor del condensador suele ser templado. No sirve automáticamente para pasteurizar o generar vapor |
| Secadores, papel, textiles, alimentos y madera | Recuperar calor del aire húmedo para precalentar aire, recircular energía o secar otra corriente | Humedad, polvo, olores y contaminación; el equipo debe resistir el proceso |
| Química y petroquímica | Integración entre corrientes, vapor, agua caliente, bombas de calor y redes de calor | Requiere propiedades de mezcla, fases, seguridad, presión y límites de operación del proceso |
| Aguas residuales y torres de refrigeración | Bomba de calor, agua caliente o recuperación de agua | Temperatura baja, ensuciamiento, corrosión y coste de tratamiento |
| Centros de datos y electrónica | Calefacción de edificios, agua caliente con bomba de calor, invernaderos u otros usuarios próximos | Normalmente calor de baja temperatura; la disponibilidad eléctrica del centro no garantiza que haya comprador de calor |

La lista de usos del DOE incluye agua de caldera, secado, precalentamiento de materiales, aire de combustión y líquidos de lavado. La temperatura y la curva de disponibilidad determinan qué opción puede funcionar. [DOE, Improving Process Heating System Performance](https://www.energy.gov/sites/default/files/2016/04/f30/Improving%20Process%20Heating%20System%20Performance%20A%20Sourcebook%20for%20Industry%20Third%20Edition_0.pdf)

## Qué productos comerciales son más creíbles

### 1. Producto existente fabricado con menos combustible

El calor se entrega a un proceso que ya existe. Ejemplos: secar malta, papel, alimentos, madera o materiales. El comprador ya vende el producto. El calor reduce el combustible que necesita.

Un caso europeo documenta calor de una fundición de aluminio enviado por una tubería de 1,2 km a una maltería para secar cebada. El caso es evidencia de una instalación descrita públicamente. Sus ahorros publicados no son una auditoría independiente. [ECCP, intercambio de calor industrial](https://www.clustercollaboration.eu/content/industrial-symbiosis-exchanging-heat)

### 2. Producto secundario obtenido por secado

Se puede investigar secar subproductos alimentarios, biomasa, lodos, madera o productos agrícolas. El resultado puede pesar menos, durar más o servir como materia prima. Eso no garantiza que se pueda vender. Hay que demostrar calidad, permisos, suministro y comprador.

Un estudio de Madrid analizó secar residuos alimentarios húmedos como coproducto. Es un modelo técnico-económico, no prueba de una planta comercial que funcione solo con calor residual. [Wallin et al., 2020](https://doi.org/10.3303/CET2081232)

### 3. Alimentos producidos junto a una fuente de calor

Un centro de datos puede aportar calor templado a cultivos protegidos. RISE describe una operación hidropónica dentro de un centro de datos sueco que suministraba lechuga a restaurantes. La fuente no publica cuentas independientes de rentabilidad. [RISE, 2022](https://www.ri.se/en/lettuce-and-servers-industrial-symbiosis-through-waste-heat-from-the-data-center)

### 4. Calefacción y agua caliente como servicio

El calor se vende o se factura mediante una red. El producto vendido es energía térmica. El usuario final puede ser una fábrica, un barrio, un hospital o edificios comerciales. Hay que calcular tubería, bombas, aislamiento, pérdidas, respaldo, medición y contrato.

En Canadá, el sistema Zibi usa calor residual de una papelera mediante bombas de calor para suministrar calefacción y agua caliente a edificios. La fase inicial está operativa. El tamaño total anunciado para la urbanización completa es una meta futura, no la capacidad actual. [Natural Resources Canada, Zibi](https://natural-resources.canada.ca/funding-partnerships/zibi-district-thermal-system)

### 5. Frío producido con calor

Un enfriador por absorción puede usar calor para producir agua fría. Puede interesar a fábricas de alimentos, almacenes refrigerados o procesos con demanda de frío. El DOE describe estos sistemas para refrigeración de proceso y edificios. Hay que comprobar la temperatura del calor, la demanda horaria y el calor que el propio enfriador debe rechazar. [DOE, absorption chillers](https://betterbuildingssolutioncenter.energy.gov/resources/combined-heat-and-power-technology-fact-sheet-absorption-chillers-chp-systems)

### 6. Electricidad

El calor puede generar electricidad con turbinas de vapor u ORC. La electricidad suele aprovechar solo una parte del calor. Por eso, si hay un proceso que pueda usar ese calor directamente, suele ser necesario comparar ambas opciones antes de elegir electricidad.

Canadá documentó un demostrador ORC en un sitio de motores de compresión en Alberta. El proyecto informó problemas de fiabilidad con un sello del eje y necesitó modificaciones. Es una prueba de posibilidad técnica en ese sitio, no una garantía de rentabilidad general. [NRCan, Great Northern Power](https://natural-resources.canada.ca/funding-partnerships/clean-power-waste-heat-recovery-reciprocating-engines)

## Evidencia por región

| Región | Evidencia concreta | Qué indica |
|---|---|---|
| Estados Unidos | Waupaca Foundry informa que calor recuperado regenera un secador de aire para el horno. El socio reporta ahorros de energía, reducción de coque e inversión con recuperación simple en 3,8 años. La página aclara que es información del socio, no un aval del DOE ni una auditoría independiente. No es un promedio de fundiciones. [DOE Better Buildings](https://betterbuildingssolutioncenter.energy.gov/showcase-projects/waupaca-foundry-cupola-furnace-blast-air-dehumidification-improvement) | El reuso interno para mejorar una operación existente tiene un caso concreto. Sus cifras económicas deben verificarse antes de usarlas como referencia. |
| Europa | DryFiciency reportó demostraciones industriales de bombas de calor para secado hasta 160 °C; sus dos sistemas de circuito cerrado superaron 4.000 horas cada uno, con COP reportado de 2 a 5 según condiciones. Son resultados de un proyecto europeo y no valores universales. [CORDIS](https://cordis.europa.eu/project/id/723576/reporting/fr) | Una bomba de calor puede convertir calor residual en calor de proceso de mayor temperatura. Hay que calcular consumo eléctrico y condiciones reales. |
| Europa | La fundición Aleris y la maltería Avangard documentan suministro de calor mediante tubería. [ECCP](https://www.clustercollaboration.eu/content/industrial-symbiosis-exchanging-heat) | Vender calor a una planta próxima puede sostener un producto existente, si ambas empresas coordinan operación y contrato. |
| Canadá | Zibi usa calor de una papelera para calefacción y agua caliente con bombas de calor. [NRCan](https://natural-resources.canada.ca/funding-partnerships/zibi-district-thermal-system) | El calor industrial puede convertirse en un servicio local de calefacción. La red y los edificios cercanos son parte central del proyecto. |
| Canadá | NRCan documentó un demostrador ORC con motor de compresión en Alberta. [NRCan](https://natural-resources.canada.ca/funding-partnerships/clean-power-waste-heat-recovery-reciprocating-engines) | La generación eléctrica es posible en casos concretos, con riesgo de fiabilidad y mantenimiento. |

Estos ejemplos no permiten afirmar qué región tiene el mejor mercado. No se hizo un estudio comparable de precios de energía, ayudas, impuestos, red térmica o demanda por país.

## Filtro científico y económico

ThermoGap debería descartar una idea si no supera estas preguntas:

1. **¿Cuánto calor hay de verdad?** Medir caudal, temperatura y horas. Calcular la energía con propiedades adecuadas del fluido.
2. **¿A qué temperatura puede entregarse?** El calor fluye de caliente a frío. Hace falta una diferencia de temperatura para intercambiarlo.
3. **¿Coincide con el usuario?** Un calor disponible de noche no cubre una demanda que solo opera de día, salvo que almacenamiento o una bomba de calor lo hagan viable.
4. **¿Se puede integrar sin dañar el proceso?** Comprobar presión, caída de presión, corrosión, ensuciamiento, higiene, seguridad y control.
5. **¿Qué producto o servicio compra alguien?** Un producto nuevo requiere materia prima y comprador. El calor no sustituye esos requisitos.
6. **¿Cuál es el coste total?** Incluir intercambiadores, tuberías, bombas, bomba de calor, almacenamiento, instalación, electricidad, mantenimiento, respaldo, permisos y paradas.
7. **¿Qué energía se ahorra realmente?** Informar por separado calor capturado, calor entregado, combustible evitado, electricidad añadida, coste neto y emisiones netas.

El **COP** de una bomba de calor es el calor entregado dividido por la electricidad consumida. Cambia con la temperatura de origen y de entrega. No debe copiarse como un número fijo de catálogo.

## Revisión crítica independiente

Un revisor independiente comprobó estas rutas y destacó estos límites:

- El primer paso es buscar reuso directo dentro de la fábrica. El total de calor rechazado no equivale al calor recuperable.
- Las bombas de calor y el almacenamiento pueden resolver algunos problemas de temperatura u horario. Añaden electricidad, pérdidas, inversión y mantenimiento.
- La venta a otra empresa requiere distancia corta, demanda firme, tubería, respaldo y contrato. En una revisión de 45 casos externos austríacos, 42 servían redes de calefacción y solo 3 a otras empresas industriales. Ese resultado no representa todas las regiones, pero advierte que el intercambio empresa-a-empresa no es automáticamente habitual. [Moser y Jauschnik, 2023](https://doi.org/10.3390/su151310559)
- La refrigeración por absorción requiere calor y demanda de frío compatibles. El calor templado de un condensador no sirve automáticamente.
- La electricidad de calor residual solo merece estudio cuando fuente, temperatura, tamaño y horas justifican equipos y mantenimiento. Comparar producción eléctrica neta, no bruta.
- Recuperar agua o crear cultivos puede funcionar como proyecto local, pero la evidencia encontrada consiste principalmente en proyectos y casos concretos. No es un mercado probado para toda fábrica.
- EMB3Rs documenta emparejamiento de fuentes y usuarios, perfiles de carga, modelos técnicos y económicos, costes y pérdidas de redes, almacenamiento y métricas financieras. SymbiosisMatch describe cribado de sinergias de energía y carbono, calor, almacenamiento e infraestructura compartida. La idea de ThermoGap no es original solo por combinar fuentes y usuarios, horarios o costes. Para alegar una diferencia haría falta comparar función por función y comprobar, sin presumirlo, si hay vacíos en incertidumbre de medición, explicación auditable de descartes, privacidad local u otros puntos. [EMB3Rs](https://www.emb3rs.eu/platform/), [resultados EMB3Rs](https://www.emb3rs.eu/results/), [SymbiosisMatch](https://www.sdu.dk/en/forskning/centreforenergyinformatics/software-solutions/symbiosismatch)

**Conclusión crítica:** los mejores casos iniciales son la mejora interna y el calor para un proceso próximo que ya tiene producto y comprador. Las rutas de cultivo, agua, frío o electricidad se evalúan solo cuando un sitio concreto justifique el estudio.

## Estado de conocimiento

- **VERIFIED:** existen casos y demostraciones documentados para reuso interno, bombas de calor industriales, suministro de calor a edificios o procesos, secado, cultivos y ORC.
- **OBSERVED:** las fuentes públicas consultadas describen proyectos, equipos o resultados comunicados por participantes.
- **INFERRED:** la ruta más sólida para un primer análisis comercial es comparar reuso interno, bomba de calor y comprador térmico cercano antes de proponer un producto nuevo.
- **HYPOTHESIS:** ThermoGap podría ayudar si presenta los datos, supuestos e incertidumbre de forma auditable y explica por qué una opción falla. No se ha demostrado que esa combinación sea distinta de las herramientas existentes.
- **NOT_VERIFIED:** demanda de clientes, disposición a pagar por ThermoGap, tamaño de mercado comparable entre países y rentabilidad de cualquier sitio futuro.

## Aprendizajes que se deben conservar

| Campo | Resultado |
|---|---|
| **LEARNING** | Las rutas de valorización realistas incluyen ahorro interno, calor como servicio, calor para productos existentes, secado de coproductos, cultivos, frío, electricidad, agua y almacenamiento. No tienen igual madurez. |
| **EVIDENCE** | Fuentes oficiales de DOE y NRCan, CORDIS, RISE, ECCP, un artículo revisado por pares y revisión crítica independiente. Véanse enlaces en cada sección. |
| **IMPACT** | ThermoGap debe puntuar el caso concreto y no anunciar que todo calor residual puede transformarse en un producto rentable. |
| **CONFIDENCE** | Alta en las leyes físicas y en que existen las demostraciones citadas. Media en la prioridad relativa de rutas. Baja en tamaño de mercado y rentabilidad futura. |
| **CARRY_FORWARD** | Usar perfiles horarios, curvas de temperatura, pérdidas, potencia, costes totales y comprador/uso final como datos mínimos. |
| **UNRESOLVED** | No se compararon precios actuales, incentivos elegibles desde España, cotizaciones de equipos ni clientes en los tres mercados. No se ejecutó un modelo numérico ni se verificaron datos de una planta. |

## Decisión actual

**RESEARCH FURTHER.** Hay oportunidades físicas y casos reales. Aún no está probado que ThermoGap tenga una ventaja comercial frente a herramientas existentes ni que clientes paguen por ella. El siguiente análisis útil sería elegir un sector y comparar proyectos con datos horarios y cotizaciones reales autorizadas.
