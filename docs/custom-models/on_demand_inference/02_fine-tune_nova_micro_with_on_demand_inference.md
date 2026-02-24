---
tags:
    - Fine-Tuning
    - Bedrock-SDK
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/custom-models/on_demand_inference/02_fine-tune_nova_micro_with_on_demand_inference.ipynb){:target="_blank"}"

# Fine-tune Nova Micro with On-Demand Inference

### Overview

This notebook demonstrates the complete fine-tuning and deployment process for Amazon Nova Micro using on-demand inference. You'll learn how to create, monitor, and deploy a fine-tuned model, then test it using multiple API methods.

### What You'll Learn

**Key Features:**
- Creates and monitors fine-tuning jobs for Nova Micro
- Visualizes training and validation loss curves
- Deploys the fine-tuned model for on-demand inference
- Tests the deployed model using multiple API methods

**Fine-tuning Configuration:**
- Base model: `amazon.nova-micro-v1:0:128k`
- Hyperparameters:
  - Epochs: 2
  - Batch size: 1
  - Learning rate: 0.00005
- Training time: ~60 minutes for 5K records

**API Testing Methods:**
1. **Converse API** - Synchronous conversation with complete response
2. **Converse Stream API** - Streaming response with progressive token delivery
3. **Invoke API** - Direct model invocation with custom parameters
4. **Invoke Stream API** - Streaming version of the Invoke API

**Prerequisites:**
- Completion of `01_setup_nova_micro.ipynb`
- Same kernel and instance as setup notebook
- Region: us-west-2 (required for Nova Micro fine-tuning)

### Use Cases

This tutorial is ideal for:
- **Text Summarization:** Fine-tuning models for domain-specific summarization tasks
- **Custom Model Development:** Learning the end-to-end process of model customization
- **API Integration:** Understanding different methods to interact with deployed models
- **Performance Evaluation:** Monitoring training metrics and model performance

### Important Notes

⚠️ **Cost Considerations:**
- Fine-tuning jobs incur charges based on training time and data volume
- On-demand inference deployments have associated costs
- Remember to clean up resources after testing

### Architecture

The workflow follows this pattern:
1. Data preparation and S3 storage
2. IAM role and policy creation
3. Fine-tuning job submission and monitoring
4. Model deployment with on-demand inference
5. API testing and validation
