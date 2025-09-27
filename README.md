# DCDDyAA - Unidad 9 - Grupo E - Entrega Trabajo Final

Se realiza la entrega final de la diplomatura en Ciencia de Datos. Grupo E.

# Análisis y Modelado de Reviews del E-Commerce Brasileño

Este repositorio contiene un **notebook Jupyter (`.ipynb`)** que realiza un análisis exploratorio (EDA), limpieza de datos, feature engineering y modelado de probabilidades de malas reseñas en pedidos de un e-commerce brasileño (dataset Olist).  

---

## 📂 Datasets utilizados

Se utiliza el dataset público de **e-commerce brasileño Olist**, disponible en [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce).  
Incluye CSV con información de pedidos, productos, clientes, vendedores, pagos, reseñas y geolocalización.  

---

## Descarga de los datasets

Por el tamaño de los archivos CSV, **no se incluyen directamente en este repositorio**.  
En su lugar, deben descargarse desde la fuente oficial:

👉 [Dataset Olist Brazilian E-Commerce en Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

### Pasos:

1. Descargar todos los archivos `.csv` del dataset desde Kaggle.  
2. En tu **Google Drive**, dentro de la carpeta principal del proyecto: TrabajoFinalGrupoE/
3. crear una subcarpeta llamada `Datos/`.  
4. Copiar dentro de `Datos/` todos los CSV descargados de Kaggle.  

---

## 🚀 Cómo ejecutar el notebook

1. **Subir el proyecto a Google Drive**  
   - Se debe subir el proyecto con el nombre de la carpeta principal en la unidad no agregar ni modificar el nombre de ninguna carpeta/subcarpeta de lo contrario el programa no funcionara.

2. **Abrir con Colab**  
   - Haz click derecho sobre el notebook `.ipynb` → `Abrir con` → `Google Colaboratory`.  
   - Colab cargará el notebook y montará tu Google Drive para leer y guardar archivos.  

3. **Estructura de carpetas esperada en Drive**  
- /MiDrive/TrabajoFinalGrupoE/ -> Dentro de esta van los siguientes contenidos.
- notebook.ipynb
- /Datos/ <- carpeta con los CSV de Kaggle
- /artefactos/ <- se crean automáticamente al ejecutar
- /eda/ <- estadísticas y tablas del EDA
- /figuras/ <- gráficos generados

---


4. **Ejecutar celdas del notebook**  
- Primero se montará Google Drive y se definirán las rutas base. Se requiere iniciar sesion en colab con la misma cuenta donde esta el proyecto y dar todos los permisos solicitados  
- Luego se cargarán los CSV desde `Datos/`.  
- A continuación se ejecutan las secciones de EDA, limpieza, modelado y evaluación.  
- Al final se exportan métricas, modelos y gráficos en la carpeta `artefactos/`.  

---

## 📊 Qué hace el notebook

- Limpieza de datos y normalización de columnas (fechas, ZIPs, precios, fletes).  
- Feature engineering (distancias geográficas, recencia/frecuencia por cliente, tasas históricas de malas reseñas).  
- Preparación de variables categóricas y numéricas listas para modelado.  
- División temporal de datos en **Train / Valid / Test**.  
- Modelado con **XGBoost** y **LightGBM**, incluyendo calibración isotónica.  
- Evaluación con métricas clásicas y prioritarias (ROC-AUC, PR-AUC, Recall@Top-N).  
- Interpretabilidad con **SHAP**, mostrando importancia global y local de features.  

---

## 💾 Resultados generados

- Probabilidades de test (`prob_test_xgb_lgbm.csv`)  
- Top-N priorizados (`top_5000_priorizados.csv`)  
- Tablas de EDA, gráficos y ranking de importancias  
- Modelos guardados con `joblib` para reutilización (`.joblib`)  

---

## ⚠️ Notas finales

- El notebook está diseñado para **ejecutarse en Google Colab con Drive**:
- Se debe cargar la carpeta TrabajoFinalGrupoE en el drive directamente. no ingresar adentro de ninguna carpeta.
- Debe existir una carpeta `Datos/` con los CSV de Kaggle.  
- Las carpetas `artefactos/`, `eda/` y `figuras/` se generan automáticamente.  
- Esto asegura que cualquier persona que tenga el notebook y los datos en Drive pueda reproducir los resultados sin modificar rutas.
- Respetar las mayusculas y minusculas de las carpetas
