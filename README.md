# Práctica IA (RA4 · a) — Automatización y optimización

## 1) Proceso elegido
- Nombre del proceso: Detección de fraude
- Contexto (empresa/servicio web/IT):
  es un conjunto de estrategias, tecnologías y procedimientos diseñados para identificar, prevenir y
  responder a actividades sospechosas dentro de plataformas digitales
- Rol/es implicados:
  Equipo de Riesgo,
  Data & Machine Learning e
  Ingeniería

## 2) ANTES (sin IA)
- Pasos (5–7):
  1. Recolección de Datos
  2. Definición de Reglas Predefinidas (Rule-based)
  3. Evaluación de Riesgo Manual y Revisión de Alertas
  4. Toma de Decisiones
  5.Ajuste y Optimización Manual
- Tiempo aproximado por caso:
  15 a 30 minutos
- Problemas / cuellos de botella:
  Alta Carga de Trabajo para los Analistas, Mayor tiempo en la toma de decisiones

## 3) DESPUÉS (con IA)
- ¿Qué automatiza la IA?
  El analisis de patrones de comportamiento, Analisis de redes
- ¿Qué queda para humanos?
  Aunque la IA es muy eficaz en la detección de fraudes, los humanos siguen jugando un papel crucial en el proceso, especialmente en los siguientes aspectos:
  Validación y juicio final: Aunque los sistemas automáticos pueden marcar una transacción
  como sospechosa, los analistas humanos pueden ser necesarios para revisar casos complejos que la IA no pueda resolver con certeza.
  Por ejemplo, si hay un patrón atípico pero legítimo en el comportamiento de un cliente, un experto puede intervenir para hacer un juicio basado en el contexto.
- Datos necesarios (tipos de datos, sin datos personales):
  Transaccionales, de Comportamiento y de Red
- Modelo/técnica (NLP, clasificación, recomendación, visión, etc.):
  Dependiendo de la naturaleza del fraude que se desee detectar, diferentes modelos y técnicas de IA pueden ser aplicados:

- **Clasificación**:

  - **Modelos de clasificación supervisada** (como **SVM**, **Árboles de decisión**, **Random Forests**, **XGBoost** o **Redes neuronales**) para predecir si una transacción es fraudulenta o no, basándose en características conocidas de transacciones fraudulentas y legítimas.

  - **Regresión logística**: A veces utilizada para estimar la probabilidad de fraude en una transacción basada en las características observadas.

- **Redes neuronales**:

  - **Redes neuronales profundas (Deep Learning)** pueden aprender representaciones complejas de los datos, siendo útiles cuando los patrones de fraude son muy complejos o no lineales. Los **Autoencoders** o **Redes LSTM** son ejemplos para detectar anomalías.

- **Procesamiento de Lenguaje Natural (NLP)**:

  - **NLP** se utiliza para analizar textos como correos electrónicos, interacciones de chat o transcripciones de llamadas. Técnicas como **análisis de sentimiento**, **detección de intenciones** o **clasificación de texto** pueden identificar patrones de fraude en la forma en que los usuarios comunican sus solicitudes o quejas.

## 4) Optimización (mejora medible)
Define 3 métricas con valores antes/después:
- Tiempo:
  - **Antes**: El tiempo necesario para detectar un fraude y procesar una transacción sospechosa podría ser de entre 30 minutos a 1 hora, dependiendo de la complejidad del caso y la intervención manual.
  - **Después**: Con la IA implementada, la detección de fraude y el procesamiento de transacciones sospechosas se reduce a unos pocos segundos, permitiendo una intervención en tiempo real (generalmente menos de 1 minuto por transacción).
- Coste:
  - **Antes**: El coste de los recursos humanos dedicados a la revisión manual de transacciones sospechosas puede ser significativo, representando hasta un 30% del presupuesto total de operaciones en algunas empresas.
  - **Después**: La automatización reduce la necesidad de personal para la detección y gestión del fraude, lo que puede disminuir el coste operativo en un 20-40%, dependiendo de la escala de la implementación y los sistemas automatizados utilizados.
- Calidad:
- **Antes**: La tasa de falsos positivos (transacciones legítimas marcadas como fraudulentas) podría estar en un rango de 15-25%, lo que genera frustración en los usuarios y posibles pérdidas de ingresos por clientes insatisfechos.
- **Después**: La calidad de las predicciones mejora significativamente, reduciendo la tasa de falsos positivos a un rango de 5-10%, gracias a los modelos de IA que se ajustan a patrones de comportamiento complejos y evolucionan con el tiempo.

## 5) Diagrama del flujo (ASCII o Mermaid)
graph TD
    A[Inicio] --> B[Recopilación de datos de transacciones]
    B --> C{¿Datos completos?}
    C -->|Sí| D[Preprocesamiento de datos]
    C -->|No| E[Obteniendo datos faltantes]
    E --> D
    D --> F[Análisis y extracción de características]
    F --> G{¿Es sospechoso el comportamiento?}
    G -->|Sí| H[Marcado de transacción como fraudulenta]
    G -->|No| I[Transacción aprobada]
    H --> J[Generación de alerta y notificación al usuario]
    I --> K[Fin]
    J --> K

## 6) Riesgos y mitigación
- **Riesgo 1**: **Falsos positivos y negativos**
  - **Mitigación 1**: Implementar un sistema de retroalimentación continuo, donde las transacciones marcadas como sospechosas sean revisadas por analistas humanos para ajustar los modelos y reducir tanto los falsos positivos como negativos. Además, se pueden ajustar los umbrales de confianza del modelo para mejorar su precisión sin perder demasiada sensibilidad.

- **Riesgo 2**: **Dependencia excesiva de la IA y falta de supervisión humana**
  - **Mitigación 2**: Asegurar que siempre haya un proceso de supervisión humana en casos complejos o cuando el modelo indique una posible alerta de fraude. La IA debe ser vista como una herramienta complementaria y no como un reemplazo total de la intervención humana. También es importante realizar auditorías regulares del sistema para garantizar su rendimiento y alineación con los objetivos empresariales.

## 7) Fuente oficial
- - **Enlace**: [https://www.acm.org/publications/](https://www.acm.org/publications/)  
