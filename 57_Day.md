12 Mayo 2024

## Progreso de hoy:
- Retrieval en Langchain 
## Lo que aprendí 
- retrieval is the process of fetching relevant information from a knowledge base or document store to augment the capabilities of language models.
- Similarity Search
```
smalldb.similarity_search(question, k=2)
```
-  Maximum Marginal Relevance (MMR)
```
smalldb.max_marginal_relevance_search(question,k=2, fetch_k=3)
```
- Self-query retriever 
```
document_content_description = "Lecture notes"
llm = OpenAI(model='gpt-3.5-turbo-instruct', temperature=0)
retriever = SelfQueryRetriever.from_llm(
    llm,
    vectordb,
    document_content_description,
    metadata_field_info,
    verbose=True
)
```
- Compresión
```
compressor = LLMChainExtractor.from_llm(llm)
compression_retriever = ContextualCompressionRetriever(
    base_compressor=compressor,
    base_retriever=vectordb.as_retriever()
)
```

### Question Answering 
- RetrievalQA chain
```
from langchain.chains import RetrievalQA

qa_chain = RetrievalQA.from_chain_type(
    llm,
    retriever=vectordb.as_retriever()
)
```
## **Pensamientos**:
- Es interesante cómo funciona Langchain Plus, que te muestra las peticiones al modelo 
## Link to work: 
- No work 
## Plan para mañana: 
- Terminar Memory y el pequeño curso. 
