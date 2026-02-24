---
tags:
    - Fine-Tuning
    - Multimodal
    - Vision
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/custom-models/bedrock-fine-tuning/amazon-titan-image-generator/2-TIGFT-provisioned-throughput-inference.ipynb){:target="_blank"}"

<h2>Titan Image Generator Fine-Tuning: Provisioned Throughput Inference</h2>

This notebook demonstrates how to invoke a fine-tuned Amazon Titan Image Generator G1 model on Amazon Bedrock using provisioned throughput.

**What You'll Learn**

- Setting up provisioned throughput for your fine-tuned model
- Invoking the fine-tuned model with custom prompts
- Comparing outputs between base model and fine-tuned model
- Generating images featuring your custom-trained subjects (Ron the dog and Smila the cat)

**Prerequisites**

- Completed the fine-tuning customization job (notebook 1)
- Provisioned throughput configured for your fine-tuned model
- Access to Amazon Bedrock runtime

**Key Features**

- Side-by-side comparison of base vs fine-tuned model outputs
- Multiple prompt examples demonstrating the fine-tuned capabilities
- Seed control for reproducible results
- Visual comparison utilities

**Use Cases**

- Generating branded content with specific subjects
- Creating consistent character appearances across images
- Product visualization with custom items
- Personalized image generation for marketing

This notebook shows how the fine-tuned model can generate images featuring Ron the dog and Smila the cat in various scenarios that would not be possible with the base model.
