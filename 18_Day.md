21 Marzo 2024

## Progreso de hoy:
- Modelo de multiclasificación de aves, analizar los elementos que no conocía y repasarlos. 
## Lo que aprendí 
- random_state - sklearn es un valor para hacer el shuffle de los valores es una variable entera, puede ser hasta 2147483647
- LabelBinarizer() - una función para hacer one hot encoding de valores categóricos
- fit_transform - usa fit para sacar las categorías y transform para hacer el one hot encoding
- Repasar categorical_crossentropy - una función de pérdica usada para evaluar el performance de la clasificación de modelos. Con categorical se refiere a las categorías y con crossentrop y se refiere a que mide la diferencia entre dos probabilidades de distribución.
	- Probabilidad de distribución se refiere a que si tengo tres clases, perro, gato y conejo. Y sé que una imagen tiene .7 de ser perro .2 de gato y .1 de conejo . 
- plot de loss function - que tanto se equivoca el modelo, entre menor sea mejor. Es la diferencia entre la predicción y el valor real. A diferencia de accuracy que mide la proporción o porcentaje de correctos, generalmente están inversamente relacionadas.
## **Pensamientos**:
- Hoy fue un repaso, fue interesante poder entender mejor un modelo de multi clasificación de una mejor manera. 
## Link to work: 
- https://colab.research.google.com/drive/1Z0HqdC9PjaEqk8NEg6ceL7f2ZGEJlsov?usp=sharing 
## Plan para mañana: 
-  Continuar con ejercicios. 
