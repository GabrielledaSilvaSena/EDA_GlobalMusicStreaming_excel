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
├── Global_Music_Streaming_Listener_Preferences.csv #Datos originales
└── Excels
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

### **5. Recap sesiones**
### Sesión 1
- Creacion del repositorio
- Generacion de archivo README
- Creacion de informe mediante Claude.AI para simular Informe_Global_Music_Streaming
- Creacion sistema carpetas del repo
- Se añadio el conjunto de datos original Global_Music_Streaming_Listener_Preferences.csv

### **6. Próximos Pasos**

1.  **Análisis Exploratorio de Datos (EDA)**: Realizar un análisis inicial de los datos, identificando patrones y posibles problemas (valores faltantes, outliers, etc.).

2.  **Diseño de Dashboards**: Crear dashboards interactivos que resalten las métricas más relevantes, con un enfoque en preferencias musicales y segmentación de usuarios.

3.  **Presentación de Resultados**: Entregar un informe final con los insights obtenidos y recomendaciones para mejorar la experiencia del usuario y optimizar las estrategias de contenido.