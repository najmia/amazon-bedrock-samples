---
tags:
    - Fine-Tuning
    - Agents
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/custom-models/bedrock-reinforcement-fine-tuning/models/nova/nova_gsm8k_rft.ipynb){:target="_blank"}"

<h2>Reinforcement Fine-Tuning Amazon Nova 2.0 Lite with GSM8K</h2>

This notebook walks through training an Amazon Nova model using Reinforcement Fine-Tuning (RFT) on the GSM8K math dataset.

**What's RFT?**

Traditional fine-tuning shows a model examples and says "produce outputs like this." RFT takes a different approach: it lets the model generate its own responses, then uses a reward signal to reinforce good outputs and discourage bad ones. For math problems, this works particularly well because we can automatically verify if an answer is correct.

**What's GSM8K?**

GSM8K (Grade School Math 8K) is a dataset of ~8,000 grade-school math word problems. Each problem requires multi-step reasoning to solve. It's become a standard benchmark for testing whether language models can actually "think" through problems rather than just pattern-match.

The notebook covers:

- Prerequisites and SageMaker role permissions
- Installing dependencies
- Preprocessing the GSM8K dataset from HuggingFace into Bedrock RFT format
- Deploying a Lambda reward function that scores model responses
- Creating IAM roles for Lambda and Bedrock execution
- Testing the reward function
- Starting an RFT training job with customized hyperparameters
- Monitoring training progress

By the end, you'll have a Nova model that's better at step-by-step math reasoning.
