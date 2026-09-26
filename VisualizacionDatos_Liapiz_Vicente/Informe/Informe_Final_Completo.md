# Evaluación Sumativa Unidad 1: Informe Final

**Estudiante:** Vicente Jesús Liapiz Ávila

---

## PARTE II: Análisis Crítico de Visualizaciones Reales

### Visualización 1: Dashboard de IPC e Inflación (INE Chile)
**1. Descripción:** 
* **Fuente:** Instituto Nacional de Estadísticas (INE) Chile, sección de series estadísticas.
* **Contexto:** Reporte mensual de las variaciones del Índice de Precios al Consumidor (IPC).
* **Audiencia objetivo:** Economistas, periodistas financieros y ciudadanos interesados en el costo de vida.

**2. Evaluación Técnica:**
* **Tipo de gráfico:** Gráfico de líneas interactivo con áreas sombreadas.
* **Variables representadas:** Tiempo (eje X, meses/años) y Variación Porcentual (eje Y).
* **Calidad de representación:** Alta precisión, datos limpios (estructurados).
* **Nivel de complejidad:** Intermedio. Requiere noción básica de porcentajes y acumulación.

**3. Evaluación Crítica:**
* **Claridad visual:** El gráfico es minimalista, evitando el uso excesivo de "tinta de datos".
* **Buenas prácticas:** Utiliza etiquetas claras al hacer *hover* (interacción). 
* **Posibles problemas:** Al mostrar múltiples divisiones (alimentos, transporte, etc.) en un solo recuadro, las líneas se cruzan y generan "efecto espagueti".
* **Posibles sesgos:** Escala del eje Y. Si no empieza en 0 o si se ajusta automáticamente, puede exagerar la percepción de la inflación.

**4. Propuesta de Mejora:**
* **Qué modificaría:** En lugar de un solo gráfico con muchas líneas, utilizaría *Small Multiples* (pequeños múltiplos) para separar las divisiones de consumo en cuadrículas individuales.
* **Qué eliminaría:** Eliminaría las líneas de cuadrícula secundarias (gridlines) que generan ruido visual.
* **Justificación técnica:** Aplicando principios de [[Diseño de Información]] y reduciendo la carga cognitiva del [[Usuario]], facilitando la comparación independiente de tendencias.

---

### Visualización 2: Mapa Global de Riesgos 2026 (Foro Económico Mundial)
**1. Descripción:**
* **Fuente:** World Economic Forum (WEF) Global Risks Report.
* **Contexto:** Mapeo de la percepción global de riesgos económicos, ambientales y tecnológicos a corto y largo plazo.
* **Audiencia objetivo:** Líderes gubernamentales, directores ejecutivos (CEOs) e investigadores.

**2. Evaluación Técnica:**
* **Tipo de gráfico:** Gráfico de red (Network Graph) y gráfico de burbujas.
* **Variables representadas:** Tipo de riesgo (color), impacto/probabilidad (tamaño de burbuja) y fuerza de interconexión (grosor de línea).
* **Calidad de representación:** Alta resolución, pero visualmente muy densa.
* **Nivel de complejidad:** Muy alto (multivariable).

**3. Evaluación Crítica:**
* **Claridad visual:** Es visualmente impactante, pero analíticamente confuso de leer de un vistazo.
* **Buenas prácticas:** Buen uso de la teoría del color categórico (verde para clima, azul para economía, morado para tecnología).
* **Posibles problemas:** Sobreposición de nodos y enlaces cruzados imposibles de seguir.
* **Posibles sesgos:** El tamaño de las burbujas (área) muchas veces es mal interpretado por el cerebro humano comparado con longitudes.

**4. Propuesta de Mejora:**
* **Qué modificaría:** Cambiaría el mapa de red estático por un panel interactivo que resalte solo los nodos conectados al hacer clic.
* **Qué agregaría:** Un gráfico de barras horizontales ordenadas (ranking) acompañando a la red para facilitar la lectura del top 10 de riesgos de forma lineal.
* **Justificación técnica:** Basado en las [[Buenas Prácticas]] de la [[Visualización de Datos]], los humanos comparan longitudes más fácilmente que áreas o ángulos. El [[Storytelling]] requiere guiar al lector, no abrumarlo.

---

### Visualización 3: Panel de Monitoreo Epidémico (Dashboard de Salud Pública)
**1. Descripción:**
* **Fuente:** Dashboard tipo John Hopkins o plataformas ministeriales de salud.
* **Contexto:** Monitoreo en tiempo real de brotes, casos activos y tasas de recuperación.
* **Audiencia objetivo:** Autoridades de salud pública, medios masivos y público general.

**2. Evaluación Técnica:**
* **Tipo de gráfico:** Mapa de coropletas (Heatmap geográfico) combinado con KPIs numéricos masivos.
* **Variables representadas:** Ubicación geográfica, intensidad de casos (gradiente de color) y métricas acumuladas.
* **Calidad de representación:** Datos integrados mediante APIs en tiempo real.
* **Nivel de complejidad:** Bajo/Medio (muy intuitivo por asociación geográfica).

**3. Evaluación Crítica:**
* **Claridad visual:** El uso de un mapa es muy natural para el [[Usuario]] común.
* **Buenas prácticas:** Destaca los números más importantes en la parte superior (KPIs).
* **Posibles problemas:** Usar colores muy dramáticos (como rojo oscuro a negro) puede generar pánico injustificado.
* **Posibles sesgos:** Los mapas de coropletas absolutos tienden a mapear densidad poblacional. Regiones grandes se ven más amenazantes incluso si tienen pocos casos per cápita.

