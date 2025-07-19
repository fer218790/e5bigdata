Título: 
Implementación de Big Data en la Bolsa de Valores (NVDA @ S&P500)

Descripción: 
Predecir el precio futuro de cierre de la acción NVDA usando técnicas de Deep Learning con LSTM en TensorFlow.

Instalación: 
| Componente                   | Herramienta / Tecnología   | Función clave                                                     |
| ---------------------------- | -------------------------- | ----------------------------------------------------------------- |
| **Ingesta de datos**         | `yfinance` + Pandas        | Extracción de precios históricos desde Yahoo Finance              |
| **Procesamiento y limpieza** | `pandas`                   | Selección de columnas, manejo de nulos, conversión temporal       |
| **Ventaneo (ventana móvil)** | `pandas` + NumPy           | Transformar series en supervisadas con `lookback` (e.g., 20 días) |
| **Escalamiento**             | `MinMaxScaler` (`sklearn`) | Normalización de precios entre 0 y 1                              |
| **Serialización**            | `joblib` + `numpy.save`    | Guardado de datasets (`X_train`, `y_train`, etc.) y scaler        |
| **Visualización**            | `matplotlib`               | Inspección visual del comportamiento del activo                   |
| **Modelado (opcional)**      | `TensorFlow` (Keras)       | Construcción y entrenamiento de modelo LSTM                       |

Uso: 
Predecir el precio futuro (por ejemplo, del día siguiente) de una acción financiera —en este caso, NVDA (NVIDIA)— con base en su comportamiento histórico de precios.
