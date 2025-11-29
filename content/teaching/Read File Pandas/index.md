---
title: Carga de Datos con pandas.read_
summary: Guía Técnica: Carga de Datos con pandas.read_
date: 2023-10-24
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

filepath_or_buffer

Ruta del archivo o URL.

```python
df = pd.read_csv("datos.csv")
```

