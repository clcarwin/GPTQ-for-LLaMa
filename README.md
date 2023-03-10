# GPTQ-for-LLaMa
4 bits quantization of [LLaMa](https://arxiv.org/abs/2302.13971) using [GPTQ](https://arxiv.org/abs/2210.17323)

GPTQ is SOTA one-shot weight quantization method

## How to use
```
pip install git+https://github.com/zphang/transformers@llama_push

git lfs install
git clone https://huggingface.co/decapoda-research/llama-7b-hf
git clone https://github.com/clcarwin/GPTQ-for-LLaMa-Inference
cd GPTQ-for-LLaMa-Inference

# Download llama-7b-4bit_part* from release page
cat llama-7b-4bit_part* > llama-7b-4bit.pt

# Install kernels
python setup_cuda.py install

python llama_inference.py ../llama-7b-hf --wbit 4 --load llama-7b-4bit.pt --text "this is a"
```


## Acknowledgements
This code is based on [GPTQ](https://github.com/IST-DASLab/gptq) and [GPTQ-for-LLaMa](https://github.com/qwopqwop200/GPTQ-for-LLaMa)

Thanks to Meta AI for releasing [LLaMa](https://arxiv.org/abs/2302.13971), a powerful LLM.
