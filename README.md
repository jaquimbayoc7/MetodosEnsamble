# 🤖 Métodos de Ensamble 🤖

## 📝 Descripción
Este repositorio contiene implementaciones y experimentos con diferentes métodos de ensamble para aprendizaje automático. Los métodos de ensamble combinan múltiples modelos para mejorar el rendimiento y la estabilidad de las predicciones.

## 📂 Estructura del Repositorio
- **01ExperimentosIniciales**: Contiene los primeros experimentos realizados con diferentes técnicas de ensamble.

## 🔧 Técnicas de Ensamble Implementadas
- **🌳 Bagging**: Reduce la varianza mediante el entrenamiento de múltiples modelos en diferentes subconjuntos de datos.
- **🚀 Boosting**: Mejora el rendimiento combinando modelos débiles secuencialmente.
- **🔄 Stacking**: Utiliza las predicciones de múltiples modelos como entrada para un meta-modelo.
- **🗳️ Voting**: Combina las predicciones de diferentes modelos mediante votación (promedio o ponderado).

## ✨ Ventajas de los Métodos de Ensamble
1. **📈 Mayor precisión**: Generalmente superan a los modelos individuales.
2. **🛡️ Mejor estabilidad**: Reducen la varianza y el sobreajuste.
3. **💪 Robustez**: Menos sensibles a datos atípicos y ruido.

## 🚀 Cómo Usar

```python
# Ejemplo de uso de un ensamble ponderado
from sklearn.ensemble import VotingRegressor
from sklearn.linear_model import LinearRegression
from sklearn.tree import DecisionTreeRegressor
from sklearn.svm import SVR

# Definir modelos base
models = [
    ('lr', LinearRegression()),
    ('dt', DecisionTreeRegressor()),
    ('svr', SVR())
]

# Crear ensamble
ensemble = VotingRegressor(estimators=models)

# Entrenar
ensemble.fit(X_train, y_train)

# Predecir
predictions = ensemble.predict(X_test)
```
## 📊 Resultados
Los experimentos iniciales muestran que los métodos de ensamble mejoran significativamente el rendimiento en comparación con los modelos individuales:

- **📉 Reducción del error cuadrático medio (MSE)**
- **📈 Aumento del coeficiente de determinación (R²)**
- **🧮 Mayor estabilidad en las predicciones**
  
## 🔍 Requisitos
- Python 3.7+
- scikit-learn
- numpy
- matplotlib
- pandas

## ⚙️ Instalación
```python
git clone https://github.com/jaquimbayoc7/MetodosEnsamble.git
cd MetodosEnsamble
pip install -r requirements.txt
```
## 👥 Contribuciones
Las contribuciones son bienvenidas. Por favor, sigue estos pasos:

- Haz un fork del repositorio
- Crea una rama para tu característica (git checkout -b feature/nueva-caracteristica)
- Haz commit de tus cambios (git commit -m 'Añadir nueva característica')
- Haz push a la rama (git push origin feature/nueva-caracteristica)
- Abre un Pull Request
  
## 📄 Licencia
Este proyecto está licenciado bajo la Licencia MIT - ver el archivo LICENSE para más detalles.
