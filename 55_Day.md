07 Mayo 2024

## Progreso de hoy:
- Primer día de AI Creativa 
- Embeddings 
## Lo que aprendí 
### Embeddings Open AI
```
from langchain.embeddings.openai import OpenAIEmbeddings
embedding = OpenAIEmbeddings()

sentence1 = "i like dogs"
sentence2 = "i like canines"

embedding1 = embedding.embed_query(sentence1)
embedding2 = embedding.embed_query(sentence2)

np.dot(embedding1, embedding2)

```
### Vector store - Chroma 
```
from langchain.vectorstores import Chroma
persist_directory = 'docs/chroma/'
!rm -rf ./docs/chroma  # remove old database files if any
vectordb = Chroma.from_documents(
    documents=splits,
    embedding=embedding,
    persist_directory=persist_directory
print(vectordb._collection.count())
)

## K3 es el número de resultados de regreso
docs = vectordb.similarity_search(question,k=3)
```
## **Pensamientos**:
- 
## Link to work: 
- 
## Plan para mañana: 
- 
