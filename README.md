# **Informe Global Music Streaming**

### **1. Contexto y Problema Actual**

Las plataformas de streaming musical enfrentan varios desafíos en la comprensión de **las preferencias y comportamientos de sus usuarios**. A pesar de contar con vastas bases de datos de reproducción, existe una falta de visibilidad clara sobre **los patrones de consumo musical** por demografía y región, lo que dificulta la **personalización de contenido** y la optimización de las estrategias de retención de usuarios.

A través de un análisis detallado de los datos globales de streaming y el comportamiento de los oyentes, se busca **identificar patrones específicos** que puedan ayudar a mejorar la experiencia del usuario y aumentar el engagement. Además, se necesita una herramienta visual que permita **monitorear y evaluar de manera continua** las métricas clave de negocio, como el tiempo de escucha, la efectividad del descubrimiento de música y las preferencias por géneros y artistas según diferentes segmentos demográficos.

### **2. Objetivo Principal del Proyecto**

El objetivo principal de este proyecto es crear **uno o varios dashboards interactivos** que faciliten la **visualización de datos relevantes** y proporcionen **insights prácticos** para la toma de decisiones estratégicas. Los dashboards permitirán a los equipos de producto y marketing:

-   **Identificar patrones de comportamiento** relacionados con el tiempo de escucha, preferencias de género y engagement con nuevas funcionalidades.

-   **Evaluar la efectividad de las recomendaciones** y el impacto de las listas de descubrimiento en las decisiones de consumo de los usuarios.

-   **Optimizar las estrategias de contenido** basándose en los intereses de diferentes segmentos de oyentes, para incrementar la retención y satisfacción del usuario.

En resumen, la creación de estos dashboards será clave para **mejorar la experiencia del usuario** y **reducir la incertidumbre en la toma de decisiones de producto**.


### **3. Estructura Repo**
```bash
├── data
├──── Global_Music_Streaming_Listener_Preferences.csv #Datos originales
└── Excels
├──── Carga_tranf_datos.xlsx #Excel con los Datos originales
```


### **4. Descripción de las Columnas del Conjunto de Datos**

El conjunto de datos contiene información detallada sobre los usuarios, sus hábitos de escucha y comportamiento en plataformas de streaming musical. A continuación, se presenta una breve descripción de las columnas más relevantes:

### **Datos de los Usuarios:**

-   **User_ID**: Identificador único del usuario.

-   **Age**: Edad del oyente.

-   **Country**: País de origen del usuario.

-   **Subscription_Type**: Tipo de suscripción (Free, Premium).

### **Datos de Consumo Musical:**

-   **Streaming_Platform**: Plataforma de streaming utilizada (Spotify, Apple Music, etc.).

-   **Top_Genre**: Género musical preferido del usuario.

-   **Most_Played_Artist**: Artista más reproducido por el usuario.

-   **Minutes_Streamed_Per_Day**: Minutos promedio de escucha diaria.

-   **Number_of_Songs_Liked**: Cantidad de canciones marcadas como favoritas.

### **Patrones de Comportamiento:**

-   **Listening_Time**: Momento preferido de escucha (Morning, Afternoon, Night).

-   **Discover_Weekly_Engagement**: Porcentaje de engagement con listas de descubrimiento semanal.

-   **Repeat_Song_Rate**: Porcentaje de repetición de canciones.

### **5. Recap versiones**
### Version 1
- Creación del repositorio
- Generación de archivo README
- Creación de informe mediante Claude.AI para simular Informe_Global_Music_Streaming
- Creación sistema carpetas del repo
- Se añadió el conjunto de datos original 'Global_Music_Streaming_Listener_Preferences.csv'
- Se creó el excel 'Carga_tranf_datos.xlsx', se cargó el conjunto de datos original mediante Power Query

