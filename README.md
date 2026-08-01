# RiskScore OECE

Proyecto de ciencia de datos para construir un modelo predictivo binario orientado a estimar el riesgo de sanción futura de proveedores vinculados a contratación pública peruana.

## Dashboard desplegado

El dashboard de resultados del modelo está disponible en Vercel:

**https://risk-score-oece-dashboard.vercel.app**

El dashboard permite visualizar el ranking de proveedores/postores evaluados, la probabilidad estimada de sanción en 24 meses, el nivel de riesgo, la comparación de modelos y la importancia de variables.

## Objetivo

Desarrollar un modelo de clasificación binaria que estime si un proveedor registra una sanción posterior dentro de un horizonte de 24 meses.

## Variable objetivo

`target_sancionado_24m`

- `1`: proveedor con sanción posterior dentro de 24 meses.
- `0`: proveedor sin sanción posterior dentro de 24 meses.

## Estructura

```text
notebooks/       Cuadernos Jupyter de las fases del proyecto
data/processed/  Bases limpias, featured y resultados procesados
models/          Modelo final y artefactos de entrenamiento
reports/         Informes y capturas del proyecto
```

## Fases del proyecto

1. Identificación del CSV y variable objetivo.
2. Carga correcta de datos.
3. Limpieza básica.
4. Creación de features.
5. Entrenamiento del modelo.
6. Evaluación del modelo.
7. Guardado del pipeline en `.joblib` y `.pkl`.

## Modelo final

Regresión Logística y Random Forest balanceado, entrenado con variables temporales, severidad de sanción, tipo de proveedor y motivo de infracción.

## Herramientas

- Python
- Pandas
- NumPy
- Scikit-learn
- Joblib
- Jupyter Notebook
- Anaconda
- Vercel

## Nota sobre datos

El proyecto utiliza información pública descargada de fuentes abiertas vinculadas a contratación pública y sanciones administrativas. Los archivos de datos brutos de mayor tamaño no se incluyen en esta versión ligera del repositorio.