**4. Propuesta de Mejora:**
* **Qué modificaría:** Normalizar los datos. En lugar de mostrar "Total de Casos", mostrar "Casos por cada 100.000 habitantes".
* **Qué cambiaría:** Ajustar la paleta de colores secuencial a tonos más neutrales (ej. azul oscuro a azul claro) para evitar semiótica del miedo.
* **Justificación técnica:** Una correcta [[Calidad de Datos]] exige normalización. Desde la [[Comunicación Visual]], el color tiene peso emocional que debe gestionarse con responsabilidad ética.

---

## PARTE III: Ensayo Reflexivo Profesional

**¿Cómo contribuye la visualización de datos a transformar datos en conocimiento útil para la toma de decisiones en una organización?**

En la actual era digital, las organizaciones generan volúmenes masivos de datos estructurados y no estructurados. Desde la infraestructura en la nube gestionada en Google Cloud o AWS, hasta los registros transaccionales bancarios o las interacciones de un usuario en una aplicación móvil, el flujo de información es incesante. Sin embargo, como establece Ignasi Alcalde Perea en su obra *"Visualización de la información: De los datos al conocimiento"*, los datos por sí solos carecen de significado. Es aquí donde la visualización de datos emerge no como un simple ejercicio estético, sino como una herramienta estratégica de traducción y síntesis cognitiva.

Para ilustrar este fenómeno, es útil recurrir al modelo DIKW (Datos, Información, Conocimiento, Sabiduría). Tomemos como ejemplo el desarrollo de sistemas de monitoreo técnico y auditoría, como el proyecto Audit-AI en el que he trabajado utilizando entornos de ejecución como Node.js y bases de datos relacionales como PostgreSQL. Estos sistemas recopilan miles de filas de *logs*, eventos de navegador y marcas de tiempo. Analizar tabularmente estos datos puros es humanamente ineficiente. La visualización de datos actúa como el catalizador que convierte esos registros brutos en información estructurada, utilizando gráficos y dashboards para revelar patrones de comportamiento.

Una vez que la información es visual (por ejemplo, identificando un pico anómalo de actividad a través de un gráfico de series de tiempo), el usuario o auditor puede aplicar su contexto, experiencia y marcos teóricos (como el modelo UTAUT para entender el comportamiento de aceptación tecnológica). Es en este preciso instante donde ocurre la verdadera alquimia: la información se transforma en **conocimiento**. Este conocimiento es accionable; permite a los tomadores de decisiones identificar fraudes, optimizar recursos de infraestructura en servidores o mejorar la integridad de un proceso. 

Además, la visualización fomenta la democratización de los datos. En una organización, no todos los directivos poseen habilidades en Ciencia de Datos o entienden consultas SQL complejas. El diseño de información efectivo, que respeta las buenas prácticas de carga cognitiva y percepción visual (Gestalt), actúa como un puente. Herramientas de visualización modernas permiten aplicar técnicas de *Storytelling*, guiando al espectador a través de una narrativa lógica que justifica una inversión o un cambio de estrategia comercial. 

En conclusión, la visualización de datos es el eslabón crítico en la cadena de valor de la analítica. Reduce la asimetría de información dentro de las organizaciones, mitiga la incertidumbre y acelera drásticamente el proceso mediante el cual los números abstractos se convierten en decisiones ejecutivas fundamentadas, seguras e impactantes.

---

## PARTE IV: Reflexión sobre Gestión del Conocimiento Digital

**¿Cómo aportan Obsidian y GitHub a la construcción y gestión del conocimiento en proyectos de Ciencia de Datos?**

La gestión moderna del conocimiento requiere herramientas que superen la linealidad de los procesadores de texto tradicionales. En proyectos de Ciencia de Datos o Arquitectura de Software, donde los conceptos, códigos, algoritmos y métricas están intrínsecamente entrelazados, la combinación de Obsidian y GitHub representa un ecosistema de documentación sumamente robusto.

Obsidian, al basarse en archivos Markdown locales y utilizar un modelo de red interconectada (Graph View), simula la manera en que el cerebro humano asocia ideas. En lugar de archivar documentos en carpetas jerárquicas rígidas, permite crear enlaces bidireccionales. Esto es vital para la **organización del conocimiento** y la **documentación técnica**: un concepto estadístico sobre limpieza de datos puede vincularse directamente a una nota sobre scripts de Python o queries en bases de datos PostgreSQL. No existen silos de información; todo es una bóveda orgánica donde el aprendizaje significativo se hace visualmente evidente.

Por su parte, GitHub aporta la columna vertebral del **trabajo colaborativo**, la **reproducibilidad** y la **trazabilidad del aprendizaje**. En la ciencia de datos, mantener el control de versiones no solo aplica al código fuente, sino también a la documentación y a los modelos de análisis. Realizar *commits* periódicos permite registrar la evolución del pensamiento crítico y técnico del desarrollador o del equipo. Si un marco conceptual cambia o un análisis se actualiza, Git preserva el historial, permitiendo auditar por qué se tomaron ciertas decisiones de diseño en el pasado.

En conjunto, mientras Obsidian empodera la síntesis cognitiva y el relacionamiento abstracto individual, GitHub estructura, distribuye y asegura el proyecto. Ambas herramientas garantizan que el conocimiento generado en una organización o investigación no dependa de plataformas propietarias cerradas, sino que se mantenga trazable, auditable y listo para escalar en cualquier entorno profesional.
