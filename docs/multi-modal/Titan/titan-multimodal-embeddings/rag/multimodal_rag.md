---
tags:
    - RAG
    - Multimodal
    - Embedding
    - Vision
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/multi-modal/Titan/titan-multimodal-embeddings/rag/1_multimodal_rag.ipynb){:target="_blank"}"

<h2>Multimodal RAG with Titan Embeddings</h2>

This notebook demonstrates building a multimodal RAG (Retrieval Augmented Generation) system using Amazon Titan Multimodal Embeddings and FAISS vector database.

**Use Case: Visual Product Search**

The notebook implements a product search system where customers can find products using:
- Text descriptions
- Images of products
- Combination of text and images

**Architecture**

1. Download product data from the Amazon Berkeley Objects dataset (images with metadata and tags)
2. Convert images to Base64 encoding
3. Generate embeddings for images and associated text using `amazon.titan-embed-image-v1` model
4. Store embeddings in FAISS in-memory vector database
5. For retrieval: Convert customer's text description and/or image into embeddings
6. Perform similarity search to find relevant products
7. Use Claude V2 to refine results by reasoning through matches and explaining why each result was accepted or rejected

**Key Features**

- Single `invoke_model` call to embed both image and text together
- Cross-modal search: text query finds images, image query finds similar products
- LLM-powered result refinement with explanations
- Integration with FAISS for efficient vector similarity search

**Note:** Run the `0_data_prep.ipynb` notebook first to prepare the dataset. In production, consider using persistent vector stores like Amazon OpenSearch Service Serverless or pgvector for PostgreSQL instead of in-memory FAISS.
