18 Marzo 2024
## Progreso de hoy:
- Creación de Modelo para el cambio de caras de personajes - Preparación de imágenes , detección y predicción de puntos. Y triangulación de cara.
## Lo que aprendí 
- Acerca de la librería dlib
- Dlib Detector y predictor para sacar caras y landmarks 
- Uso de Landmarks con dlib de 68 puntos
- Cómo sacar triángulos de los landmarks haciendo uso de la triangulación de Delaunay
	- cv2.boundingRect - Crear un rectángulo
	- cv2.Subdiv2D - Subdividir una figura
	- subdiv.getTriangleList()  - Crear triángulos
	- Np.where - Crear un nuevo array con las condiciones 
	- 
## **Pensamientos**:
- Es interesante ver la optimización de triángulos 
- Hay muchos procesos que si corriera sólo el código no entendería 
## Link to work: 
- https://colab.research.google.com/drive/17uz1rVI2mufyEcWpOOgIHrhBhikogCQs?usp=sharing 
## Plan para mañana: 
- Terminar y trabajar el proyecto con Flask 
