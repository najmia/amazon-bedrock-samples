---
tags:
    - Multimodal
    - Vision
    - Bedrock-SDK
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/multi-modal/Titan%20Image%20Generator/Background%20Removal/Introduction%20to%20Background%20Removal.ipynb){:target="_blank"}"

<h2>Introduction to Background Removal with Titan Image Generator V2</h2>

This notebook demonstrates the Background Removal feature introduced in Amazon Titan Image Generator V2, which automatically removes backgrounds from images containing multiple objects, isolating the foreground subjects.

**Background Removal Feature**

The Background Removal capability allows you to:
- Automatically remove backgrounds from images
- Isolate foreground subjects
- Process images with multiple objects
- Generate clean product images for catalogs
- Create transparent backgrounds for design work

**Prerequisites**

- An AWS account with access to Amazon Bedrock
- Enable Titan Image Generator V2 model access in Amazon Bedrock
- Necessary IAM permissions to invoke Amazon Bedrock models
- AWS SDK for Python (Boto3) installed

**Use Cases**

- E-commerce product photography
- Marketing materials creation
- Design and creative workflows
- Image preprocessing for other AI tasks

The notebook includes practical examples with visualization of original and processed images side-by-side.
