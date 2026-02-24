---
tags:
    - Embedding
    - Bedrock-SDK
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/multi-modal/Titan/embeddings/v2/Titan-V2-Embeddings.ipynb){:target="_blank"}"

<h2>Benchmark Titan Text Embeddings V2</h2>

This notebook demonstrates how to benchmark Amazon Titan Text Embeddings V2, a state-of-the-art embeddings model on Amazon Bedrock using the MTEB (Massive Text Embedding Benchmark) dataset.

**About Titan Text Embeddings V2**

Amazon Titan Text Embeddings V2 is a multilingual text embeddings model that converts text inputs like single words, phrases, or large documents into high-dimensional numerical vector representations. Key features include:

- Support for over 100 languages (compared to 25 in V1)
- Flexible output dimensions: 256, 512, and 1024 (compared to fixed 1,536 in V1)
- Input support up to 8,192 tokens
- Cost savings through reduced embedding size
- Optimized for multi-lingual data and use cases

**Use Cases**

Embeddings are integral to various natural language processing applications:

- Knowledge bases for efficient similarity search and retrieval
- Retrieval Augmented Generation (RAG) for context-aware responses
- Personalization and recommendation systems
- Semantic search applications

The notebook covers:

- Understanding how text is converted into vectors using Transformer-based models
- Setting up the Bedrock client
- Benchmarking with MTEB datasets
- Comparing performance across different output dimensions
- Integration with vector databases like FAISS

This flexible output embedding model allows organizations to balance performance and cost by choosing the appropriate dimension size for their use case.
