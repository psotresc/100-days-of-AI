26 Marzo 2024

## Progreso de hoy:
- H2o .ai Plataforma 
- Lectura de Papers - Transferencia de estilo 
## Lo que aprendí 
- Uso de RAG's (Retrieval Augmented Generation) utilizando embeddings
	- Ajuste de parámetros 
		- Top P - ofrece un control sobre la creatividad y la previsibilidad de las respuestas de los LLM. Permite controlar la aleatoriedad de la salida del texto. Te ayuda a encontrar un equilibrio entre las opciones más probables y la creatividad en las respuestas. Le dices al modelo un valor de probabilidad (P) que actúa como un filtro.
			- Establece un umbral.
				- Ejemplo Top P alto (0.9) - Abanico más amplio de palabras. Solo considerará las palabras que tengan una probabilidad individual mayor o igual al 90%
				- Ejemplo Top P bajo (0.3) - Limita drásticamente las opciones a las palabras. Sólo las que obtienen el 30% de probabilidad.
		- Top K - Al igual que Top P, sirve para influenciar la creatividad y la previsibilidad de las respuestas. En lugar de basarse en probabilidades (top P), Top k te permite definir un número específico de opciones (k) que el modelo considerará para continuar la oración o frase.
			- Limita las opciones
				- Ejemplo K alto (50):  El modelo considere 50 apalabras, un abanico más amplio de palabras dentro de las más probables. Esto puede generar respuestas más variadas y creativas
				- Ejemplo K bajo (5): Limita drásticamente a las 5 opciones, las absolutamente más probables. Esto da como resultado respuestas predecibles y seguras. 
		- Temperatura-  Es un parámetro que controla la aleatoriedad de la salida del texto.
	- Cómo se combinan: 
		- **Para salidas más creativas:** Probar con un Top P alto o un Top k moderado.
		- **Para salidas más seguras:** Utilizar un Top P bajo o un Top k muy bajo.
- Entrenamiento sobre Mixtral 8x7B 
	- 32k context window
	- Funciona bien en español 
- Uso de Plataforma [H20.ai ](https://h2o.ai/)
- Repaso de Notebook LM 
	- Sólo aplicable a inglés y en Estados Unidos. 
	- Funciona con VPN
- Lectura de Papers sobre transferencia de estilo 
	- Low-Resource Authorship Style Transfer: Can Non-Famous Authors Be Imitated? - [Link](https://arxiv.org/pdf/2212.08986.pdf)
	- Deep Learning for Text Style Transfer: A Survey - [link](https://aclanthology.org/2022.cl-1.6.pdf)
	- 

## **Pensamientos**:
- Está interesante, sólo que siento que hay un montón de opciones, creo que debería de empezar a usar un sólo modelo. Determina cuál es el más barato bajo una métrica. 
## Link to work: 
- Hoy fue teórico
## Plan para mañana: 
- Leer más papers
