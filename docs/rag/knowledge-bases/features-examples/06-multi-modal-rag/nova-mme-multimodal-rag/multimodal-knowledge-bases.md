---
tags:
    - RAG
    - Knowledge-Bases
    - Multimodal
    - Vision
---

!!! tip inline end "[Open in github](https://github.com/aws-samples/amazon-bedrock-samples/tree/main/rag/knowledge-bases/features-examples/06-multi-modal-rag/nova-mme-multimodal-rag/multimodal-knowledge-bases.ipynb){:target="_blank"}"

<h2>Amazon Bedrock Multimodal Knowledge Bases with S3 Vectors</h2>

This notebook provides sample code for building multimodal RAG applications using Amazon Bedrock Knowledge Bases with Amazon Nova Multimodal Embeddings and S3 Vectors.

**Overview**

Amazon Bedrock Knowledge Bases now supports multimodal retrieval, enabling you to search and retrieve information across text, images, audio, and video within a fully managed service. With multimodal retrieval, you can now:

- Ingest multiple content types: Process text, images, videos, and audio in a unified workflow
- Preserve visual context: Content is encoded using multimodal embeddings that maintain visual and audio characteristics
- Enable cross-modal search: Search using text to find videos, or upload an image to find visually similar content

**Amazon Nova Multimodal Embeddings**

This notebook uses Amazon Nova Multimodal Embeddings—the first unified embedding model that encodes text, documents, images, video, and audio into a single shared vector space. This enables powerful use cases like visual product search in e-commerce, finding similar scenes in video content, and matching products across different media types.

The notebook demonstrates:

1. Uploading a product catalog (images/videos) to S3
2. Creating an S3 Vector Store and Index
3. Creating a multimodal Knowledge Base with Nova embeddings
4. Creating and syncing the data source
5. Testing with text queries
6. Testing with image-based visual search
7. Understanding retrieval results
8. Cleanup

**Use Case: Visual Product Search**

Build a product catalog search system where customers can search using text descriptions, upload a photo to find similar products, or query using natural language about product features. The system retrieves visually similar items by comparing embedded representations across product images and videos.
