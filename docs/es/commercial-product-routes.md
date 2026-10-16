# ThermoGap — calor residual como insumo para productos comerciales

**Fecha de revisión:** 15-10-2026  
**Conclusión corta:** Sí existen vías comerciales para transformar calor residual en ingresos o en productos vendibles. La evidencia más sólida corresponde a suministrar calor a una fábrica vecina que ya fabrica un producto, y a usar calor de baja temperatura de un centro de datos en horticultura. Convertir residuos en nuevos productos mediante secado es prometedor, pero la prueba de escala y rentabilidad depende mucho del caso. No se ha demostrado una ventaja de ThermoGap frente a las herramientas recientes de simbiosis industrial.

> **Actualización del alcance:** el usuario precisó que el producto adicional debe fabricarse en la misma fábrica que genera el calor. Por eso, los ejemplos de venta de calor a otra empresa o a redes externas que aparecen en este informe ya no cumplen el requisito principal. Véase el análisis actualizado [Producto nuevo en la misma fábrica](same-factory-new-product.es.md).

## Qué significaría la idea

ThermoGap no tendría que ser solo un calculador de ahorro. Su objeto sería hallar y evaluar **rutas de valorización**: qué producto o servicio puede salir de una nueva operación alimentada por calor residual, quién lo compraría, qué alimentación y equipos requiere, y si el margen neto justifica la instalación.

Hay dos modelos de negocio que deben mantenerse separados:

1. **Vender calor útil** a una planta existente. El producto —por ejemplo, malta— ya tiene proceso y comprador. La fábrica que genera calor obtiene ingresos por el suministro y la receptora reduce combustible.
2. **Crear una operación secundaria** que fabrica un producto con ese calor, como cultivos de invernadero, biomasa seca o un subproducto alimentario deshidratado. Aquí hay que probar además el suministro del material, calidad, permisos, logística y venta del producto.

## Casos y evidencia

