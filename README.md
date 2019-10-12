**Status:** Archive (code is provided as-is, no updates expected)

# gpt-2

GPT-2, a Transformer-based language model and a successor to GPT, has shown unprecedented performance in language modeling, primarily due to its over an order of magnitude more parameters. While GPT-2’s performance on QA with no task-specific training is embryonic, it indicates that an unsupervised language model could contribute to their performance through fine-tuning.
    This repo includes an experiment of fine-tuning GPT-2 345M for Question Answering (QA). It also runs the model on Stanford Question Answering Dataset 2.0 (SQuAD).

## Testing

Open your terminal and clone https://github.com.Adminixtrator/gpt-2.git

Then run these:
    !python3 download_model.py 345M
    !export PYTHONIOENCODING=UTF-8
    
    #Changing directory..
    import os
    os.chdir('src')  #You must be in gpt-2
    
    Then install regex #pip install regex
    
    and lastly,
    
    run Test_GPT2.py 
    
    then have FUn..

## Challenges faced

Major issue was the fine-tuning of the model with BERT on the Stanford Question answering Dataset as most of the online sources had no sample to use for understanding what goes on in the fine-tunning. 

## Requirements

    fire>=0.1.3 - Fire 
    regex==2017.4.5 - For OpenAI GPT
    requests==2.21.0    - Used for downloading models over HTTP 
    tqdm==4.31.1    - progress bars in model download and training scripts
    torch>=0.4.1    - PyTorch
    boto3   - Accessing files from S3 directly.

## Colab Notebook

https://colab.research.google.com/drive/1LeOsYzxxMXDFiI3CXKgUktGZJ7Bvl2-7#scrollTo=oEQYAQ_8Rv3P

## REFERENCE

https://github.com/aswalin/SQuAD


## License

[MIT](./LICENSE)
