15 Mayo 2024

## Progreso de hoy:
- Aprendizaje de modelos 
## Lo que aprendí 
- Modelos más famosos, evaluaciones y métricas.
	- Leaderboard OPen Source https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard 
	- All models Arena  https://huggingface.co/spaces/lmsys/chatbot-arena-leaderboard 
	- Uso de la librería de transformers e importación de modelos 

```
chatbot = pipeline(task="conversational",
                   model="./models/facebook/blenderbot-400M-distill")

translator = pipeline(task="translation",
                      model="./models/facebook/nllb-200-distilled-600M",
                      torch_dtype=torch.bfloat16) 
```
	
	- Modelos para traducción y modelos para conversación 
## **Pensamientos**:
- Que cantidad de modelos, no sé si soy más del team open source, o estar en los modelos cerrados.
## Link to work: 
- 
## Plan para mañana: 
- 
