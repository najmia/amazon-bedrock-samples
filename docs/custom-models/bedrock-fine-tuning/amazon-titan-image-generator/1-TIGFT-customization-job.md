---
tags:
    - Fine-Tuning
    - Multimodal
    - Vision
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/custom-models/bedrock-fine-tuning/amazon-titan-image-generator/1-TIGFT-customization-job.ipynb){:target="_blank"}"

<h2>Fine-Tuning Amazon Titan Image Generator G1</h2>

This notebook demonstrates how to fine-tune Amazon Titan Image Generator G1 on Amazon Bedrock to recognize custom classes and generate images with specific subjects.

**Use Case**

The notebook teaches the model to recognize two new classes:
- Ron the dog
- Smila the cat

After fine-tuning, you can generate images featuring these specific subjects in various scenarios and styles.

**What You'll Learn**

- Preparing training data for Titan Image Generator fine-tuning
- Creating a model customization job on Amazon Bedrock
- Configuring fine-tuning hyperparameters
- Monitoring the fine-tuning job progress
- Understanding the fine-tuning process and requirements

**Prerequisites**

- Amazon SageMaker Studio with Data Science 3.0 kernel
- Access to Amazon Bedrock
- Training images of your custom subjects
- IAM permissions for Bedrock model customization

**Training Data Requirements**

- Minimum 8 images per class
- Images should show the subject from different angles and in different settings
- Clear, high-quality images work best
- Consistent subject across all training images

**Next Steps**

After completing this notebook, proceed to the provisioned throughput inference notebook to test your fine-tuned model.
