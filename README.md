# Proyecto: Preprocesamiento y Clasificación de Datos de Clientes Bancarios

Este proyecto es una aplicación práctica de preprocesamiento y análisis de datos de una base de clientes de un banco. Su objetivo principal es identificar posibles riesgos de bancarrota utilizando modelos de aprendizaje automático basados en datos históricos.

## Descripción del Proyecto

El proyecto está dividido en varias etapas, cada una implementada en un archivo separado. Estas etapas incluyen:

1. **Preprocesamiento de datos (Archivo 01):** Limpieza y transformación de la base de datos original.
2. **Análisis de agrupamiento (Archivo 02):** Uso de K-means para segmentar clientes en clusters.
3. **Modelado predictivo (Archivo 03):** Entrenamiento y evaluación de múltiples modelos de clasificación.
4. **Predicción con nuevos datos (Archivo 04):** Aplicación del modelo entrenado para clasificar nuevos registros.

## Variables en la Base de Datos

- **ID:** Número único del cliente (eliminado durante el preprocesamiento).
- **AgnosDirec:** Años viviendo en la misma dirección.
- **AgnosEmpleo:** Años en el mismo empleo.
- **DeudaExt:** Deuda externa al banco.
- **DeudaInt:** Deuda interna en el banco.
- **Edad:** Edad del cliente.
- **Ingreso/Ingreso2:** Ingreso reportado por dos fuentes diferentes.
- **Nacionalidad:** Nacionalidad del cliente.
- **NivelEdu:** Nivel de educación.
- **VarObj:** Variable objetivo; indica si el cliente caería en bancarrota al recibir un crédito ('S' para sí, 'N' para no).

## Dependencias

El proyecto requiere las siguientes librerías:

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `scipy`
- `plotly`
- `imbalanced-learn`
- `joblib`
- `statsmodels`

## Estructura del Proyecto

### Archivo 01: Preprocesamiento de la base de datos

- Manejo de valores nulos y transformación de variables.
- Análisis exploratorio de datos con gráficos.
- Generación de variables log-transformadas y eliminación de colinealidad.

### Archivo 02: Análisis de clustering

- Implementación de K-means para segmentar clientes.
- Visualización de clusters con coordenadas paralelas.

### Archivo 03: Modelado predictivo

Entrenamiento de modelos de clasificación como:

- Regresión logística.
- Árboles de decisión.
- K-vecinos más cercanos.
- Random Forest.
- Redes neuronales.
- Máquinas de soporte vectorial (SVM).

Evaluación de modelos con curvas ROC y métricas como AUC.

### Archivo 04: Predicción

- Aplicación del modelo entrenado para predecir riesgos en un conjunto de datos nuevos.
- Guardado de predicciones en un archivo CSV.

## Resultados

El proyecto genera:

- Modelos entrenados guardados en formato `.joblib`.
- Análisis de clusters con insights de segmentación.
- Evaluación comparativa de modelos predictivos.
- Predicciones para nuevos clientes exportadas como archivo CSV.

## Ejecución

1. Preprocesar los datos con **Archivo 01**.
2. Realizar clustering con **Archivo 02**.
3. Entrenar y evaluar modelos con **Archivo 03**.
4. Realizar predicciones con datos nuevos usando **Archivo 04**.

## Notas Adicionales

- Todos los gráficos y métricas se encuentran generados en las etapas correspondientes.
- Las configuraciones de hiperparámetros se seleccionaron utilizando `GridSearchCV`.
- El modelo final y las predicciones se almacenan en la carpeta especificada en el código.

## Contribuciones

Se aceptan mejoras al código y sugerencias para ampliar el análisis.
