# Práctica IA (RA4 · b+c) — Big Data, análisis, rentabilidad y valoración IA

## 1) Caso y objetivo de negocio

- **Empresa/sector (real o ficticia):** NeoTech (empresa ficticia de comercio electrónico)
- **Problema a resolver:** Alta tasa de abandono de carrito y bajo índice de recompra.
- **Objetivo de negocio (rentabilidad):** Aumentar ventas y mejorar la fidelización de clientes mediante recomendaciones personalizadas basadas en IA.

## 2) Big Data: recogida masiva de datos

Se considera Big Data por cumplir las **3V**:

- **Volumen:** Millones de eventos diarios de navegación.
- **Velocidad:** Datos generados en tiempo real.
- **Variedad:** Datos estructurados y no estructurados.

### Fuentes de datos

- **Fuente 1:** Historial de compras (base de datos transaccional).
- **Fuente 2:** Eventos de navegación web (clics, búsquedas, tiempo en página).
- **Fuente 3:** Interacciones en redes sociales y reseñas de productos.

### Volumen/velocidad (estimación)

- 2–5 millones de eventos diarios.
- Flujo en tiempo real (streaming).

### Formatos

- Texto (reseñas).
- Eventos (clics).
- Series temporales (historial de compras).
- Logs estructurados (base de datos SQL).

## 3) Tratamiento/análisis: pipeline de datos

### Ingesta (captura/eventos)
- Uso de APIs y herramientas de streaming (ej. Kafka).
- Captura automática de eventos web.

### Limpieza/normalización
- Eliminación de datos duplicados.
- Tratamiento de valores nulos.
- Estandarización de formatos de fecha y moneda.

### Almacenamiento (data lake/warehouse)
- Data Lake para datos en bruto.
- Data Warehouse para análisis estructurado.

### Preparación de variables (features)
- Frecuencia de compra.
- Ticket medio.
- Categorías más visitadas.
- Tiempo desde última compra.

### Análisis/BI (opcional)
- Paneles en Power BI o Tableau.
- Segmentación de clientes (RFM).

## 4) IA aplicada: modelo y decisión

- **Tipo de IA/técnica:** Sistema de recomendación (Machine Learning supervisado + filtrado colaborativo).
- **Entrada del modelo:** Historial de compras, comportamiento de navegación, perfil del usuario.
- **Salida del modelo:** Lista personalizada de productos recomendados.
- **Decisión que habilita:** Mostrar productos personalizados en la web y enviar emails automatizados con recomendaciones.

## 5) Rentabilidad: KPIs antes/después

### KPI 1: Tasa de conversión
- **Antes:** 2,1%
- **Después:** 3,4%
- **Mejora:** Incremento de ventas gracias a recomendaciones personalizadas.

### KPI 2: Ticket medio
- **Antes:** 42€
- **Después:** 55€
- **Mejora:** Ventas cruzadas (cross-selling) y productos complementarios.

### KPI 3: Tasa de recompra (30 días)
- **Antes:** 18%
- **Después:** 27%
- **Mejora:** Mayor fidelización y reducción del coste de adquisición de clientes.

## 6) Diagrama del pipeline (ASCII o Mermaid)
```mermaid
flowchart TD

A[Usuarios Web/App] --> B[Captura de Eventos<br/>(Tracking en tiempo real)]
B --> C[Data Lake<br/>(Datos en bruto)]
C --> D[Limpieza y Transformación<br/>(ETL/ELT)]
D --> E[Data Warehouse<br/>(Datos estructurados)]
E --> F[Modelo IA Recomendador<br/>(Machine Learning)]
F --> G[Recomendaciones Personalizadas]
G --> H[Aumento de Ventas y Fidelización]
```

## 7) Riesgos y mitigación
Riesgo 1:
- Cumplimiento de RGPD, anonimización y consentimiento explícito.

Riesgo 2:
- Auditorías periódicas del modelo y revisión de datos de entrenamiento

## 8) Valoración (criterio c): importancia presente y futura de la IA (10–15 líneas)
- Importancia actual (hoy):
- Actualmente, la IA es clave en el comercio electrónico para personalizar la experiencia del cliente.
  Permite analizar grandes volúmenes de datos en tiempo real y tomar decisiones automáticas que aumentan la eficiencia y
  la rentabilidad.Empresas digitales dependen cada vez más de sistemas predictivos para competir en mercados saturados.
  
- Importancia futura (3–5 años):
- La inteligencia artificial (IA) en los próximos 3 a 5 años (2026-2029) dejará de ser una herramienta experimental para convertirse en la columna vertebral operativa y estratégica de los negocios. Se espera que esta tecnología transforme la productividad, automatizando hasta el 30% de las horas laborales actuales para 2030, y cambie el enfoque de la adopción de IA de "copilotos" (asistentes) a "agentes" autónomos que ejecutan tareas completas.

- Condiciones/limitaciones (datos, costes, regulación, ética, seguridad, empleo):
- Calidad y cantidad de datos.
- Coste de infraestructura tecnológica.
- Regulación (protección de datos).
- Ética y sesgos algorítmicos.

Impacto en el empleo y necesidad de formación.
- Conclusión razonada:
- La IA no es solo una herramienta tecnológica, sino un factor estratégico de competitividad. Su correcta implementación permite mejorar la rentabilidad, reducir riesgos y crear ventajas sostenibles a largo plazo.

## 9) Fuentes oficiales (mín. 2)

- Big Data/analítica (enlace oficial):
  https://www.ibm.com/topics/big-data
- IA/técnica/modelo (enlace oficial):
  https://www.ibm.com/topics/machine-learning
