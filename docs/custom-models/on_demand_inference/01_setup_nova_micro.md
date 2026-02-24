---
tags:
    - Fine-Tuning
    - Bedrock-SDK
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/custom-models/on_demand_inference/01_setup_nova_micro.ipynb){:target="_blank"}"

# Setup Nova Micro for On-Demand Inference

### Overview

This notebook handles the initial setup required for fine-tuning Amazon Nova Micro with on-demand inference capabilities. It provides an end-to-end workflow for preparing your AWS environment and datasets.

### What You'll Learn

**Key Features:**
- Creates necessary IAM roles and policies for Bedrock customization jobs
- Sets up an S3 bucket for storing training data and model outputs
- Prepares the CNN news article dataset for fine-tuning
- Converts data to the required `bedrock-conversation-2024` schema format
- Uploads processed datasets to S3

**Dataset:**
- Uses the CNN/DailyMail dataset from Hugging Face
- Converts articles and highlights into a summarization task format
- Limits training data to 5,000 samples and validation to 999 samples (within Nova Micro limits)
- Filters data points by length (max 3,000 characters)

**Prerequisites:**
- AWS account with appropriate permissions (IAM, S3, Bedrock)
- SageMaker Studio or Jupyter environment
- Recommended kernel: Data Science 3.0, Python 3, ml.t3.medium

### Getting Started

```bash
pip install boto3 datasets jsonlines pandas matplotlib fmeval awscurl
```

### Important Notes

⚠️ **Regional Requirements:**
- Nova Micro fine-tuning is only available in us-east-1 region
- Ensure your AWS resources are in the correct region

⚠️ **Data Limits:**
- Training dataset: Maximum 20,000 records
- Validation dataset: Maximum 1,000 records
- Individual data points: Recommended max 3,000 characters
