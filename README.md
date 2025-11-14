# quantization-llm-benchmark
Testing and results for measuring performance loss of LLM models with the effects of quantization and context size.

# Goal
I didn't find many results that filled up a models context in a reproducable way to test their abilities. 

I'm working on 3 private benchmarks to test the abilities of a model to accurately perform tasks that is expected of them. Since we are running local models, it's important to see the effects of quantization on longer performance, especially on longer contexts.

# Benchmarks
## HistoryQA
Consists of Question and example Answer paring, as well as the marking schema to see if the answer from the LLM has mentioned the factual events, remembering the key facts. I would expect smaller models performance to drop off at a small but noticable rate when quantized and filling up longer context.

## PythonMath (WIP)
Model is asked to answer complex math questions by outputting a snippet of python code that should return the correct value.

## Toolcalling (WIP)
MOdel is provided an simulated user message that should prompt the correct toolcall.

# Limitations
My abilities to generate a private benchmark is limited to a mix of sythentic and random combinations but with reference to existing factual sources. My manual review is limited and benchmarks wont (absolutly impossible) achieve 100%. 

My budget and local hosting abilities is limited. I will test smaller models or limit my testing range. 

# Models for testing
### [Qwen3-4B-Instruct-2507-GGUF](https://huggingface.co/unsloth/Qwen3-4B-Instruct-2507-GGUF)
F16  
UD-Q8_K_XL  
UD-Q6_K_XL  
UD-Q5_K_XL  
Q5_K_S  
UD-Q4_K_XL  
Q4_K_S  
IQ4_NL  
UD-Q3_K_XL  
Q3_K_S  
UD-IQ3_XXS  
UD-IQ2_M  

### Qwen3-VL-30B-A3B-Instruct (not yet)

# Results
Preliminary HistoryQA results will be ready soon.
