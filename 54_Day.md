06 Mayo 2024

## Progreso de hoy:
- Inicié curso de Langchain - Aprendizaje de Importación y splitting
## Lo que aprendí 
- Importación de PDFs con PyPDFLoader

```
from langchain.document_loaders import PyPDFLoader
loader = PyPDFLoader("docs/cs229_lectures/MachineLearning-Lecture01.pdf")
pages = loader.load()

```

- Importación de Videos de Youtube con  yt_dlp y pydub - y haciendo uso de OpenAIWhisperParser VIdeos completos de una hora 

```
from langchain.document_loaders.generic import GenericLoader
from langchain.document_loaders.parsers import OpenAIWhisperParser
from langchain.document_loaders.blob_loaders.youtube_audio import YoutubeAudioLoader

url="https://www.youtube.com/watch?v=jGwO_UgTS7I"
save_dir="docs/youtube/"
loader = GenericLoader(
    YoutubeAudioLoader([url],save_dir),
    OpenAIWhisperParser()
)
docs = loader.load()
```

URL 
```
from langchain.document_loaders import WebBaseLoader

loader = WebBaseLoader("https://github.com/basecamp/handbook/blob/master/37signals-is-you.md")

docs = loader.load()
```

Splitting 
Uso de Splitters en caractéres y espacios 

```
## from langchain.text_splitter import RecursiveCharacterTextSplitter, CharacterTextSplitter

from langchain.text_splitter import CharacterTextSplitter
text_splitter = CharacterTextSplitter(
    separator="\n",
    chunk_size=1000,
    chunk_overlap=150,
    length_function=len
)
```

tokens 
```
from langchain.text_splitter import TokenTextSplitter 

text_splitter = TokenTextSplitter(chunk_size=1, chunk_overlap=0)

```

Context aware splitting
```
from langchain.text_splitter import MarkdownHeaderTextSplitter

headers_to_split_on = [
    ("#", "Header 1"),
    ("##", "Header 2"),
    ("###", "Header 3"),
]

markdown_splitter = MarkdownHeaderTextSplitter(
    headers_to_split_on=headers_to_split_on
)
md_header_splits = markdown_splitter.split_text(markdown_document)

```

## **Pensamientos**:
- Una capacidad para hacer cosas con Youtubers. 
## Link to work: 
- No work, just learning 
## Plan para mañana: 
- Continuar curso. 
