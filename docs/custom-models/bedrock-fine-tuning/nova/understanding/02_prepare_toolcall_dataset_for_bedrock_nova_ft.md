---
tags:
    - Agents
    - Fine-Tuning
    - Bedrock-SDK
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/custom-models/bedrock-fine-tuning/nova/understanding/nova_tooluse_customization/tooluse_finetuner_main/notebooks/02_prepare_toolcall_dataset_for_bedrock_nova_ft.ipynb){:target="_blank"}"

# Prepare Tool Call Dataset for Nova Fine-tuning

### Overview

This notebook guides you through converting your tool calling dataset to the format required by Amazon Nova for fine-tuning through Amazon Bedrock. Proper dataset formatting is crucial for successful fine-tuning of tool use capabilities.

### What You'll Learn

- Dataset format requirements for Nova fine-tuning
- How to convert tool calling data to Bedrock-compatible format
- Data validation and quality checks
- Best practices for preparing tool use training data

### Key Features

- Converts datasets to Amazon Bedrock Invoke API format
- Ensures compatibility with Amazon Bedrock Console
- Validates data structure and content
- Prepares both training and test datasets

### Prerequisites

- Completion of notebook 01 (understanding tool calling basics)
- Raw tool calling dataset
- Understanding of JSON/JSONL formats
