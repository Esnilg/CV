---
title: Carga de Datos con pandas.read_
summary: Guía Técnica, Carga de Datos con pandas.read_
date: 2025-11-29
type: docs
math: false
tags:
  - Python
image:
  caption: 'Embed rich media such as videos and LaTeX math'
---

Las funciones read_ de pandas están diseñadas para cargar datos desde múltiples fuentes —como archivos CSV, Excel, JSON, SQL y más— directamente en un DataFrame. Constituyen la puerta de entrada para cualquier proceso de análisis, limpieza o modelado.


## Cómo se utilizan los parámetros de las funciones read_

Aunque cada función read_ tiene parámetros específicos, muchas comparten una estructura común. A continuación, se muestran los más usados y cómo afectan la lectura de datos.

### Parámetros comunes

1. filepath_or_buffer

Ruta del archivo o URL.

```python
df = pd.read_csv("datos.csv")
```

2. sep (solo para CSV/TSV)

Define el separador entre columnas.

```python
df = pd.read_csv("datos.tsv", sep="\t")
```

3. header

Especifica la fila que contiene los nombres de columna.

```python
df = pd.read_csv("datos.csv", header=0)
```

Si un archivo no tiene encabezados:

```python
df = pd.read_csv("datos.csv", header=None)
```

4. names

Asigna nombres de columna manualmente.

```python
df = pd.read_csv("datos.csv", header=None, names=["col1", "col2", "col3"])
```

5. dtype

Define manualmente los tipos de datos.

```python
df = pd.read_csv("datos.csv", dtype={"id": int, "precio": float})
```

6. parse_dates

Convierte automáticamente columnas a formato fecha.

```python
df = pd.read_csv("ventas.csv", parse_dates=["fecha"])
```

7. na_values

Define valores que deben considerarse como NaN.

```python
df = pd.read_csv("datos.csv", na_values=["NA", "?", "-"])
```

7. usecols

Carga solo columnas específicas.

```python
df = pd.read_csv("datos.csv", usecols=["id", "monto"])
```

### Ejemplos por tipo de archivo

1. CSV

```python
df = pd.read_csv("archivo.csv", sep=",", encoding="utf-8")
```

2. Excel

```python
df = pd.read_excel("archivo.xlsx", sheet_name="Hoja1")
```

3. JSON

```python
df = pd.read_json("datos.json", orient="records")
```

4. SQL

```python
df = pd.read_sql("SELECT * FROM clientes", conexion_sql)
```