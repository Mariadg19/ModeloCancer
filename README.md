# ModeloCancer
Modelo para identificar el cáncer de mama

Estudiante: María de los Ángeles Delgado Giraldo

Introducción

En un principio, iba a trabajar con un dataset propio que contenía fotografías de cubos de colores, pero tuve muchos inconvenientes en el pre-procesamiento de los datos y me di cuenta que me estaba complicando mucho, así que decidí utilizar un dataset de la plataforma Kaggle, el cual es un Conjunto de datos de Wisconsin (diagnóstico) de cáncer de mama y la idea es predecir si es benigno o maligno. Este contiene un total de 569 muestras, 10 característica como el radio, textura, perímetro, área, uniformidad, compacidad, concavidad, puntos cóncavos, simetría y dimensión fractal y dos etiquetas que corresponden a maligno o benigno.

Desarrollo

El modelo se encuentra en la librería sklearn, así que lo primero es importarlo, para resolver el modelo se utiliza regresión logística. Se dividen los datos de validación y entrenamiento, se procede a entrenar el modelo, luego cambio el parámetro C para ajustar la regularización del modelo, este es un factor de penalización que fuerza que la estimación de los coeficientes que no son significativos tiendan a cero, se escoge un C igual a 100 y se puede verificar en los resultados. Luego procedemos a realizar un pre-procesamiento de los datos, en donde estos se normalizan por medio MinMaxScaler y se aplica PCA. El dataset original es representado en un 84,68% al hacer el PCA, por lo que concluimos que no es conveniente utilizarlo ya que se pierde parte significativa de la información.  Luego se aplican otros dos modelos, los cuales son SVM y KNN, obteniendo mejores resultados en el modelo de regresión logística.


Resultados

![image](https://user-images.githubusercontent.com/105176633/171983863-e892e733-a46e-4efb-be0d-9dee772bfc09.png)

Como se puede observar estos fueron los resultados obtenidos al aplicar cada modelo, con regresión logística se obtuvo el mejor resultado, variando el parámetro C. Sino se hubiera variado, obteníamos un 0.951, es decir igual al modelo SVM. 

Conclusiones

•	La realización de este proyecto nos ayudó a poner en práctica muchos de los conceptos vistos en clase, lo cual es fundamental para complementar el aprendizaje.
• En este caso se ajusta mejor el modelo de regresión logística al realizar un cambio en uno de sus parámetros, por lo tanto es muy importante tener en cuenta estas variaciones para así mejorar los resultados. En comparación con el modelo de SVM, al cuál no se le hizo cambio en los parámetros,también tuvo buenos resultados, tal vez si se le hubiera hecho una mejora en los parámetros hubiéramos obtenido aún mejores resultados.
• Me gustó mucho el poder analizar este conjunto de datos, debido a la gran demanda e importancia en la identifivación y detección temprana del cáncer de mama es necesaria esta aplicación de técnicas de inteligencia artificial para así poder llevarla a los territorios más apartados sin necesidad de un médico especializado, mejorando así la calidad de vida de las mujeres.
