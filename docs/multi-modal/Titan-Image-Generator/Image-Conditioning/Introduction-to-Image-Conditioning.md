---
tags:
    - Multimodal
    - Vision
    - Bedrock-SDK
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/multi-modal/Titan%20Image%20Generator/Image%20Conditioning/Introduction%20to%20Image%20Conditioning.ipynb){:target="_blank"}"

<h2>Introduction to Image Conditioning with Titan Image Generator V2</h2>

This notebook demonstrates the Image Conditioning feature in Amazon Titan Image Generator V2, which generates outputs that follow the layout and structure of a user-supplied reference image.

**Image Conditioning Modes**

Two conditioning modes are supported:

1. **Canny Edge**: Extract prominent edges from the reference image to guide the generation process
2. **Segmentation**: Define specific regions/objects within the reference image for the model to generate content aligned with those areas

**Key Features**

- Generate images that maintain the structure and layout of reference images
- Combine reference image structure with text prompts for creative control
- Preserve composition while changing content
- Useful for maintaining consistent layouts across variations

**Prerequisites**

- An AWS account with access to Amazon Bedrock
- Enable Titan Image Generator V2 model access in Amazon Bedrock
- Necessary IAM permissions to invoke Amazon Bedrock models
- AWS SDK for Python (Boto3) installed

**Use Cases**

- Maintaining consistent layouts in design work
- Generating variations while preserving composition
- Architecture and interior design visualization
- Product placement in specific layouts
- Creative exploration with structural constraints

The notebook includes examples demonstrating both Canny Edge and Segmentation modes with side-by-side comparisons.
