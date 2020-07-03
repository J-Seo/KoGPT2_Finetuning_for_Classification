# KoGPT2_Finetuning_for_Classification.pytorch

Fine-tuning [SKT-KoGPT2](https://github.com/SKT-AI/KoGPT2) for Korean Sentiment Analysis [NSMC](https://github.com/e9t/nsmc) based on [SKT-KoBERT](https://github.com/SKTBrain/KoBERT) code


## Result

Test accuracy for NSMC **88%**


<img src = "https://github.com/J-Seo/KoGPT2_Finetuning_for_Classification/blob/master/result_img/epoch_5_result.png">




## Introduction

This repository is KoGPT2 fine-tuning for binary-classification (Korean).  

## Why you need this repo?

In KoGPT2 repository, there is no solution to fine-tuning for NSMC task (text classification). 

## Where I modify?

- Pooler

I made it to fit on Pytorch and add pooler hidden state in GPT2 classifier's forward. Also, I consider the place of 
indexing pooler output for the way of sentence representation in text classification for GPT2.

- GPT2 module 

I refer to [Huggingface-transformers](https://huggingface.co/transformers/) for getting the hint that how to set up
GPT2 functions' arguments. 

- KoBERT to KoGPT2

Most of the code is very similar to koBert. This is because, I made the maximum use the original BERT-pytorch frame.

## Setting

Python 3.6+

Pytorch 1.5

CUDA 10.2

or

Colab-pro (for gpu)

## installation

!pip install -r requirements.txt

## How to use

- Colab link

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/J-Seo/KoGPT2_Finetuning_for_Classification/blob/master/kogpt2_script/gpt2_text_classification_finetune_torch.ipynb)

With this link, you just download this repository and upload it in your own google drive path. 
