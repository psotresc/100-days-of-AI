25 Marzo 2024
## Progreso de hoy:
- Google Vertex AI configuración 
## Lo que aprendí 
- Fine Tuning - en Vertex AI lo encotnraremos como Tuning o Tune a model
	- Hay 3 tipos de Modelos - [Link](https://cloud.google.com/vertex-ai/generative-ai/docs/models/tune-models?hl=es-419) 
		- **Ajuste supervisado**: (Supervised Tuning) El ajuste supervisado de un modelo de texto es una buena opción cuando el resultado del modelo no es complejo y es relativamente fácil de definir. 
			- Se recomienda para: la clasificación, el análisis de opiniones, la extracción de entidades, el resumen del contenido que no es complejo y la escritura de consultas específicas del dominio.
		- **Aprendizaje por refuerzo con retroalimentación humana (RLHF):** El ajuste de RLHF es una buena opción cuando el resultado de tu modelo es complejo y no se logra fácilmente con el ajuste supervisado. 
			- Se recomienda para responder preguntas, resumir contenido complejo y crear contenido, como una reescritura.
		- **Destilación de modelos:** La destilación es una buena opción si tienes un modelo grande que deseas hacer más pequeño sin disminuir su capacidad de hacer lo que deseas. El proceso de _destilación_ crea un modelo entrenado nuevo y más pequeño cuyo uso cuesta menos y tiene una latencia más baja que el modelo original.
	- Hay varios objetivos - Para la generación de textos podemos usar text-bison@002 o text-bison-32K - [Link](https://cloud.google.com/vertex-ai/generative-ai/docs/learn/models?hl=es-419#foundation_models)
		- PaLM 2 for Text - (text-bison)   
			- Cantidad máxima de tokens de entrada: 8192
			- Cantidad máxima de tokens de salida: 1024
			- Datos de entrenamiento: hasta febrero de 2023
				- text-bison@002 - Lanzamiento 6 de diciembre de 2023
				- text-bison@001 -  Lanzamiento 7 de junio de 2023	
		- PaLM 2 for Text 32,000 - (text-bison-32k)
			- Máximo de tokens (entrada + salida): 32,768  
			- Máximo de tokens de salida: 8192  
			- Datos de entrenamiento: hasta agosto de 
	 - Precios - [Link](https://cloud.google.com/vertex-ai/generative-ai/pricing?hl=es-419)   ![[Pasted image 20240325213846.png]]- 
	 - Para ajuste Supervisado - [Link video LevelUp_Plus - Fine Tuning a Model in Gemini and Vertex AI ](https://www.youtube.com/watch?v=ej_ZUcyKpoc&ab_channel=LevelUp_Plus) - [Documentación](https://cloud.google.com/vertex-ai/generative-ai/docs/models/tune-text-models-supervised?hl=en) 
		 - A veces los veremos como PEFT Models o Parameter-Efficient Fine-Tuning. Es una técnica de Procesamiento de Lenguaje Natural para mejorar el performance de LLMs en una tarea.
		 - Seleccionar un modelo entre text-bison@002 o text-bison-32k
			 - Acá una tabla de usos de caso:

| Feature        | text-bison@002     | text-bison-32k                   |
| -------------- | ------------------ | -------------------------------- |
| **Strengths**  | Shorter text tasks | Longer text tasks                |
| **Examples**   | Summarization, Q&A | Document analysis, complex Q&A   |
| **Advantages** | Stability, speed   | High capacity, in-depth   
- Relación de Epochs y training steps 
	- El número total de pasos de entrenamiento generalmente se calcula en función del número de épocas (epochs) y el tamaño del lote (batch size): 
		- Pasos de entrenamiento totales = Épocas * Batch Size
		- Si se tiene 10 000 ejemplos de entrenamiento y un tamaño de lote de 100.
			- Si entrenas durante 2 épocas: 
				- Pasos de entrenamiento totales = 2 épocas * (10 000 muestras/100 lotes/época) = 200 pasos
- input_text is 8,192 tokens y output_text es 1,024 tokens
- El número máximo de ejemplos que puede contener un conjunto de datos para un modelo de generación de texto es 10.000.
## **Pensamientos**:
- A diferencia de Open AI y su playground , Vertex AI tiene mayor complejidad 
## Link to work: 
- LATER
## Plan para mañana: 
- Continuar con Reinforced Learning from Human Feedback (RLHF) 

