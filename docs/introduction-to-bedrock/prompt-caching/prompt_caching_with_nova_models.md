---
tags:
    - Prompt-Engineering
    - Bedrock-SDK
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/introduction-to-bedrock/prompt-caching/prompt_caching_with_nova_models.ipynb){:target="_blank"}"

<h2>Prompt Caching with Amazon Nova models</h2>

This notebook demonstrates how to use prompt caching with Amazon Nova models (Nova Micro, Nova Lite, and Nova Pro) using both the Bedrock Converse API and InvokeModel API.

Prompt caching allows you to cache frequently used context across multiple model invocations, which is especially valuable for:

- Document Q&A systems where users ask multiple questions about the same document
- Coding assistants that maintain context about code files
- Applications with long, repeated prompts

The cached context remains available for up to 5 minutes after each access, with each cache hit resetting this countdown.

The notebook includes:

- Understanding prompt caching benefits and use cases
- Implementation with InvokeModel API
- Implementation with Converse API
- A practical use case: Chat with document
- Optimal prompt structure for caching (separating static and dynamic content)
- Examples showing cache write and cache read operations

This feature helps reduce costs and improve response times for applications that repeatedly use the same context or instructions.
