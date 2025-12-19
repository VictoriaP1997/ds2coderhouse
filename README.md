# Anomalías en equipos industriales con inclusión de API meteorológica
## Abstract
Dentro de una industria es esencial realizar seguimiento de variables. No solo de las que tienen incidencia en resultados financieros sino también en el desempeño de la producción. El área de de mantenimiento realiza mediciones recurrentes para evitar futuros prejuicios de los equipamentos e instalaciones y asi no comprometer la seguridad de los mismos y de las personas dentro del establecimiento.

El dataset utilizado en este modelo de ML ,obtenido desde la página de Kaggle, muestra un registro de variables fisicas (Presión, temperatura, vibración y humedad) en compresores, bombas y turbinas. Los equipos están ubicados en diferentes locaciones dentro de Estados Unidos.

## Hipótesis
Se buscará encontrar una relación entre las variables físicas (Presión, temperatura de trabajo del equipo ,humedad) y las veces que ocurrieron fallas en la Turbina. El mismo análisis se puede hacer con los otros equipos del dataset.
Adicionalmente se incluirá una API que obtiene los datos de temperatura de la ciudad de Atlanta, Estados Unidos para averiguar si la temperatura ambiente incide en la probabilidad de falla de la turbina.

Se comprobará cual de las variables tiene más incidencia en los eventos de fallas. Como por ejemplo, si valores altos de vibraciones son la principal causa de fallas en Turbinas.
Posteriormente, se desarrollará un modelo de machine learning para saber si fallará o no frente a nuevos valores de variables físicas.

Una vez obtenido el modelo de predicción se optimizará el modelo de Random Forest con GridSearchCV
