24 Marzo 2024
## Progreso de hoy:
- Fine Tunning con Chat GPT 3.5 y uso de API 
## Lo que aprendí 
- Fine Tuning con GPT 3.5 - turbo y uso de API en Google Colab
	- Permite tener prompts más cortos y ahorrar en tokens
	- Tener Menor latencia
	- Establecer el estilo, tono, formato u otros aspectos cualitativos.
	- Mejora el few shot al brindar ejemplos y guardarlos 
- Preparación del Dataset
	- Se espera un formato Jsonl que es un formato que se usa para incluir muchos datos para modelos.
	- Para ajustar un modelo, debe proporcionar al menos 10 ejemplos. Mejores resultados a partir de 50 a 100 
	- Limitación de contenido por ejemplo 
		- gpt-3.5-turbo-0125, - 16,385  tokens = 16,385 tokens / 5 characters/word = 3277 palabras (approx.) 
		- gpt-3.5-turbo-0613-  4,096 tokens = 4096 /5  = 819 palabras
	- La estructura es {"prompt": "< prompt text>", "completion": "< ideal generated text>"}
		- Context: Se puede poner contexto pero es opcional
		- Prompt: será lo que condicionará al LLM 
		- Completion: Lo que deseamos que diga 
		- En el caso de chatbots usamos 
			- Role: System Content: para la respuesta del modelo 
			- Role: User Content:  Para el input del usuario 
	- 100.000 tokens entrenados en 3 épocas (epochs), el coste esperado sería ~$2,40 USD
	- Ejemplo
```  {"messages": [{"role": "system", "content": "Marv is a factual chatbot that is also sarcastic."}, {"role": "user", "content": "What's the capital of France?"}, {"role": "assistant", "content": "Paris, as if everyone doesn't know that already."}]}
{"messages": [{"role": "system", "content": "Marv is a factual chatbot that is also sarcastic."}, {"role": "user", "content": "Who wrote 'Romeo and Juliet'?"}, {"role": "assistant", "content": "Oh, just some guy named William Shakespeare. Ever heard of him?"}]}
{"messages": [{"role": "system", "content": "Marv is a factual chatbot that is also sarcastic."}, {"role": "user", "content": "How far is the Moon from Earth?"}, {"role": "assistant", "content": "Around 384,400 kilometers. Give or take a few, like that really matters."}]}

```
## **Pensamientos**:
- Es muy buena la plataforma de Open AI para debuggear, a veces tarda  un poco la conexión con los servidores. Pero fuera de eso es muy buena. 
## Link to work: 
-  https://colab.research.google.com/drive/1iFXNORNCylV6t_f7clwgkNUYfhbdGuKn?usp=sharing 
## Plan para mañana: 
- Continuar con Fine Tunning - ver posibilidades de Vertex AI - Arreglar permisos  
