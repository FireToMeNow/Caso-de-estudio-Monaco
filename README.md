# Caso de estudio Manaco

Notebook de análisis de comercio exterior de calzado reportado por España (2020–2024). No contiene datos de Manaco ni de Bolivia.

## Entorno local

Requiere Python 3.10 o posterior. Desde la carpeta del repositorio:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
jupyter lab Caso_Manaco_Estacion2.ipynb
```

En VS Code, selecciona el kernel `Python (Manaco)` después de activar el entorno o registra uno explícitamente:

```bash
python -m ipykernel install --user --name manaco --display-name "Python (Manaco)"
```

## Dataset requerido

El notebook espera el Excel `Bae_de_Datos_MANACO_-_INTERMEDIO_1.xlsx` en esta carpeta. Si el nombre es distinto, detecta automáticamente el único archivo `.xlsx` disponible. El dataset debe incluir `País_reportante`, `Flujo_comercial`, `Año`, `Código_SA6`, `Categoría_calzado`, `Socio_comercial`, `Valor_miles_USD`, `Cantidad_pares`, `Valor_USD` y `Valor_USD_por_par`. En este workspace está disponible `Bae de Datos MANACO - INTERMEDIO (1).xlsx`, con 240 filas y las 10 columnas esperadas. En Google Colab, la primera celda permite subir el archivo si no está en la carpeta.

El notebook genera `Manaco_tabla_depurada.xlsx` en esta carpeta. Los archivos de datos y resultados se excluyen de Git para evitar publicar datos del caso por accidente.