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

## Conclusiones Finales
En primer instancia recordemos nuestra hipótesis.

*Se comprobará si alguna de las variables tiene más incidencia en los eventos de fallas*

La matriz de correlación lanzó que las 3 principales variables que influyen en la probabilidad de fallo de la turbina son.

-Vibraciones

-Presión

-Temperatura de trabajo del equipo

Esto se condice con los principios de mecánica de equipamientos industriales. 
Altos valores de vibraciones hace que haya fricción entre partes estáticas y rotativas, disminuyendo la vida útil de acoplamientos, cojinetes, etc e induciendo finalmente el fallo de la turbina.

Valores de presión fuera de lo recomendado por el fabricante pueden hacer que el vapor que ingresa a la turbina (en caso que sea una turbina de vapor) condense generándose asi pequeñas microgotas. Las mismas al chocar contra los álabes de la turbina que giran a grandes rpm funcionan como granos de arena que los erosionan, conduciendo asi al fallo. De igual manera influye la temperatura a la que trabaja el equipo, esta variable también afecta en la calidad del vapor utilizado.

Una vez entendido en problema y como se relacionan las variables, creamos un modelo de machine learning  con RandomForest que prediga la probabilidad de fallo de la turbina según ciertos valores de las variables físicas críticas que la matriz de correlación arrojó.
Para hacer aún más robosto nuestro modelo, lo optimizamos por hiperparámetros con GridSearchCV (cross-validation). Esto permitirá que una vez que esté en producción, las predicciones sean confiables ante la presencia de nuevos datos. 

## Resultados
Se encontró efectivamente que la variable que más incide sobre la falla de Turbinas, son las vibraciones del equipamiento.
Desde el punto de vista mecánico esto se justifica por el hecho de que si en un equipo rotante está desalineado, el equipo presentará vibraciones que causarán mayor desgaste en el punto de contacto entre las partes estáticas y las partes móviles. LLegando así a la falla del equipamiento.
