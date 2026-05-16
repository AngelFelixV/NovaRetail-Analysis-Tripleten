# Contribuir a NovaRetail+ Analytics

¡Gracias por tu interés en contribuir a este proyecto! Valoramos todas las contribuciones, ya sean reportes de bugs, sugerencias de mejora, o código nuevo.

## 📋 Código de Conducta

Este proyecto adhiere a un Código de Conducta que esperamos que todos los colaboradores respeten. Por favor, lee [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) antes de participar.

## 🚀 Cómo Contribuir

### 1. Reportar Bugs

Si encuentras un bug, crea un issue con:

- **Título descriptivo**: Sé específico sobre el problema
- **Descripción detallada**: Qué esperabas vs. qué pasó
- **Pasos para reproducir**: Lista paso a paso cómo reproducir el bug
- **Entorno**: Python version, SO, librerías utilizadas
- **Screenshots/Código**: Si es relevante, incluye ejemplos

**Template:**
```markdown
## Descripción del Bug
[Descripción clara]

## Pasos para Reproducir
1. ...
2. ...

## Comportamiento Esperado
[Qué debería suceder]

## Comportamiento Actual
[Qué sucede realmente]

## Entorno
- Python: 3.9
- pandas: 1.3.0
- scipy: 1.7.0
```

### 2. Sugerir Mejoras

Las sugerencias de mejora son bienvenidas. Crea un issue con:

- **Título claro**: Resumen de la mejora
- **Descripción**: ¿Por qué sería útil?
- **Ejemplos**: Casos de uso
- **Alternativas**: Otros enfoques considerados

### 3. Hacer un Pull Request

#### Preparación
1. **Fork** el repositorio
2. Clona tu fork localmente
   ```bash
   git clone https://github.com/tu-usuario/project-novaretail.git
   cd project-novaretail
   ```
3. Crea una rama para tu feature
   ```bash
   git checkout -b feature/mi-mejora
   # o para bug fixes
   git checkout -b fix/nombre-del-bug
   ```

#### Desarrollo
4. Realiza los cambios manteniendo la estructura del proyecto
5. Prueba tus cambios localmente
   ```bash
   python -m pytest  # si hay tests
   jupyter notebook  # Verifica el notebook
   ```
6. Asegúrate de que tu código sea limpio y bien documentado

#### Commit y Push
7. Commits con mensajes descriptivos
   ```bash
   git commit -m "Feat: Agregar análisis de segmentación de clientes"
   git commit -m "Fix: Corregir cálculo de correlación en datos faltantes"
   git commit -m "Docs: Actualizar sección de metodología"
   ```
8. Push a tu fork
   ```bash
   git push origin feature/mi-mejora
   ```

9. Abre un **Pull Request** en el repositorio principal

#### Descripción del PR
```markdown
## Descripción
Breve descripción de los cambios realizados.

## Tipo de Cambio
- [x] Bug fix (cambio no conflictivo que corrige un issue)
- [ ] Nueva feature (cambio no conflictivo que agrega funcionalidad)
- [ ] Breaking change (arreglo o feature que causaría cambio de comportamiento)
- [ ] Cambios en documentación

## ¿Cómo se ha probado?
Describe la prueba realizada.

## Checklist
- [ ] Mi código sigue el estilo del proyecto
- [ ] He actualizado la documentación
- [ ] Los cambios no generan warnings nuevos
- [ ] He añadido comentarios a código complejo
- [ ] Los cambios se han probado localmente
```

## 📐 Guía de Estilo

### Python
- Usa **PEP 8**
- Máximo 79 caracteres por línea
- Nombres descriptivos para variables y funciones
- Documenta funciones con docstrings

```python
def correlacion_pearson(df, col1, col2):
    """
    Calcula la correlación de Pearson entre dos columnas.
    
    Parameters
    ----------
    df : pandas.DataFrame
        DataFrame que contiene las columnas
    col1 : str
        Nombre de la primera columna
    col2 : str
        Nombre de la segunda columna
    
    Returns
    -------
    tuple
        (coeficiente, p_value)
    """
    coef, p_value = pearsonr(df[col1], df[col2])
    return coef, p_value
```

### Notebooks Jupyter
- Usa títulos claros para secciones (`## Sección`)
- Explica el propósito antes del código
- Incluye visualizaciones cuando sea relevante
- Limpia outputs antes de hacer commit
- Mantén celdas pequeñas y focalizadas

### Documentación
- Markdown con sintaxis clara
- Enlaces internos cuando sea posible
- Ejemplos de código cuando sea necesario
- Actualiza el README si es relevante

## 🔍 Proceso de Revisión

1. **Revisión automática**: GitHub Actions verificará:
   - Sintaxis válida
   - Tests (si existen)
   - Documentación actualizada

2. **Revisión manual**: Al menos un maintainer revisará:
   - Calidad del código
   - Relevancia para el proyecto
   - Documentación
   - Cumplimiento de guías

3. **Merge**: Una vez aprobado, tu PR será mergeado en `main`

## 💡 Ideas para Contribuir

### Análisis
- [ ] Análisis adicionales de segmentación
- [ ] Modelos predictivos
- [ ] Análisis de comportamiento temporal
- [ ] Benchmarking con estándares industriales

### Visualización
- [ ] Dashboards interactivos
- [ ] Gráficos adicionales
- [ ] Reportes exportables (PDF)

### Documentación
- [ ] Traducción a otros idiomas
- [ ] Tutoriales paso a paso
- [ ] Documentación de API
- [ ] Casos de uso adicionales

### Testing
- [ ] Unit tests
- [ ] Integration tests
- [ ] Test coverage

## 📚 Recursos Útiles

- [Git Tutorial](https://git-scm.com/book/es/v2)
- [GitHub Flow Guide](https://guides.github.com/introduction/flow/)
- [Markdown Syntax](https://www.markdownguide.org/)
- [Python Best Practices](https://pep8.org/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)

## ❓ Preguntas?

Si tienes dudas sobre cómo contribuir:
1. Revisa las issues existentes
2. Crea un issue con la etiqueta `question`
3. Contacta al equipo de mantenedores

## 🙏 Agradecimientos

Apreciamos tu tiempo y esfuerzo. Todas las contribuciones, sin importar el tamaño, ayudan a mejorar este proyecto.

¡Gracias por ser parte de la comunidad NovaRetail+ Analytics! 🎉