### Version 2
- Se comprobó la presencia de duplicados. No se encontraron registros duplicados en el dataset.
- Se verificó la consistencia y completitud de los datos en todas las columnas principales.
- Se convirtieron los datos de "Hours Streamed Per Day" de minutos a formato decimal de horas.
- Se comprobaron los datos de "Age", "Number of Songs Liked", "Discover Weekly Engagement %" y "Repeat Song Rate %". Al ser columnas numéricas se verificó que no hubiera valores nulos o texto en dichas columnas.
- Se procesaron los datos de "Discover Weekly Engagement %" y "Repeat Song Rate %" convirtiéndolos a porcentajes legibles.
- Se categorizó la columna "Age" creando rangos de edad en "Age_Range": "Youth", "Young Adults", "Adults" y "Seniors".
- Se crearon las columnas categóricas "Discover Weekly_Categories" y "Repeat Song Rate_Categories" basadas en los valores porcentuales correspondientes.
- Se verificó la coherencia de los datos en las columnas "Streaming Platform", "Country", "Top Genre" y "Subscription Type".

### Version 3
- Se identificaron las variables de tipo numéricas (cuántitativas) y se realizaron sus respectivos análisis descriptivos.
- Se elaboraron tablas dinámicas y gráficos de caja (box plots) para cada variable numérica.
- En las variables "Age", "Number of Songs Liked", "Discover Weekly Engagement %" y "Repeat Song Rate %" se eliminaron todos los decimales de sus análisis descriptivos.
- Se establecieron tablas dinámicas por rangos para cada variable numérica.
- Los resultados de las tablas dinámicas se convirtieron al porcentaje total de las columnas para facilitar su interpretación.
- Se respetó la escala por defecto de cada gráfico de columnas, conservando el eje de los porcentajes.
### Version 4

- Se identificaron las variables de tipo categóricas del dataset.
- Se elaboraron tablas dinámicas para las variables: "Age_Range", "Country", "Streaming_Platform", "Discovery_Weekly_Categories", "Repeat_Song_Categories", "Music_Genre", "Subscription_Type", "Artist" y "Listening_time".
- Se crearon gráficos de columnas para cada variable categórica respetando su escala por defecto.
- Los gráficos se configuraron con porcentaje del total de columnas, manteniendo dos decimales por cada categoría.
- Se añadieron dos tablas dinámicas adicionales con categorías independientes de "USER_ID": "Discovery_Weekly_Categories" y "Repeat_Song_Categories".


### Version 5

- Se realizó un análisis bivariante sistemático entre las variables categóricas y numéricas clave del dataset para identificar patrones de comportamiento en el streaming musical.
- Se analizó la relación entre "Age_Range" y "Hours Streamed Per Day_Decimal" mediante un gráfico de barras, identificando que "Young Adults" presenta el mayor promedio de horas de streaming diario (101.87% del % total de columnas).
- Se exploró "Discover Weekly_Categories" versus "Hours Streamed Per Day_Decimal" con un gráfico de columnas, donde la categoría "High" mostró el mayor consumo (101.25% del % total de columnas).
- Se examinó "Top Genre" respecto a "Hours Streamed Per Day_Decimal" mediante un gráfico de barras, destacando "Rock" con el mayor tiempo de streaming (104.88% del % total de columnas).
- Se comparó "Subscription Type" con "Hours Streamed Per Day_Decimal" usando un gráfico de columnas, observando que los usuarios "Free" tienen un consumo ligeramente superior (100.11% del % total de columnas).
- Se evaluó la relación entre "Subscription Type" y "Discover Weekly Engagement %" mediante un gráfico de columnas, donde los usuarios "Free" mostraron mayor engagement (100.47% del % total de columnas).
- Se analizó "Country" versus "Hours Streamed Per Day_Decimal" con un gráfico de columnas, identificando a Alemania con el mayor consumo por país (104.10% del % total de columnas).
- Se creó una tabla dinámica cruzada entre "Country" y "Top Genre" calculando el % total de columnas, destacando con formato condicional amarillo el género con mayor porcentaje en cada país (fila).
- Se exploró "Country" y "Subscription Type" mediante un gráfico de columnas, revelando que Australia lidera en suscripciones "Free" (11% del % total de columnas), mientras que UK y Canadá destacan en "Premium" (11% del % total de columnas cada uno), los demás países oscilan entre 9-10% del % total de columnas.
- Se comparó "Age_Range" con "Number of Songs Liked", donde el grupo "Adults" mostró el mayor porcentaje (40% del % total de columnas).
- Se analizó "Top Genre" con "Repeat Song Rate %", identificando que EDM, Jazz y Reggae presentan las tasas más altas de repetición (11% del % total de columnas cada uno).
- Se examinó "Listening Time" versus "Top Genre" para entender las preferencias por momento del día: "Country" domina en "Afternoon" (38% del % total de columnas), EDM y Rock empatan en "Morning" (35% del % total de columnas cada uno), y "Reggae" lidera en "Night" (39% del % total de columnas) destacando con formato condicional amarillo el género con mayor porcentaje en cada país (fila).
- Se evaluó "Listening Time" con "Hours Streamed Per Day_Decimal", determinando que el periodo "Afternoon" concentra el mayor tiempo de streaming (100.61% del % total de columnas).

