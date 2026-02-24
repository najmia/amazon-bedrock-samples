---
tags:
    - Multimodal
    - Vision
    - Bedrock-SDK
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/multi-modal/Titan%20Image%20Generator/Instant%20Customization/Introduction%20to%20Instant%20Customization.ipynb){:target="_blank"}"

<h2>Introduction to Instant Customization with Titan Image Generator</h2>

This notebook demonstrates the Instant Customization feature for Amazon Titan Image Generator, which allows users to generate variations of an image by providing reference images along with a text prompt.

**Instant Customization Feature**

This powerful capability enables:
- Generate image variations guided by up to 5 reference images
- Preserve key aspects of the subject while transferring styles from references
- Mix and combine styles from multiple reference images
- Adjust the similarity strength to control how much the output resembles the references
- Use in conjunction with fine-tuned Titan Image Generator models for even more precise control

**Key Benefits**

- No complex prompt engineering required
- No model fine-tuning needed for style transfer
- Combine with fine-tuned models for maximum control
- Quick iteration on creative concepts

**Prerequisites**

- An AWS account with access to Amazon Bedrock
- Enable Titan Image Generator model access in Amazon Bedrock
- Necessary IAM permissions to invoke Amazon Bedrock models
- AWS SDK for Python (Boto3) installed

**Use Cases**

- Brand-consistent image generation
- Style transfer for creative projects
- Product visualization with specific aesthetics
- Marketing content creation with consistent visual identity

The notebook includes examples of generating images with different reference styles and similarity strengths.
