---
tags:
    - Agents
    - Fine-Tuning
    - Bedrock-SDK
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/custom-models/bedrock-fine-tuning/nova/understanding/nova_tooluse_customization/tooluse_finetuner_main/notebooks/03_toolcall_fullfinetune_nova_bedrock.ipynb){:target="_blank"}"

# Full Fine-tuning Nova for Tool Use

### Overview

This notebook demonstrates how to set up and execute a complete fine-tuning job for Amazon Nova models to improve tool calling capabilities. You'll learn how to configure IAM roles, prepare S3 storage, and launch fine-tuning jobs using the Bedrock API.

### What You'll Learn

- Setting up IAM roles with proper permissions for fine-tuning
- Configuring S3 buckets for training and test datasets
- Creating and starting a fine-tuning job with Amazon Nova
- Monitoring fine-tuning job progress
- Best practices for tool use fine-tuning

### Key Features

- IAM role and policy setup for Bedrock customization
- S3 bucket configuration for dataset storage
- Fine-tuning job creation via Bedrock API
- Job monitoring and status tracking

### Important Notes

⚠️ **Alternative Method:**
Fine-tuning can also be done directly from the Amazon Bedrock Console as an alternative to using the API.

### Prerequisites

- Completion of notebook 02 (dataset preparation)
- Formatted training and test datasets in S3
- AWS account with appropriate IAM permissions
- Understanding of Amazon Bedrock fine-tuning concepts