### **6. Análisis de conclusiones**

#### **Análisis nº 1: variables numéricas**

- **Tasa de Repetición de Canciones (Repeat_Song_Rate):**
la tasa de repetición muestra una media del 39% y mediana del 38%, con una alta desviación estándar del 23% que evidencia comportamientos muy diversos entre usuarios. Su curtosis negativa de -1 indica una distribución platicúrtica (más plana que la normal), confirmando que no existe un patrón dominante de repetición. El gráfico de columnas revela una distribución relativamente uniforme con ligera concentración en el rango 0.5-10.5%, mientras que el boxplot muestra simetría con algunos valores atípicos superiores. Esta alta dispersión sugiere la coexistencia de dos perfiles claramente diferenciados: usuarios "exploradores" que buscan constantemente música nueva y usuarios "tradicionales" que prefieren escuchar repetidamente sus canciones favoritas, lo cual requiere estrategias de personalización específicas para cada segmento.

- **Engagement Semanal (Weekly_Engagement):**
el engagement con las recomendaciones semanales presenta una media y mediana idénticas del 46%, con una desviación estándar del 26% que indica variabilidad considerable. La curtosis de -1 confirma una distribución platicúrtica, con el gráfico de columnas mostrando mayor concentración en los rangos medios (41-51%) y una caída notable en el engagement alto, donde solo el 10.40% de usuarios supera el 81% de engagement. El boxplot confirma simetría perfecta sin valores atípicos significativos. Esta distribución sugiere que la mayoría de usuarios interactúa moderadamente con las recomendaciones algorítmicas, indicando una oportunidad clara de optimización del sistema de recomendación para aumentar el engagement, especialmente considerando que esta función debería ser un diferenciador clave del servicio premium.

- **Horas de Streaming Diarias (Hours_Streamed):**
el consumo diario promedio de 5.2 horas (mediana 5.3) con desviación estándar de 2.9 horas muestra patrones de uso consistentes y saludables para la plataforma. La curtosis de -1.2 indica una distribución platicúrtica ligeramente más pronunciada, con el gráfico de columnas revelando que la mayoría de usuarios (21.24%) consume entre 5.2 y 7.2 horas diarias. El boxplot presenta simetría perfecta con el 50% central de usuarios entre 2.7 y 7.5 horas diarias, un rango intercuartílico relativamente estrecho que facilita la predicción de uso de recursos. Este consumo promedio considerable de más de 5 horas diarias indica un alto nivel de dependencia del servicio, lo cual es positivo para la retención pero también sugiere que los usuarios obtienen valor significativo incluso sin pagar premium.

- **Canciones Marcadas como Favoritas (Songs_Liked):**
Con una media y mediana perfectamente alineadas en 254 canciones y una desviación estándar alta de 146, esta variable muestra comportamientos de "colección" muy diversos. La curtosis de -1 indica distribución platicúrtica, pero el gráfico de columnas revela un patrón bimodal interesante: concentraciones en usuarios con pocas favoritas (1-100 canciones, 19.84%) y usuarios coleccionistas (401-500 canciones, 21.46%). El boxplot confirma distribución uniforme sin sesgos. Esta bimodalidad natural sugiere dos perfiles de usuario claramente diferenciados - "casuales" versus "coleccionistas" - que podrían aprovecharse para estrategias de marketing segmentadas y potencialmente diferentes límites de almacenamiento o funcionalidades según el plan de suscripción.
- **Edad de Usuarios (Age)**:
la edad promedio de 37 años (mediana idéntica) con desviación estándar de 14 años revela una base de usuarios significativamente más madura de lo esperado en servicios de streaming. La curtosis de -1 y la distribución casi uniforme entre grupos etarios (con ligera disminución solo en 53-62 años) confirma diversidad generacional sin concentraciones específicas. El boxplot muestra perfecta simetría con el rango intercuartílico entre 25-49 años. Esta madurez demográfica contradice completamente la percepción del streaming como servicio juvenil y representa una oportunidad estratégica importante: los usuarios de 30-50 años tienen típicamente mayor poder adquisitivo y estabilidad financiera, sugiriendo potencial no explotado para servicios premium de mayor valor si se diseñan adecuadamente para sus necesidades específicas.

