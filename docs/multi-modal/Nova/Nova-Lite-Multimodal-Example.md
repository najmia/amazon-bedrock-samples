---
tags:
    - Multimodal
    - Vision
    - Bedrock-SDK
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/multi-modal/Nova/Nova-Lite-Multimodal-Example.ipynb){:target="_blank"}"

<h2>Interacting with Amazon Nova-Lite with images</h2>

This notebook demonstrates how to use Amazon Nova Lite's multimodal capabilities to process and analyze images. Amazon Nova Lite is a very low-cost multimodal model that is lightning fast for processing image, video, and text inputs to generate text output.

The notebook covers:

- Setting up dependencies and the Bedrock runtime client
- Building helper functions to encode images and send them to the model
- Using the Converse API to interact with Nova Lite
- Multiple use cases including:
  - Image description
  - Vehicle damage assessment for insurance claims
  - Structured data extraction from product images
  - Chart and graph analysis

Amazon Nova Lite can handle real-time customer interactions, document analysis, and visual question-answering tasks with high accuracy. The model processes inputs up to 300K tokens in length and can analyze multiple images or up to 30 minutes of video in a single request.
