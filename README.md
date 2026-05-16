# 📊 NovaRetail+ | Análisis de Comportamiento de Clientes

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg?style=flat-square&logo=python)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-1.0+-green.svg?style=flat-square&logo=pandas)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg?style=flat-square&logo=jupyter)](https://jupyter.org/)
[![Scipy](https://img.shields.io/badge/SciPy-Statistics-red.svg?style=flat-square&logo=scipy)](https://www.scipy.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen.svg?style=flat-square)](https://github.com/)

> 📈 Análisis correlacional exploratorio de factores que influyen en el ingreso anual generado por clientes en la plataforma de e-commerce **NovaRetail+**

---

## 📋 Tabla de Contenidos

- [Descripción del Proyecto](#-descripción-del-proyecto)
- [Pregunta de Investigación](#-pregunta-de-investigación)
- [Dataset](#-dataset)
- [Estructura del Proyecto](#-estructura-del-proyecto)
- [Requisitos](#-requisitos)
- [Instalación](#-instalación)
- [Uso](#-uso)
- [Metodología](#-metodología)
- [Resultados Clave](#-resultados-clave)
- [Limitaciones](#-limitaciones)
- [Contribuciones](#-contribuciones)
- [Licencia](#-licencia)

---

## 🎯 Descripción del Proyecto

NovaRetail+ es una plataforma de comercio electrónico líder en Latinoamérica con millones de usuarios activos. Este proyecto forma parte de la iniciativa del equipo de **Crecimiento y Retención** para identificar qué factores del comportamiento del cliente están más fuertemente asociados con el ingreso anual generado.

Es un análisis **correlacional exploratorio** que busca entender patrones sin establecer relaciones causales.

> ⚠️ **Importante**: Correlación ≠ Causalidad

---

## 🔍 Pregunta de Investigación

### Pregunta Principal
**¿Qué factores del comportamiento del cliente están más fuertemente asociados con el ingreso anual generado?**

### Objetivo Secundario
- Explorar relaciones entre variables numéricas, binarias y categóricas
- Identificar segmentos de clientes de alto y bajo valor
- Proporcionar insights para estrategias de retención y crecimiento

---

## 📊 Dataset

### Origen
Dataset interno de NovaRetail+ correspondiente a 2024

### Estadísticas Generales
- **Registros**: 15,000 clientes
- **Columnas**: 12 variables
- **Valores Nulos**: 0
- **Período**: 2024

### Variables Disponibles

| Variable | Tipo | Descripción |
|----------|------|-------------|
| `id_cliente` | Categórica | Identificador único del cliente |
| `edad` | Numérica | Edad del cliente (18-75 años) |
| `nivel_ingreso` | Numérica | Ingreso anual estimado ($8K-$74K) |
| `visitas_mes` | Numérica Discreta | Visitas mensuales a la plataforma |
| `compras_mes` | Numérica Discreta | Compras realizadas en el mes |
| `gasto_publicidad_dirigida` | Numérica | Gasto en anuncios personalizados |
| `satisfaccion` | Ordinal | Calificación 1-5 de satisfacción |
| `miembro_premium` | Binaria | Suscripción premium (0/1) |
| `abandono` | Binaria | Abandono de plataforma (0/1) |
| `tipo_dispositivo` | Categórica | Móvil, Escritorio, Tablet |
| `region` | Categórica | Geografía: Norte, Sur, Este, Oeste |
| `ingreso_anual` | Numérica | **Métrica principal de análisis** |

---

## 🗂️ Estructura del Proyecto

```
project-novaretail/
├── README.md                                    # Este archivo
├── S8_Student_Version-Project-NovaRetail.ipynb  # Notebook principal
├── data/
│   └── novaretail_comportamiento_clientes_2024.csv
├── results/
│   ├── correlation_analysis.csv
│   ├── heatmap_correlation.png
│   └── insights.txt
└── requirements.txt                             # Dependencias
```

---

## 📦 Requisitos

- Python 3.8+
- Jupyter Notebook / JupyterLab
- pandas >= 1.0
- numpy >= 1.19
- scipy >= 1.5
- matplotlib >= 3.3
- seaborn >= 0.11

---

## ⚙️ Instalación

### 1. Clonar el repositorio
```bash
git clone https://github.com/tu-usuario/project-novaretail.git
cd project-novaretail
```

### 2. Crear entorno virtual (Recomendado)
```bash
# Con venv
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate

# O con conda
conda create -n novaretail python=3.9
conda activate novaretail
```

### 3. Instalar dependencias
```bash
pip install -r requirements.txt
```

### 4. Lanzar Jupyter
```bash
jupyter notebook
```

---

## 🚀 Uso

### Ejecución del Análisis

1. **Abrir el Notebook**
   ```bash
   jupyter notebook S8_Student_Version-Project-NovaRetail.ipynb
   ```

2. **Secciones del Notebook**
   - **Sección 1**: Cargar y explorar el dataset
   - **Sección 2**: Preparar datos y documentar supuestos
   - **Sección 3**: Visualizar relaciones entre variables
   - **Sección 4**: Análisis correlacional según tipo de variable
   - **Sección 5**: Insights y recomendaciones

3. **Ejecutar Celdas**
   - Presiona `Shift + Enter` para ejecutar cada celda
   - O usa `Kernel → Restart & Run All` para ejecutar todo

---

## 🔬 Metodología

### Enfoques de Análisis Correlacional

Según el tipo de variables, utilizamos distintos coeficientes de correlación:

#### 1️⃣ **Correlación de Pearson**
- **Uso**: Variable numérica ↔ Variable numérica
- **Supuestos**: Relación lineal, distribución normal
- **Rango**: -1 a +1

```python
from scipy.stats import pearsonr

coef, p_value = pearsonr(df['var1'], df['var2'])
```

#### 2️⃣ **Correlación de Spearman**
- **Uso**: Variables ordinales o cuando no se cumple normalidad
- **Supuestos**: Relación monótona
- **Rango**: -1 a +1

```python
from scipy.stats import spearmanr

coef, p_value = spearmanr(df['var1'], df['var2'])
```

#### 3️⃣ **Correlación Punto-Biserial**
- **Uso**: Variable binaria ↔ Variable numérica
- **Supuestos**: Binaria y numérica normal
- **Rango**: -1 a +1

```python
from scipy.stats import pointbiserialr

coef, p_value = pointbiserialr(df['binaria'], df['numerica'])
```

#### 4️⃣ **V de Cramér**
- **Uso**: Variable categórica ↔ Variable categórica
- **Supuestos**: Independencia en tabla de contingencia
- **Rango**: 0 a 1

```python
from scipy.stats import chi2_contingency

chi2 = chi2_contingency(pd.crosstab(df['cat1'], df['cat2']))[0]
v = np.sqrt(chi2 / (n * (min_dim - 1)))
```

### Interpretación de Coeficientes

| Rango | Interpretación |
|-------|----------------|
| 0.0 - 0.2 | Correlación muy débil |
| 0.2 - 0.4 | Correlación débil |
| 0.4 - 0.6 | Correlación moderada |
| 0.6 - 0.8 | Correlación fuerte |
| 0.8 - 1.0 | Correlación muy fuerte |

---

## 📈 Resultados Clave

### Hallazgos Principales

#### 📊 Variables Numéricas
- **Correlación más fuerte**: Relación positiva entre compras/mes e ingreso anual
- **Segunda más fuerte**: Visitas/mes con ingreso anual
- **Gasto en publicidad**: Asociación moderada pero significativa

#### 💳 Variables Binarias
- **Membresía Premium**: Impacto positivo significativo en ingreso anual
- **Abandono**: Relación negativa fuerte con ingresos

#### 🌍 Variables Categóricas
- **Dispositivo Móvil**: Predominio (65.45%) pero ingresos variables
- **Región Geográfica**: Distribución equilibrada con variaciones de ingreso por zona

### Distribución del Target
- **Ingreso Anual**: Media $36.59, desviación estándar $34.48
- **Rango**: $0 - $244.69
- **25% inferior**: Ingresos cercanos a $0 (posibles clientes nuevos)

---

## ⚠️ Limitaciones

- ✅ **Análisis correlacional**: No establece causalidad
- ✅ **Datos transversales**: Captura un punto en el tiempo
- ✅ **Supuestos estadísticos**: Algunos pueden no cumplirse completamente
- ✅ **Valores atípicos**: Podrían influir en correlaciones
- ✅ **Multicolinealidad**: Variables independientes pueden estar correlacionadas

---

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Para participar:

1. **Fork** el repositorio
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commits con mensajes claros (`git commit -m 'Add AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un **Pull Request**

### Directrices
- Documenta cambios significativos en el análisis
- Mantén consistencia en nomenclatura y estilo de código
- Incluye explicaciones para nuevas visualizaciones

---

## 📧 Contacto

**Equipo de Crecimiento y Retención - NovaRetail+**
- 📍 Latinoamérica
- 📅 Cierre 2024

---

## 📄 Licencia

Este proyecto está bajo la licencia **MIT** - ver el archivo [LICENSE](LICENSE) para más detalles.

```
MIT License

Copyright (c) 2024 NovaRetail+ Analytics Team

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software...
```

---

## 🎓 Recursos Adicionales

- 📚 [Guía de Análisis Correlacional - Scipy Docs](https://docs.scipy.org/doc/scipy/reference/stats.html)
- 📘 [Pandas Documentation](https://pandas.pydata.org/docs/)
- 📊 [Seaborn Visualization Guide](https://seaborn.pydata.org/)
- 🔬 [Statistical Testing Guide](https://en.wikipedia.org/wiki/Statistical_hypothesis_testing)

---

## 📝 Historial de Cambios

### v1.0.0 (2026)
- ✅ Análisis correlacional completado
- ✅ Visualizaciones generadas
- ✅ Documentación finalizada

---

<div align="center">

**Hecho con ❤️ para NovaRetail+**

[⬆ Volver al inicio](#-novaretail--análisis-de-comportamiento-de-clientes)

</div>
