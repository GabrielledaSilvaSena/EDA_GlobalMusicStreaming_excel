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

### Análisis 3. Evaluación del Ecosistema de Streaming Musical.

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
