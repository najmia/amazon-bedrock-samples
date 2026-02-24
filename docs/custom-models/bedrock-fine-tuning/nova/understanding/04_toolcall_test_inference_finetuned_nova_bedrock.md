---
tags:
    - Agents
    - Fine-Tuning
    - Bedrock-SDK
    - Evaluation
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/custom-models/bedrock-fine-tuning/nova/understanding/nova_tooluse_customization/tooluse_finetuner_main/notebooks/04_toolcall_test_inference_finetuned_nova_bedrock.ipynb){:target="_blank"}"

# Test Inference with Fine-tuned Nova Model

### Overview

This notebook shows you how to deploy your fine-tuned Nova model using provisioned throughput and run inference to test its tool calling capabilities. You'll also learn how to calculate accuracy metrics to evaluate the model's performance.

### What You'll Learn

- How to deploy a fine-tuned model with provisioned throughput
- Running inference with the fine-tuned model
- Calculating accuracy metrics for tool usage
- Evaluating argument calling accuracy
- Comparing fine-tuned vs base model performance

### Key Features

- **Model Deployment:** Set up provisioned throughput for your fine-tuned model
- **Inference Testing:** Run tool calling tests with various scenarios
- **Metrics Calculation:** Measure accuracy on validation set for:
  - Tool usage accuracy (correct tool selection)
  - Arguments calling accuracy (correct parameter extraction)
- **Performance Analysis:** Compare improvements from fine-tuning

### Evaluation Metrics

The notebook calculates two key metrics:
1. **Tool Usage Accuracy:** How often the model selects the correct tool
2. **Arguments Accuracy:** How accurately the model extracts and formats tool parameters

### Prerequisites

- Completion of notebook 03 (fine-tuning job)
- Successfully completed fine-tuning job
- Validation dataset for testing
- Understanding of provisioned throughput concepts
