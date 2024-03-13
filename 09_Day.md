12 Marzo 2024

## Progreso de hoy:
- Repaso de Fine tuning en LLMS - Open AI
## Lo que aprendí 
- Estuve viendo algunas cosas de Fine tuning con Llama a través de Gradient - Creación de personajes - [Create Custom AI Characters Easily 🎭 How To Fine-Tune LLMs For AI Role Play de Matthew Berman](https://www.youtube.com/watch?v=CoM-HKM-CzM&ab_channel=MatthewBerman) 
-  Repasar las diferencias entre fine tuning y transfer modelling 
	- Leyendo un artículo interesante: [How to train ChatGPT on your own text](https://mythicalai.substack.com/p/how-to-train-chatgpt-on-your-own) 
	- Brinqué un poco a entender algunas de las bases del perceptron con el video de [But what is a neural network?](https://www.youtube.com/watch?v=aircAruvnKk&t=221s&ab_channel=3Blue1Brown) 
		- Me clavé en la función de sigmoid y lo que representa el número de Euler "E" 
	- Repasé Finetuning - Que es donde se toma un modelo existente y luego se agregan sus propios datos encima.
		- Límite de caracteres para texto 4,096 tokens para gpt-3.5-turbo [Link](https://platform.openai.com/docs/guides/text-generation/which-model-should-i-use)
		- Límite para fine tuning de gpt-3.5-turbo-0125, es de 16,385 tokens [Link](https://platform.openai.com/docs/guides/fine-tuning/token-limits)
		- Para ver la tokenización está la herramienta oficial de Open AI [Link](https://platform.openai.com/tokenizer)  y también Tiktokenizer [Link](https://tiktokenizer.vercel.app/)
		- Una regla general útil es que un token generalmente corresponde a ~4 caracteres de texto para texto común en inglés. 
			- Esto se traduce en un token por aproximadamente ¾ de palabra, por lo que 100 tokens ≈ 75 palabras.
			-   Los precios son: https://openai.com/pricing  
				- gpt-3.5-turbo - $8.00 / 1M tokens
				- davinci-002 - $6.00 / 1M tokens
				- babbage-002  - $0.40 / 1M tokens
			- Harry Potter tiene 1,084,170 palabras 
				- 1,084,170 palabras *  .75 ( token por aproximadamente ¾ de palabra) = 813,127.5 tokens 
				-  813.127,5 tokens si el costo  de 1 millón de tokens es de 8 dólares = por  entrenar una vez en chat gpt turbo costaría $6.51   
				- El número predeterminado que se utilizan sus tokens para entrenar (llamado epoch) es 4. Por lo que el total sería de $26.04 USD 
	- Hice un repaso de embeddings (Incrustaciones) que nos permiten comparar elementos, sin tener que comparar el elemento en su conjunto. [Artículo interesante](https://mythicalai.substack.com/p/how-to-fine-tune-train-stable-diffusion#%C2%A7what-are-embeddings-in-machine-learning)
## **Pensamientos**:
- Es súper interesante las opciones que hay para hacer los entrenamientos hoy en día. 
- Es muy cambiante el entorno. Y el precio ha bajado considerable en menos de 1 año 
## Link to work: 
- Sin archivo - Puro teórico 
## Plan para mañana: 
- Retomar algunos ejercicios prácticos. 
