# Análisis de Ingresos en Planes Telefónicos para Megaline

Proyecto de análisis de datos en los ingresos de la empresa de telecomunicaciones **Megaline**. El objetivo es **analizar el comportamiento de consumo** como llamadas, mensajes e internet de los usuarios y estimar los **ingresos** por cliente con el fin de comparar la rentabilidad de los planes más usados **Surf** y **Ultimate**, incluyendo validación mediante **pruebas de hipótesis**.

<p align="center">
    <img src="figures/megaline_store.png" width="500">
    <br>
    <em>Sucursal de Megaline.</em>
</p>

## Contexto y objetivo del análisis

Megaline ofrece dos planes de prepago con estructuras de cobro diferentes. La empresa necesita conocer:
- ¿Qué plan genera más ingresos?
- ¿Cómo se distribuye el consumo entre usuarios?
- ¿Existen diferencias estadísticamente significativas en los ingresos entre planes y regiones?

## Datasets

El proyecto utiliza archivos CSV con información típica del dominio telecom:

- **users**: datos del cliente como id, ciudad o estado, plan, fecha de alta y baja.
- **plans**: características y costos de cada plan como cuota mensual, límites incluidos, tarifas por excedente.
- **calls**: registros de llamadas como usuario, fecha y duración.
- **messages**: registros de mensajes como usuarios y fechas.
- **internet**: consumo de datos por usuario, fecha y MB usados.

## Metodología aplicada

1. Preparación y limpieza.
2. Ingeniería de variables.
3. Cálculo de ingresos:
   - Cálculo de excedentes:
   - Ingreso mensual:
4. Análisis exploratorio:
   - Distribuciones de consumo por plan.
   - Comparación de ingresos por plan.
   - Identificación de patrones de consumo que explican excedentes.
5. Pruebas de hipótesis:
   - Comparación de ingresos promedio entre planes.
   - Comparación de ingresos por región.

## Resultados clave y recomendaciones de negocio

1. El plan **Surf muestra consumos significativamente mayores** a Ultimate, lo que indica mayor uso del consumidor.
2. Surf presenta mayor variabilidad en el consumo de sus servicios respecto a Ultimate.
3. Ambos planes experimentan un crecimiento mensual, especialmente **Surf registra incrementos más pronunciados**, por lo que Ultimate resulta un plan atractivo para otro tipo de consumidor que no está en decremento.
4. Los **ingresos mensuales** del plan Surf superan a los de Ultimate con una variabilidad notable.
5. Las pruebas de hipótesis confirman **diferencias significativas en los ingresos promedio** entre ambos planes, mostrando que es más atractivo y generador de mayores ingresos los del plan Surf. Se recomienda explorar estrategias que potencialicen los intresos mediante este producto.

## Cómo ejecutar el proyecto

1. Crear un entorno virtual:
   ```bash
   python -m venv .venv
   ```

2. Activar el entorno:
   - Windows:
     ```bash
     .\.venv\Scripts\activate
     ```
   - macOS / Linux:
     ```bash
     source .venv/bin/activate
     ```

3. Instalar dependencias:
   ```bash
   pip install -r requirements.txt
   ```

4. Ejecutar el notebook:
   - Abrir el archivo dentro de la carpeta `notebooks`
   - Seleccionar el kernel del entorno virtual
   - Ejecutar todas las celdas en orden

## Tecnologías usadas

- Python.
- Pandas.
- NumPy.
- Matplotlib y Seaborn.
- SciPy y Statsmodels.
- Jupyter Notebook.
