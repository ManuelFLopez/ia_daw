# Práctica IA (RA4 · f)

## 1) Caso de uso
- **Tipo de aplicación:** Aplicación web de recomendación personalizada  
- **Problema:** Los usuarios tardan mucho en encontrar contenido relevante dentro de una plataforma con gran cantidad de elementos (productos, vídeos o cursos)  
- **Usuario:** Personas registradas en la plataforma (clientes, estudiantes o consumidores de contenido)

## 2) Datos
- **Datos:** Historial de navegación, clics, búsquedas, valoraciones, tiempo de visualización y datos básicos del perfil  
- **Tipo minería:** Minería de datos predictiva (recomendación y clasificación)

## 3) Pipeline
- **Recogida:** Captura automática de interacciones del usuario mediante logs y base de datos  
- **Limpieza:** Eliminación de datos duplicados, incompletos o irrelevantes  
- **Transformación:** Conversión a variables numéricas, normalización y generación de características (features)  
- **Entrenamiento:** Modelo de aprendizaje automático entrenado con datos históricos (por ejemplo, filtrado colaborativo)  
- **Predicción:** Generación de recomendaciones personalizadas en tiempo real  
- **Uso:** Mostrar al usuario contenido sugerido en la interfaz web

## 4) Integración
- **Backend:** API REST que ejecuta el modelo de IA (Node.js o Python)  
- **Frontend:** Aplicación web (HTML, CSS, JavaScript o framework como React/Vue)  
- **Flujo:**  
  1. El usuario inicia sesión  
  2. El frontend solicita recomendaciones al backend  
  3. El backend consulta el modelo de IA  
  4. Se devuelven resultados personalizados  
  5. El frontend los muestra al usuario  

## 5) Valor
- **Mejora:** Aumenta la relevancia del contenido y la satisfacción del usuario  
- **Sin IA:** Las recomendaciones serían genéricas o manuales  
- **Rentabilidad:** Mayor retención de usuarios e incremento del uso de la plataforma  

## 6) Diagrama

```mermaid
flowchart LR
    U[Usuario] --> F[Frontend Web]
    F --> B[Backend / API]
    B --> M[Modelo de IA]
    M --> D[Base de datos]
    D --> M
    M --> B
    B --> F
    F --> U
