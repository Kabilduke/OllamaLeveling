<h1 align= center>Ollama in Notebook and VSCode</h1>

## 1. $Ollama$
```
pip install ollama
```
```py
import ollama

for chunk in ollama.chat(
  model = 'llama3.2:1b', #Enter Model name
  messages = [{
    'role': 'user',
    'content': "Uses of Github?"
  }],
  stream = True
):

  print(chunk['message']['content'], end= "", flush = True)
```

## 2. $Ollama$ & $Langchain$
```
pip install langchain langchain-community
```
```py
from langchain-commmunity.chat_models import ChatOllama

LLM = ChatOllama(model = 'llama3.2:1b') #Enter Model name

response = LLM.invoke("Uses of Ollama?")
print(response.content)
```