#### **Análisis nº 2: variables categóricas**
- **Distribución de Horarios de Escucha (Listening_Time):**
los datos muestran que los usuarios prefieren escuchar música en la noche (34.90%), seguido por la tarde (32.68%) y la mañana (32.42%). Esta diferencia del 2.5% entre el horario más y menos popular es relativamente pequeña, lo que significa que la plataforma mantiene usuarios activos durante todo el día. El pico nocturno sugiere que la gente usa más el servicio para entretenimiento y relajación después del trabajo o estudios.
- **Artistas Más Reproducidos (Most Played Artist)/Descubrimiento Semanal por Artista (Discover_Weekly_Categories):**
no hay ningún artista dominante en la plataforma. Bad Bunny tiene el porcentaje más alto con solo 10.56%, seguido muy de cerca por Post Malone y Adele (ambos 10.38%). Esta distribución tan pareja (todos los artistas entre 9.54% y 10.56%) indica que los usuarios tienen gustos musicales muy variados y la plataforma no depende de un solo artista popular para mantener a sus usuarios.
- **Problema con el Modelo de Suscripciones (Subscription_Type):**
la plataforma tiene casi la misma cantidad de usuarios gratuitos (49.48%) que de pago (50.52%). Según el documento adjunto, esto representa un problema serio porque ambos tipos de usuarios escuchan prácticamente la misma cantidad de música. Esto significa que los usuarios no ven suficiente valor en pagar la suscripción premium, lo cual afecta directamente los ingresos de la empresa.

- **Tasa de Repetición por Género Musical (Repeat Song Rate):**
EDM, Jazz y Reggae tienen las tasas más altas de repetición (10.64% cada uno), mientras que Pop tiene la más baja (9.24%). Esto significa que las personas que escuchan EDM, Jazz y Reggae tienden a repetir más sus canciones favoritas, lo que indica mayor fidelidad a estos géneros. Esta información es valiosa para crear listas de reproducción y recomendaciones.

- **Géneros Musicales Preferidos (Music_Genre):**
la distribución de géneros es muy equilibrada: EDM y Jazz lideran con 10.64%, seguidos por Reggae (10.64%) y Rock (10.32%). El género menos popular es Pop con 9.24%. Esta distribución tan uniforme (diferencia máxima de 1.4%) muestra que la plataforma tiene una audiencia con gustos diversos, sin un género claramente dominante.

- **Competencia entre Plataformas (Streaming_Platform):**
Amazon Music lidera con 17.22%, seguido muy de cerca por Tidal (17.00%), YouTube (16.44%) y Spotify (16.54%). La diferencia entre la plataforma más y menos usada es de apenas 2.3%, lo que indica que los usuarios probablemente usan múltiples servicios de streaming simultáneamente. Esto representa un desafío para la retención de usuarios (mantener a los usuarios usando solo un servicio).
- **Distribución por País (Country):**
Australia tiene el porcentaje más alto de usuarios (10.52%), mientras que Germany tiene el más bajo (9.42%). Sin embargo, según el documento, Germany tiene el mayor consumo de horas a pesar de tener menos usuarios. La distribución es muy pareja entre todos los países (diferencia de solo 1.1%), lo que muestra una penetración global equilibrada sin mercados dominantes.
- **Grupos de Edad (Age_Range):**
Los adultos (Adults) representan el 40.40% de los usuarios, seguidos por adultos mayores (Seniors) con 35.40%. Los jóvenes adultos (Young Adults) solo son el 13.96% y los adolescentes (Youth) apenas 10.24%. Esto es sorprendente porque generalmente se asocia el streaming con usuarios jóvenes, pero aquí el 75% de usuarios tienen más de 35 años.


#### **Análisis nº 3: Bi-variables**

