# Changelog

Todos los cambios notables en este proyecto se documentan en este archivo.

El formato se basa en [Keep a Changelog](https://keepachangelog.com/es-ES/1.0.0/),
y este proyecto adhiere a [Semantic Versioning](https://semver.org/lang/es/).

## [Unreleased]

### Planned
- [ ] Dashboard interactivo con Plotly
- [ ] Análisis de segmentación de clientes
- [ ] Modelos predictivos de churn
- [ ] Análisis temporal de comportamiento
- [ ] API REST para resultados

---

## [1.0.0] - 2024-01-15

### Added
- ✨ Análisis correlacional exploratorio completo
- ✨ Secciones principales del notebook:
  - Carga y exploración del dataset
  - Preparación de datos y documentación de supuestos
  - Visualización de relaciones entre variables
  - Análisis correlacional según tipo de variable
  - Insights y recomendaciones
- ✨ Funciones de análisis reutilizables:
  - `correlacion_pearson()`: Correlación para variables numéricas
  - `correlacion_spearman()`: Correlación no paramétrica
  - `correlacion_punto_biserial()`: Para variable binaria-numérica
  - `cramers_v()`: Para variables categóricas
- ✨ Visualizaciones:
  - Heatmap de correlación
  - Distribuciones univariadas
  - Scatter plots de relaciones clave
- 📚 Documentación completa:
  - README con estructura profesional
  - CONTRIBUTING.md para colaboradores
  - LICENSE MIT
  - requirements.txt para dependencias
  - .gitignore para Git
  - CHANGELOG.md (este archivo)

### Changed
- Reorganización de secciones para mayor claridad
- Mejora en la explicación de supuestos estadísticos

### Fixed
- Corrección en etiquetado de variables categóricas
- Validación de tipos de datos

### Documentation
- Guía completa de instalación
- Explicación de metodología estadística
- Interpretación de coeficientes de correlación
- Limitaciones y supuestos documentados

---

## [0.9.0] - 2024-01-10

### Added
- 📊 Análisis explorador inicial del dataset
- 📈 Primeras visualizaciones
- 📋 Definición de variables y estructura

### Changed
- Ajustes en visualización de datos

---

## Versionado

Este proyecto sigue [Semantic Versioning](https://semver.org/lang/es/):

- **MAJOR**: Cambios incompatibles con versiones anteriores
- **MINOR**: Nuevas funcionalidades compatibles hacia atrás
- **PATCH**: Correcciones de bugs compatibles hacia atrás

Formato: `MAJOR.MINOR.PATCH`

Ejemplo: `1.2.3`
- 1 = Cambios mayores
- 2 = Nuevas features
- 3 = Bug fixes

---

## Notación de Cambios

- ✨ **Added**: Nuevas funcionalidades
- 🔄 **Changed**: Cambios en funcionalidades existentes
- 🔨 **Fixed**: Correcciones de bugs
- ❌ **Removed**: Funcionalidades removidas
- 📚 **Documentation**: Cambios en documentación
- ⚡ **Performance**: Mejoras de rendimiento
- 🔐 **Security**: Arreglos de seguridad

---

## Cómo Reportar Cambios

Cuando contribuyas, incluye tus cambios en la sección `[Unreleased]` usando la notación correspondiente.

Ejemplo:
```markdown
## [Unreleased]

### Added
- Nueva función de análisis de clústeres

### Fixed
- Error en cálculo de correlación con valores nulos

### Changed
- Mejora en visualización de heatmap
```
---

**Última actualización**: 2024-01-15
