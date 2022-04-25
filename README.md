# Garbage Classification

## Overview

### Backgroud
Garbage classification refers to the separation of several types of different categories in accordance with the environmental impact of the use of the value of the composition of garbage components and the requirements of existing treatment methods.

The significance of garbage classification: 
1. Garbage classification reduces the mutual pollution between different garbage, which is beneficial to the recycling of materials. 
2. Garbage classification is conducive to reducing the final waste disposal volume. 
3. Garbage classification is conducive to enhancing the degree of social civilization.

### Dataset
The garbage classification dataset is from Kaggle. There are totally 2467 pictures in this dataset. And this model is an image classification model for this dataset. There are 6 classes for this dataset, which are cardboard (393), glass (491), metal (400), paper(584), plastic (472), and trash(127).

### Model
The model is based on the [ViT](https://huggingface.co/google/vit-base-patch16-224-in21k) model, which is short for the Vision Transformer. It was introduced in the paper [An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale](https://arxiv.org/abs/2010.11929), which was introduced in June 2021 by a team of researchers at Google Brain. And first released in [this repository](https://github.com/rwightman/pytorch-image-models). I trained this model with PyTorch. I think the most different thing between using the transformer to train on an image and on a text is in the tokenizing step. 

There are 3 steps to tokenize the image:
1.	Split an image into a grid of sub-image patches
2.	Embed each patch with a linear projection
3.	Each embedded patch becomes a token, and the resulting sequence of embedded patches is the sequence you pass to the model.

I trained the model with 10 epochs, and I use Adam as the optimizer. The accuracy on the test set is 95%.

## Huggingface Space
Huggingface space is [here](https://huggingface.co/yangy50/garbage-classification).

## Huggingface Model Card
Huggingface model card is [here](https://huggingface.co/yangy50/garbage-classification/tree/main).

## Critical Analysis
1. Next step: build a CNN model on this dataset and compare the accuracy and training time for these two models.

2. Didn’t use the Dataset package to store the image data. Want to find out how to use the Dataset package to handle image data.


## Resource Links

[vit-base-patch16-224-in21k](https://huggingface.co/google/vit-base-patch16-224-in21k)

[Garbage dataset](https://huggingface.co/cardiffnlp/twitter-roberta-base)

[An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale](https://arxiv.org/abs/2010.11929)

## Code Demo

[Code Demo](https://github.com/yuechen-yang/garbage-classification) is inside this repo

## Repo
In this repo

## Video Recording