| Ruta | Evidencia encontrada | Qué está demostrado y qué no |
|---|---|---|
| Fundición de aluminio → secado de malta | La plataforma de clúster de la Comisión Europea describe un circuito cerrado de agua caliente por tubería de 1.200 m entre Aleris y Avangard Malz. La maltería sustituyó gas para secar cebada y el fundidor pudo obtener ingresos por calor que antes no utilizaba. Reporta unas 5.000 tCO₂/año evitadas. [Caso ECCP](https://www.clustercollaboration.eu/content/industrial-symbiosis-exchanging-heat) | **VERIFIED como caso documentado**, no como auditoría independiente. Es la evidencia más clara de que el calor residual puede ser un insumo vendible para un producto comercial existente. También indica inversión e infraestructura altas; no es una oportunidad replicable sin distancia, calidad térmica y comprador adecuados. |
| Calor de centro de datos → cultivos hidropónicos | RISE informa que el aire del centro de datos está aproximadamente a 30–45 °C; comunicó un ensayo de secado de biomasa para biocombustible que llegó a usar hasta 40 % del excedente térmico. También describe a Containing Greens operando cultivos hidropónicos verticales en un centro de datos y entregando lechuga a restaurantes locales. [RISE, 29-05-2022](https://www.ri.se/en/lettuce-and-servers-industrial-symbiosis-through-waste-heat-from-the-data-center) | **VERIFIED como actividad/caso descrito por el instituto**, pero no se publican aquí cuentas, volumen comercial, margen o replicabilidad independiente. Demuestra que el calor templado puede incorporarse a una operación que vende alimento; no acredita rentabilidad universal. |
| Calor residual + secado de subproducto alimentario | El estudio DRALOD plantea deshidratar residuos alimentarios húmedos para venderlos como coproducto conservando nutrientes. Modela recuperación de calor, scrubber y bomba de calor con clima horario de Madrid; el desempeño económico depende mucho de los precios de electricidad y biocombustible. [Wallin et al., 2020](https://doi.org/10.3303/CET2081232) | **VERIFIED como estudio técnico-tecnoeconómico**, no como planta comercial alimentada solo con calor residual. La ruta de producto existe en el diseño; el artículo evalúa integración y economía bajo supuestos. Los umbrales de precios son específicos del caso. |
| Calor de 40–70 °C → regeneración de desecante para secado agrícola | EU CAP Network describe el uso de soluciones salinas higroscópicas para reducir humedad y secar a baja temperatura; calor residual puede regenerar el fluido y almacenarse químicamente para desacoplar horario. Incluye escenarios de invernaderos españoles e italianos. [TheGreefa](https://eu-cap-network.ec.europa.eu/projects/thermochemical-fluids-greenhouse-farming-thegreefa_en) | **VERIFIED como proyecto/estudio**, no como despliegue comercial probado. Sugiere una vía para calor de baja temperatura, pero calidad del cultivo, inversión y demanda local deben comprobarse por cliente. |
| Bomba de calor para secado de malta | Ficha histórica CORDIS describe una instalación de 3,5 MW; alcanzó COP de diseño 4,5 durante operación, pero sufrió corrosión irreparable en el evaporador, problemas de integración y límites de potencia, que obligaron a cambiar la fuente de calor. [CORDIS, proyecto 1981–1985](https://cordis.europa.eu/project/id/EE.-00225-81) | **VERIFIED como control negativo**: aun cuando el calor puede servir para fabricar malta, incompatibilidad de materiales e integración puede parar la instalación y destruir la economía prevista. El caso no representa tecnología actual, pero el mecanismo de fallo sigue siendo pertinente. |

## ¿Hay un hueco de producto para ThermoGap?

No basta con decir «descubrimos un producto para cada calor». Ya existen herramientas de simbiosis térmica y comercialización:

- **EMB3Rs** modela matching entre fuentes y sumideros, perfiles, tecnologías, red, mercado y métricas de negocio para vender/comprar calor. Su documentación es amplia, pero no se ejecutó aquí con casos ThermoGap. [Plataforma](https://www.emb3rs.eu/platform/)
- **SymbiosisMatch**, descrito por la Universidad del Sur de Dinamarca y actualizado en septiembre de 2026, hace cribado de simbiosis de calor, CO₂, residuos orgánicos y almacenamiento; clasifica alternativas y reporta ahorro, retorno y confianza. Esto hace que un producto genérico de “matching + ranking” no sea una diferenciación sustentable. La página institucional describe capacidades, no una validación independiente de resultados. [SDU SymbiosisMatch](https://www.sdu.dk/en/forskning/centreforenergyinformatics/software-solutions/symbiosismatch)
- **INCUBIS** muestra que ejecutar estos proyectos también exige facilitación, análisis técnico-económico/regulatorio, contratos, coordinación, permisos y financiación. No es solo un problema de cálculo. [INCUBIS](https://incub-is.eu/)
- Una herramienta de simbiosis para subproductos materiales (IWMM) ya calcula emparejamientos de residuos con materias primas y beneficios económicos, aunque su foco publicado son corrientes acuosas y materiales, no calor. [Artículo revisado por pares, 2024](https://doi.org/10.3389/fceng.2024.1363888)

Un estudio de Austria identificó 45 cooperaciones implementadas de calor residual externo, de las cuales 42 suministraban redes de calefacción urbana y solo 3 empresas externas independientes. El estudio no pudo determinar la rentabilidad de todos los casos con la información disponible. Esto demuestra que existen proyectos, pero que las oportunidades típicas no necesariamente son nuevas fábricas de producto. [Moser y Jauschnik, 2023](https://doi.org/10.3390/su151310559)

**HYPOTHESIS de diferenciación:** enlazar perfil térmico medido → proceso secundario concreto → alimentación material y especificación de producto → mercado/offtake → margen neto, dejando explicables los descartes y la calidad de evidencia. Debe probarse frente a SymbiosisMatch, EMB3Rs y una evaluación humana de ingeniería. No hay evidencia aún de que estas herramientas no puedan representar esa cadena mediante inputs de usuario.

## Filtro de decisión para cada producto

ThermoGap debería descartar una ruta si falla cualquiera de estos puntos:

1. Temperatura y caudal sostienen el proceso receptor durante sus horas de uso; si no, evaluar bomba de calor/almacenamiento con balances y consumos explícitos.
2. El valor horario y estacional del calor coincide con el suministro de materia y con producción/venta. No contar el calor fuera de temporada.
3. La materia prima secundaria está disponible con calidad, contrato y volumen suficiente; el calor por sí solo no crea un producto.
4. La salida cumple calidad, inocuidad, emisiones, normativa y requisitos del comprador.
5. Ingresos del producto o del calor más energía comprada evitada cubren electricidad auxiliar, captación, HX/bomba, conducción, almacenamiento, operación, transporte, calidad, mantenimiento y CAPEX.
6. La comparación usa una base sin recuperación y mantiene separados ingreso por producto, ingreso por calor, combustible evitado, electricidad añadida y emisiones.

La fórmula de screening sería:

`margen incremental = ingreso neto del producto nuevo + ingreso por calor + coste energético evitado − OPEX incremental − anualidad de CAPEX − logística/calidad/permiso`

No se deben sumar dos veces los ahorros: si el calor se vende a otra planta, el mismo MWh no puede contabilizarse a la vez como ingreso íntegro del vendedor y combustible ahorrado íntegro del comprador en el total del proyecto.

## Prioridad preliminar y límites

1. **Prioridad para primer caso:** integrar calor a una demanda que ya fabrica y vende algo (secado de malta u otro proceso térmico próximo). La demanda y mercado de producto existen; falta probar ubicación y economía de cada pareja.
2. **Ruta de innovación a explorar:** secado de un subproducto agroalimentario o biomasa residual con calor de baja temperatura y/o bomba de calor. Tiene una cadena de valor plausible y referencia en España, pero necesita comprador, especificación y ensayo de calidad antes de inversión.
3. **Ruta dependiente de lugar y clima:** invernadero/hidroponía, acuicultura o insectos. Puede monetizar calor templado con producto final, pero el negocio depende de ubicación, energía alternativa, cultivo/ciclo, bioseguridad y clientes; no asumir que calor gratis equivale a coste de producción bajo.

Los proyectos europeos muestran tanto ejemplos como hipótesis de demostración. No prueban que la venta de nuevos productos vaya a superar a la venta de calor o al ahorro energético en una planta concreta.

## Revisión crítica independiente

El subagente crítico revisó fuentes y conclusiones por separado. Se incorporan estos hallazgos:

- **VERIFIED con límites:** el DOE Better Buildings informa en General Mills/Cedar Rapids recuperación intraplanta para agua de ingredientes, deshumidificación y calor de refrigeración. La ficha combina ahorro esperado de ~$0,5 M/año y payback apenas superior a 3 años con coste de proyecto de $10 M; no aclara límites de alcance para conciliar las cifras. No usarlas como ROI de una sola medida. [Ficha DOE](https://betterbuildingssolutioncenter.energy.gov/node/255/pdf)
- **VERIFIED en muestra austríaca, no generalizable:** de 45 casos de calor externo, 42 eran redes de calefacción y 3 compañías externas independientes. Las negociaciones exigen relación de confianza, continuidad/respaldo, garantías, medición y asignación de responsabilidades. [Moser y Jauschnik, 2023](https://doi.org/10.3390/su151310559)
- **Caso documentado como proyecto/catalogación, no desempeño medido:** Val d’Europe planeó 4 km de red, 7,8 MW, aproximadamente 20 GWh/año, caldera de respaldo y €3,46 M de coste estimado, con €1 M de apoyo ADEME. Refuerza el peso de infraestructura y proximidad. [Comisión Europea Smart Cities Marketplace](https://smart-cities-marketplace.ec.europa.eu/insights/solutions/excess-heat-datacentre-val-deurope-france)
- **NOT_VERIFIED — indicador de proveedor requiere aclaración:** Carrier afirma COP >4,8 con calor residual cercano a 20 °C y agua de salida hasta 110 °C. Si esas temperaturas fueran los límites de la máquina y el COP fuera calefacción `Q_H/W`, supera Carnot entre esos depósitos (~4,26). No se debe usar el número como benchmark hasta aclarar condiciones y frontera del COP. [Carrier](https://www.carrier.uk/en/commercial/case-studies/high-temperature-heat-pump-solution-for-industrial-decarbonisation.html)
- **HYPOTHESIS:** ThermoGap parece más defendible como preauditoría local ligada a ingeniería, proveedor/instalador y offtake que como SaaS genérico de matching. No se encontró evidencia de compradores que paguen por un matcher independiente.
- **NOT_VERIFIED:** no hay comparación que pruebe una brecha frente a EMB3Rs o SymbiosisMatch en incertidumbre, razones de descarte o selección de producto.

## LEARN

- **LEARNING:** es posible generar ingresos vendiendo calor a un proceso que ya hace un producto y, en algunos contextos, integrar calor de baja calidad en horticultura o secado de subproductos. **EVIDENCE:** caso Aleris–Avangard, RISE/Boden, estudio DRALOD y TheGreefa. **IMPACT:** ThermoGap puede investigar rutas hacia producto/servicio, no limitarse a eficiencia dentro de una fábrica. **CONFIDENCE:** alta para que esos casos/rutas se han documentado; baja para su transferibilidad general. **CARRY_FORWARD:** mantener unidades de negocio separadas: vender calor vs fabricar producto. **UNRESOLVED:** márgenes auditados, operación continua, permisos y adopción por otros sitios.
- **LEARNING:** el matching y screening genéricos ya tienen competencia directa. **EVIDENCE:** EMB3Rs y SymbiosisMatch describen perfiles, ranking, almacenamiento y evaluación de negocio; INCUBIS cubre facilitación. **IMPACT:** no presentar software de matching como novedad. **CONFIDENCE:** alta sobre alcance anunciado, no sobre su precisión comercial independiente. **CARRY_FORWARD:** probar si ThermoGap conecta calor con producto y oferta comercial con mayor valor práctico. **UNRESOLVED:** si las herramientas existentes modelan toda la cadena con configuración ordinaria.

## Estado

**DONE:** investigación documental de rutas comerciales, casos industriales/institucionales, un control negativo técnico y herramientas de simbiosis existentes; revisión crítica independiente completada.  
**MISSING:** ejecución de herramientas competidoras; datos operativos y comerciales autorizados; compradores/ofertas/cotizaciones; validación de producto y planta.  
**CRITICAL FINDINGS:** (1) monetizar calor a través de un comprador próximo tiene precedentes; (2) producir un producto secundario añade riesgos de materia prima, calidad, permisos y mercado; (3) SymbiosisMatch, EMB3Rs e INCUBIS hacen que el software genérico de matching no sea una novedad demostrada.  
**NEXT ACTION:** escoger un par fuente–producto documentado en España y construir un caso base con datos trazables y sin cifras de rentabilidad inventadas.
