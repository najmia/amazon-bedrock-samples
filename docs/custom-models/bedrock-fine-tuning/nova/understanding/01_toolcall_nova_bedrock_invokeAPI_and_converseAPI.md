---
tags:
    - Agents
    - Fine-Tuning
    - Bedrock-SDK
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/custom-models/bedrock-fine-tuning/nova/understanding/nova_tooluse_customization/tooluse_finetuner_main/notebooks/01_toolcall_nova_bedrock_invokeAPI_and_converseAPI.ipynb){:target="_blank"}"

# Tool Calling with Nova - Invoke API and Converse API

### Overview

This notebook demonstrates how to use Amazon Bedrock Invoke API and Converse API for tool use with Amazon Nova models. You'll learn how to configure tools, structure prompts, and format messages to align with both Bedrock APIs.

### What You'll Learn

- How to use Amazon Bedrock Invoke API for tool calling
- How to use Amazon Bedrock Converse API for tool calling
- Proper tool configuration format for both APIs
- How to structure prompts and messages for tool use
- Testing tool calling with different input questions

### Key Concepts

This notebook shows you how the tool config, prompt and messages API should look like to align with:
- **Bedrock Converse API** - Unified conversation interface
- **Bedrock Invoke API** - Direct model invocation

You can check how they work by using different input questions with a predefined set of tools.

### Prerequisites

- AWS account with Amazon Bedrock access
- Access to Amazon Nova models
- Basic understanding of function calling concepts
