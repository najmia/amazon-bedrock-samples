---
tags:
    - Fine-Tuning
    - Vision
    - Multimodal
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/custom-models/bedrock-fine-tuning/nova/canvas/1-CanvasFT-customization-job.ipynb){:target="_blank"}"

# Amazon Nova Canvas Model Fine-tuning - Customization Job

### Overview

This notebook provides step-by-step instructions on how to customize the Amazon Nova Canvas model. Amazon Nova Canvas delivers high-quality images, with the flexibility to tailor visual outputs to match your creative needs. It can perform advanced image editing tasks such as in-painting, out-painting, image conditioning and many more. 

You will learn how to prepare the training dataset and launch a fine-tuning job to adapt the model to unique characteristics in custom datasets that the model is not already trained on.

| Ron the dog| Smila the cat|
|---------|---------|
| <img src="data/ron_01.jpg" alt="Image 1" width="300"/> | <img src="data/smila_29.jpg" alt="Image 2" width="300"/> |

### What You'll Learn

- How to prepare training datasets for Nova Canvas fine-tuning
- How to launch a customization job using Amazon Bedrock
- Best practices for fine-tuning image generation models