- **Crisis del Modelo de Monetización:**
los resultados revelan una falla crítica en la estrategia de monetización de la plataforma. Los usuarios Free consumen prácticamente las mismas horas que los usuarios Premium (100.11% vs 99.9%), evidenciando la ausencia de una propuesta de valor diferenciadora efectiva para la suscripción paga. Adicionalmente, los usuarios Free utilizan más las funcionalidades de Discover Weekly (100.47%) que los Premium, indicando que las características distintivas del servicio pago no están generando el engagement esperado ni justificando la inversión de los usuarios.
- **Segmentación Demográfica y Geográfica:**
el análisis demográfico identifica a los Young Adults como el segmento más valioso, con un consumo 101.87% superior al promedio general. Los Adults emergen como el segmento más activo socialmente, representando el 40% del total de canciones marcadas como favoritas, lo que sugiere mayor propensión al engagement con funcionalidades sociales. A nivel geográfico, Germany se posiciona como el mercado más engaged con 104.10% de consumo, mientras que la distribución Premium se concentra equilibradamente en Australia, UK y Canada (11% cada uno), revelando oportunidades de expansión en mercados con penetración del 9-10%.

- **Estrategia de Contenido y Géneros Musicales:**
Rock domina como el género de mayor engagement con 104.88% de consumo, estableciéndose como la categoría musical más valiosa para la retención de usuarios y la generación de horas de reproducción. En contraste, EDM, Jazz y Reggae comparten el liderazgo en fidelización con 11% de repeat rate cada uno, sugiriendo que estos géneros, aunque no generen el mayor volumen de horas, crean mayor lealtad de audiencia. Esta dualidad entre volumen y fidelización presenta oportunidades para estrategias de contenido diferenciadas según objetivos específicos.

- **Patrones Temporales y Programación de Contenido:**
los datos revelan patrones de consumo claramente diferenciados por horarios. El consumo se concentra en las tardes con 100.61% por encima del promedio, estableciendo esta franja como el momento óptimo para lanzamientos y campañas promocionales. Las preferencias musicales varían significativamente según el horario: Country domina las tardes (38%), EDM y Rock se equilibran en las mañanas (35% cada uno), y Reggae lidera las noches (39%). Esta segmentación temporal indica la necesidad de implementar programación específica por franjas horarias para maximizar el engagement.
- **Efectividad de Algoritmos de Recomendación:**
los usuarios con High engagement en Discover Weekly apenas superan el promedio de consumo general (101.25%), sugiriendo que los algoritmos de recomendación no están generando el impacto esperado en el comportamiento de escucha total. La correlación débil entre engagement con recomendaciones y tiempo de consumo indica que los sistemas de recomendación requieren optimización para convertir el descubrimiento de contenido en mayor tiempo de permanencia en la plataforma.

- **Distribución Global y Estrategia de Expansión:**
el análisis de distribución por países muestra que la base de usuarios está equilibradamente repartida entre las diferentes naciones, con cada país representando aproximadamente entre 9-11% del total de usuarios. Australia lidera ligeramente con usuarios Free (11%), mientras que UK y Canada destacan en usuarios Premium (11% cada uno), pero estas diferencias son mínimas y no indican concentración significativa. La distribución de preferencias musicales por país revela patrones culturales distintivos que pueden aprovecharse para desarrollar estrategias de contenido localizado, donde cada región muestra preferencias particulares por ciertos géneros musicales.

- **COMPORTAMIENTO DE FIDELIZACIÓN:**
la correlación entre descubrimiento de nuevo contenido y repetición de canciones muestra que ciertos géneros como EDM, Jazz y Reggae logran el equilibrio óptimo entre novedad y fidelización, mientras que otros géneros podrían beneficiarse de estrategias específicas para mejorar su capacidad de retención de audiencia.

### **7. Próximos Pasos**

1.  **Análisis Exploratorio de Datos (EDA)**: Realizar un análisis inicial de los datos, identificando patrones y posibles problemas (valores faltantes, outliers, etc.).

2.  **Diseño de Dashboards**: Crear dashboards interactivos que resalten las métricas más relevantes, con un enfoque en preferencias musicales y segmentación de usuarios.

3.  **Presentación de Resultados**: Entregar un informe final con los insights obtenidos y recomendaciones para mejorar la experiencia del usuario y optimizar las estrategias de contenido.
