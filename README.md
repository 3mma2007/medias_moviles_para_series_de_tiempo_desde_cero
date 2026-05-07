# 📈 Promedios Móviles — Series de Tiempo

Implementación paso a paso de un modelo de **promedios móviles** para series de tiempo, construido desde cero en Python sin librerías de forecasting externas.

## ¿Qué hace?

- Genera una serie de tiempo ficticia con datos aleatorios (semilla fija para reproducibilidad)
- Implementa manualmente la función de promedios móviles con parámetros `n` (día a predecir) y `k` (ventana de días anteriores)
- Calcula el error del modelo usando **RMSE** (Root Mean Squared Error)
- Visualiza la serie original vs. las predicciones con `matplotlib`

## Estructura del notebook

| Sección | Descripción |
|---|---|
| Generación de datos | Serie aleatoria de 100 valores enteros |
| Función `moving_avg` | Lógica del promedio móvil paso a paso |
| Cálculo de error | RMSE comparando predicciones vs. valores reales |
| Visualización | Gráficas de la serie y el modelo |

## Requisitos

```bash
pip install matplotlib
```

> Solo se usa `random` y `matplotlib` — ambos de la biblioteca estándar / común de Python.

## Uso

Abre el notebook en Jupyter o Google Colab y ejecuta las celdas en orden. Puedes ajustar el parámetro `k` para experimentar con distintos tamaños de ventana y observar su impacto en el RMSE.

## Concepto clave

El promedio móvil de orden `k` para el día `n` se calcula como:

$$\hat{y}_n = \frac{1}{k} \sum_{i=1}^{k} y_{n-i}$$
