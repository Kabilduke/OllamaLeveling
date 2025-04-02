# Default input tokens by ollama $'2048'$ tokens

#### Step1: Check max input tokens
```
ollama show deepseek-r1:1.5b
```
#### Step2: Run the Model
```
ollama run deepseek-r1:1.5b
```
#### Step3: Change input token (context length)
```
/set parameter num_ctx 131072
```
#### Step4: Save the Model
```
/save deepseek-r1:max
```
#### Check the saved model
```
ollama ls
```
