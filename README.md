<h1 color="green">gpt-2</h1>

Status: [![Status](https://img.shields.io/badge/Updates-Completed-skirretgreen)](https://github.com/openai/gpt-2) 

-------------------------

**GPT-2** - *a Transformer-based language model and a successor to GPT* - has shown unprecedented performance in language modeling, primarily due to its over an order of magnitude more parameters. While GPT-2’s performance on QA with no task-specific training is embryonic, it indicates that an unsupervised language model could contribute to their performance through fine-tuning.

-   This repo includes an experiment of fine-tuning GPT-2 345M for Question Answering _(QA)_. It also runs the model on Stanford Question Answering Dataset 2.0 _(SQuAD)_.

------------------------------------------------------------------------

## :page_with_curl: _Testing_

**1.** Open your terminal and clone this repository somewhere 

```shell    
$ git clone https://github.com.Adminixtrator/gpt-2.git
```
**2.** Download the 345M model

```shell
# from your notebook
!python3 download_model.py 345M
!export PYTHONIOENCODING=UTF-8
```
**3.** Changing directory

```python
import os
os.chdir('src')  #You must be in gpt-2
```
**4.** Install regex 

```shell
$ pip install regex
```
**5** Run the model

```shell
run Test_GPT2.py 
```
See the [Colab Notebook](https://colab.research.google.com/drive/1LeOsYzxxMXDFiI3CXKgUktGZJ7Bvl2-7#scrollTo=oEQYAQ_8Rv3P) if you seem to have issues with testing and working with SQuAD.

**_Happy Developing!_**

-------------------------------------------------------

## Challenges faced

Major issue was the fine-tuning of the model with **BERT** on the Stanford Question answering Dataset _(SQuAD)_ as most of the online sources had no sample to use for understanding what goes on in the fine-tunning. 

## Requirements

```python
fire>=0.1.3 # Fire 
regex==2017.4.5 # For OpenAI GPT
requests==2.21.0    # Used for downloading models over HTTP 
tqdm==4.31.1    # progress bars in model download and training scripts
torch>=0.4.1    # PyTorch
boto3   # Accessing files from S3 directly.
```

**REFERENCE** - [SQuAD](https://github.com/aswalin/SQuAD)

--------------------------------------------
## Credentials

### License: [![Status](https://img.shields.io/badge/MIT-Approved-blue)](./LICENSE)
