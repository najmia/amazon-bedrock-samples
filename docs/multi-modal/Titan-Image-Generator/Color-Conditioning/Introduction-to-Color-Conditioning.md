---
tags:
    - Multimodal
    - Vision
    - Bedrock-SDK
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/multi-modal/Titan%20Image%20Generator/Color%20Conditioning/Introduction%20to%20Color%20Conditioning.ipynb){:target="_blank"}"

<h2>Introduction to Color Conditioning with Titan Image Generator V2</h2>

This notebook demonstrates the Color Conditioning feature in Amazon Titan Image Generator V2, which controls the color palette of generated images by providing a list of hex color codes.

**Color Conditioning Feature**

This capability allows you to:
- Control the color palette of generated images using hex color codes
- Adhere to brand color guidelines automatically
- Optionally combine color palette with reference image styling
- Generate visuals that match specific color schemes

**Key Features**

- Specify exact colors using hex codes
- Maintain brand consistency across generated images
- Combine with reference images for style transfer
- Ensure color compliance for marketing materials

**Prerequisites**

- An AWS account with access to Amazon Bedrock
- Enable Titan Image Generator V2 model access in Amazon Bedrock
- Necessary IAM permissions to invoke Amazon Bedrock models
- AWS SDK for Python (Boto3) installed

**Use Cases**

- Brand-compliant marketing content generation
- Product visualization with specific color schemes
- Design mockups matching brand guidelines
- Seasonal or themed content creation
- Consistent visual identity across campaigns

The notebook includes examples showing how to generate images with specific color palettes and how to combine color conditioning with reference images.
