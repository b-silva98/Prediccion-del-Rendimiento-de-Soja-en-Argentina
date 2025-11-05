# 🌾 Predicción del Rendimiento de Soja en Argentina (1941–2023)

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-yellow)

---

## 📋 Descripción del proyecto

Este proyecto analiza datos históricos del cultivo de **soja en Argentina** (años 1941–2023) con el objetivo de **predecir el rendimiento (kg/ha)** mediante modelos de **Machine Learning**.  
Se trabaja con un dataset oficial del Ministerio de Agricultura y se aplican técnicas de limpieza, análisis exploratorio y modelado predictivo con **Random Forest Regressor**.

---

## 🎯 Objetivo

> Desarrollar un modelo predictivo capaz de estimar el rendimiento de soja a partir de variables como superficie sembrada, superficie cosechada, provincia y año, con el fin de identificar patrones productivos y apoyar la toma de decisiones en el sector agronómico.

---

## 🧩 Tecnologías y herramientas utilizadas

- 🐍 **Python 3.10+**
- 📦 **Librerías principales:**
  - `pandas`, `numpy` → Análisis y manipulación de datos
  - `matplotlib`, `seaborn` → Visualización y gráficos
  - `scikit-learn` → Modelos de Machine Learning
  - `jupyter` → Entorno de desarrollo

---

## 🔍 Proceso del proyecto

1. **Carga e inspección de datos:** Exploración de estructura y tipos.  
2. **Limpieza de datos:** Manejo de valores nulos y detección de outliers.  
3. **Análisis exploratorio:** Distribuciones, correlaciones y tendencias históricas.  
4. **Entrenamiento del modelo:** Uso de **Random Forest Regressor**.  
5. **Evaluación del modelo:** Medición de métricas de desempeño y análisis de errores.  
6. **Interpretación:** Importancia de variables y patrones productivos.  

---

## 📊 Estructura del proyecto


```
📁 soja-rendimiento-ml/
│
├── 📄 soja-serie-1941-2023.csv        # Dataset original
├── 📔 analisis_rendimiento_soja.ipynb     # Notebook principal
├── 📊 resultados_prediccion_rendimiento_soja.csv # Resultados detallados
├── 📈 importancia_variables_rendimiento_soja.csv # Relevancia de variables
└── 📘 README.md                           # Documentación del proyecto
```


---

## 📈 Resultados del modelo

### 🔹 Modelo: Random Forest Regressor
**Parámetros principales:**  
`n_estimators=100`, `max_depth=10`, `min_samples_split=5`, `min_samples_leaf=2`, `random_state=42`

### 🔹 Métricas de evaluación
| Métrica | Valor |
|----------|--------|
| MAE (Error Absoluto Medio) | **178.45 kg/ha** |
| RMSE (Raíz del Error Cuadrático Medio) | **263.05 kg/ha** |
| R² (Coeficiente de Determinación) | **0.88** |

> El modelo explica aproximadamente el **88% de la variabilidad** del rendimiento real, con errores promedio menores a **200 kg/ha**, lo que se considera un desempeño sólido para datos agrícolas históricos.

---

## 🌿 Importancia de las variables

| Variable | Importancia Normalizada |
|-----------|--------------------------|
| Producción (tm) | 0.45 |
| Superficie cosechada (ha) | 0.33 |
| Superficie sembrada (ha) | 0.12 |
| Año | 0.06 |
| Provincia | 0.04 |

> Las variables más influyentes son **producción** y **superficie cosechada**, lo que coincide con la lógica agronómica del rendimiento (rendimiento = producción / superficie cosechada).

---

## 📉 Análisis de residuos

| Indicador | Resultado |
|------------|------------|
| Media de errores | **-3.01 kg/ha** |
| Desviación estándar de errores | **263.05 kg/ha** |
| % de predicciones con error < 100 kg/ha | **44.2%** |
| % de predicciones con error < 200 kg/ha | **68.7%** |

> Los residuos se distribuyen de forma equilibrada (media cercana a 0), lo que indica que el modelo **no presenta sesgo sistemático**.  
> Más del **68% de las predicciones** tienen un error menor a **200 kg/ha**, mostrando una buena capacidad de generalización.

---

## 💡 Conclusiones

- El modelo logra una **alta precisión (R²=0.88)** y demuestra ser útil para **predecir rendimientos históricos** con bajo margen de error.  
- Se observó que las provincias con mayores rendimientos promedio son **Buenos Aires, Córdoba y Santa Fe**, donde el manejo y la infraestructura agrícola son más desarrollados.  
- Las variables productivas tienen un **impacto directo** en el rendimiento, confirmando la coherencia entre la predicción y la realidad agronómica.  
- Este modelo puede servir como **base para sistemas de monitoreo productivo** y proyecciones futuras de rendimiento bajo distintos escenarios.

---

## 🚀 Cómo ejecutar el proyecto

```bash
# Clonar el repositorio
git clone https://github.com/b-silva98/Prediccion-del-Rendimiento-de-Soja-en-Argentina.git

# Navegar al directorio
cd soja-rendimiento-ml

# Instalar dependencias
pip install -r requirements.txt

# Ejecutar el análisis
jupyter notebook analisis_rendimiento_soja.ipynb 

```
---

## 📬 Autor

👨‍💻 **Brian Emanuel Silva**  
Estudiante de **Analista Programador Universitario**  
📍 Argentina  
📧 [briiansiilva08@gmail.com](mailto:briiansiilva08@gmail.com)  
📱 +54 9 3886 47-9127  

---

## 🏷️ Licencia
Este proyecto se distribuye bajo la licencia **MIT**, por lo que puede ser utilizado y modificado libremente citando al autor original.
