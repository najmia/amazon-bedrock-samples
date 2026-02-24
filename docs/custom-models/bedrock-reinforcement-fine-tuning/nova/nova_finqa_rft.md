---
tags:
    - Fine-Tuning
    - Agents
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/custom-models/bedrock-reinforcement-fine-tuning/models/nova/nova_finqa_rft.ipynb){:target="_blank"}"

<h2>Reinforcement Fine-Tuning Amazon Nova 2.0 Lite with FinQA</h2>

This notebook walks through training an Amazon Nova model using Reinforcement Fine-Tuning (RFT) on the FinQA dataset for financial reasoning tasks.

**What's RFT?**

Traditional fine-tuning shows a model examples and says "produce outputs like this." RFT takes a different approach: it lets the model generate its own responses, then uses a reward signal to reinforce good outputs and discourage bad ones. For math problems, this works particularly well because we can automatically verify if an answer is correct.

**What's FinQA?**

FinQA is a dataset of 8,281 question-answer pairs derived from 2,789 earnings reports of S&P 500 companies. Each example contains textual context, structured data tables, and multi-step reasoning questions requiring numerical calculations across both text and tables.

The notebook covers:

- Prerequisites and SageMaker role permissions
- Installing dependencies
- Preprocessing the FinQA dataset into Bedrock RFT format
- Deploying a Lambda reward function that scores model responses
- Creating IAM roles for Lambda and Bedrock execution
- Testing the reward function
- Starting an RFT training job with customized hyperparameters
- Monitoring training progress

By the end, you'll have a Nova model that's better at step-by-step financial reasoning and multi-step calculations.
