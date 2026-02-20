# Amazon Bedrock Cookbook

A collection of recipes, guides, and examples to help you build with Amazon Bedrock.

> 💡 **New to Bedrock?** Start with our [Quickstarts](#quickstarts) to get running in 15 minutes.

## 🔍 Searchable Interface

**[Open Interactive Search →](./cookbook-search.html)** - Search through 120+ recipes with filters and free-text search

Or browse by category below:

---

## 📑 Table of Contents

- [Quickstarts](#quickstarts) - Get started in 15 minutes
- [Core Capabilities](#core-capabilities) - Feature-by-feature guides
- [Integrations](#integrations) - Third-party tools and frameworks
- [Use Case Recipes](#use-case-recipes) - Complete solutions
- [Advanced Techniques](#advanced-techniques) - Optimization and patterns
- [Responsible AI & Safety](#responsible-ai--safety) - Guardrails and security
- [Evaluation & Observability](#evaluation--observability) - Testing and monitoring
- [Production Patterns](#production-patterns) - POC to production
- [Workshops](#workshops) - Hands-on learning paths

---

## Quickstarts

Get up and running with Amazon Bedrock in minutes.

### Basic APIs
- [Bedrock Invoke API](./introduction-to-bedrock/bedrock_apis/) - Make your first API call
- [Converse API](./introduction-to-bedrock/converse_api/) - Multi-turn conversations
- [Streaming Responses](./introduction-to-bedrock/converse_api/) - Real-time response streaming

### Essential Features
- [Embeddings with Titan](./embeddings/) - Generate text embeddings
- [Prompt Caching](./introduction-to-bedrock/prompt-caching/) - Reduce costs with caching
- [Structured Outputs](./introduction-to-bedrock/structured-outputs/) - JSON mode for structured data
- [Batch Processing](./introduction-to-bedrock/batch_api/) - Large-scale batch inference

### Getting Started Guides
- [Authentication & Setup](./introduction-to-bedrock/) - Configure AWS credentials and IAM
- [Model Selection Guide](./introduction-to-bedrock/) - Choose the right model for your use case
- [Cross-Region Inference](./introduction-to-bedrock/cross-region/) - Multi-region deployment

---

## Core Capabilities

Deep dive into specific Bedrock features.

### 🤖 Agents & Function Calling

**Getting Started:**
- [Introduction to Agents](./agents-and-function-calling/introduction-to-agents/) - Build your first agent
- [Function Calling Basics](./agents-and-function-calling/function-calling/) - Native function calling with Converse API

**Bedrock Agents Features:**
- [Create Agent with Function Definition](./agents-and-function-calling/bedrock-agents/features-examples/01-create-agent-with-function-definition/) - Define custom functions
- [Create Agent with API Schema](./agents-and-function-calling/bedrock-agents/features-examples/02-create-agent-with-api-schema/) - Use OpenAPI specs
- [Return of Control](./agents-and-function-calling/bedrock-agents/features-examples/03-create-agent-with-return-of-control/) - Human-in-the-loop patterns
- [Agent with Knowledge Base](./agents-and-function-calling/bedrock-agents/features-examples/04-create-agent-with-single-knowledge-base/) - RAG-enabled agents
- [Knowledge Base + Action Groups](./agents-and-function-calling/bedrock-agents/features-examples/05-create-agent-with-knowledge-base-and-action-group/) - Combined capabilities
- [Prompt & Session Attributes](./agents-and-function-calling/bedrock-agents/features-examples/06-prompt-and-session-attributes/) - Context management
- [Advanced Prompts & Parsers](./agents-and-function-calling/bedrock-agents/features-examples/07-advanced-prompts-and-custom-parsers/) - Custom orchestration
- [Agent with Guardrails](./agents-and-function-calling/bedrock-agents/features-examples/08-create-agent-with-guardrails/) - Safety controls
- [Agent with Memory](./agents-and-function-calling/bedrock-agents/features-examples/09-create-agent-with-memory/) - Persistent memory
- [Code Interpreter Agent](./agents-and-function-calling/bedrock-agents/features-examples/10-create-agent-with-code-interpreter/) - Execute code dynamically
- [User Confirmation](./agents-and-function-calling/bedrock-agents/features-examples/11-create-agents-with-action-user-confirmation/) - Approval workflows
- [Non-Optimized Models](./agents-and-function-calling/bedrock-agents/features-examples/12-models-not-yet-optimized-for-bedrock-agents/) - Use any model
- [CDK Deployment](./agents-and-function-calling/bedrock-agents/features-examples/13-create-agent-using-CDK/) - Infrastructure as code
- [Custom Orchestration](./agents-and-function-calling/bedrock-agents/features-examples/14-create-agent-with-custom-orchestration/) - Advanced control
- [Inline Agents](./agents-and-function-calling/bedrock-agents/features-examples/15-invoke-inline-agents/) - Stateless agents

**Agent Blueprints:**
- [CDK Agent Templates](./agents-and-function-calling/bedrock-agents/agent-blueprint-templates/) - Reusable agent infrastructure

**Testing:**
- [Agent Testing Framework](./agents-and-function-calling/bedrock-agents/test-agent/) - Test agents with synthetic data

**Advanced Patterns:**
- [Agentic Guardrails](./agents-and-function-calling/agentic-guardrails/) - Multi-framework guardrails (CrewAI, LangGraph, Strands)
- [Code Interpreter](./agents-and-function-calling/agent-code-interpreter/) - Data analysis agents
- [Bedrock Flows](./agents-and-function-calling/bedrock-flows/) - Prompt management flows
- [Model Context Protocol (MCP)](./agents-and-function-calling/mcp/) - MCP integration

### 📚 RAG (Retrieval Augmented Generation)

**Bedrock Knowledge Bases:**
- [Zero-Setup Chat](./rag/knowledge-bases/) - Quick start with Knowledge Bases
- [RAG Concepts](./rag/knowledge-bases/features-examples/) - Understanding RAG fundamentals
- [Evaluation & Optimization](./rag/knowledge-bases/features-examples/) - Improve RAG performance
- [Multi-Modal RAG](./rag/knowledge-bases/features-examples/) - Images + text retrieval
- [Structured RAG](./rag/knowledge-bases/features-examples/) - Structured data retrieval
- [Graph RAG](./rag/knowledge-bases/features-examples/) - Knowledge graph integration
- [Managed Index](./rag/knowledge-bases/features-examples/) - Vector index management
- [S3 Vectors](./rag/knowledge-bases/features-examples/) - Custom vector storage

**Open-Source RAG:**
- [LangChain RAG](./rag/open-source/) - RAG with LangChain
- [LlamaIndex RAG](./rag/open-source/) - RAG with LlamaIndex
- [Chunking Strategies](./rag/open-source/) - Document chunking techniques
- [Reranking](./rag/open-source/) - Improve retrieval with reranking
- [Vector Stores](./rag/open-source/) - Pinecone, Chroma, Weaviate, etc.

**Advanced RAG:**
- [Prompt Flow + Knowledge Bases](./rag/bedrock-prompt-flow-kb-rag-app/) - Visual RAG workflows

### 🎨 Multimodal

**Vision (Claude 3):**
- [Getting Started with Vision](./multi-modal/Claude3/) - Image understanding basics
- [Best Practices for Vision](./multi-modal/Claude3/) - Optimize vision prompts
- [Multimodal RAG](./multi-modal/Claude3/) - RAG with images

**Image Generation (Titan):**
- [Image Generation Basics](./multi-modal/Titan%20Image%20Generator/) - Generate images
- [Background Removal](./multi-modal/Titan%20Image%20Generator/) - Remove backgrounds
- [Color Conditioning](./multi-modal/Titan%20Image%20Generator/) - Control colors
- [Image Conditioning](./multi-modal/Titan%20Image%20Generator/) - Image-to-image generation
- [Instant Customization](./multi-modal/Titan%20Image%20Generator/) - Style transfer

**Multimodal Models:**
- [Nova Multimodal](./multi-modal/Nova/) - Nova model examples
- [Titan Embeddings](./multi-modal/Titan/) - Multimodal embeddings
- [Video Embeddings](./multi-modal/TwelveLabs/) - Video search with TwelveLabs

### 🎯 Custom Models

**Fine-Tuning:**
- [Claude Haiku Fine-Tuning](./custom-models/bedrock-fine-tuning/) - Fine-tune Claude
- [Meta Llama Fine-Tuning](./custom-models/bedrock-fine-tuning/) - Fine-tune Llama
- [Nova Fine-Tuning](./custom-models/bedrock-fine-tuning/) - Fine-tune Nova
- [Titan Fine-Tuning](./custom-models/bedrock-fine-tuning/) - Fine-tune Titan
- [Dataset Validation](./custom-models/bedrock-fine-tuning/) - Validate training data

**Advanced Techniques:**
- [Reinforcement Fine-Tuning (RLHF)](./custom-models/bedrock-reinforcement-fine-tuning/) - RLHF with reward functions
- [Model Distillation](./custom-models/model_distillation/) - Knowledge distillation
- [On-Demand Inference](./custom-models/on_demand_inference/) - Nova Micro setup

**Model Import:**
- [Import Llama Models](./custom-models/import_models/) - Import Llama 2/3
- [Import Mistral](./custom-models/import_models/) - Import Mistral models
- [Import Flan-T5](./custom-models/import_models/) - Import Flan-T5
- [Import Qwen](./custom-models/import_models/) - Import Qwen models
- [Import DeepSeek](./custom-models/import_models/) - Import DeepSeek

### 📝 Text Generation

**Common Use Cases:**
- [Code Generation](./genai-use-cases/text-generation/) - Generate code
- [Entity Extraction](./genai-use-cases/text-generation/) - Extract structured data
- [Text Summarization](./genai-use-cases/text-generation/) - Summarize documents
- [Translation](./genai-use-cases/text-generation/) - Multi-language translation
- [Batch Processing](./genai-use-cases/text-generation/) - Large-scale text processing

**Specialized:**
- [AWS Glue Metadata Generation](./genai-use-cases/aws-glue-metadata-generation/) - Auto-generate data catalog metadata

---

## Integrations

Connect Bedrock with your existing tools and frameworks.

### 🔗 Open-Source Frameworks

**Agent Frameworks:**
- [LangChain Agents](./agents-and-function-calling/open-source-agents/) - Build agents with LangChain
- [LangGraph Multi-Agent](./agents-and-function-calling/open-source-agents/) - Multi-agent orchestration
- [CrewAI Agent Teams](./agents-and-function-calling/open-source-agents/) - Collaborative agents
- [LlamaIndex Agents](./agents-and-function-calling/open-source-agents/) - Data-focused agents

**Model Context Protocol:**
- [MCP Integration](./agents-and-function-calling/mcp/) - Connect with MCP servers

### 🗄️ Vector Databases

Available in [RAG Open-Source Examples](./rag/open-source/):
- Pinecone
- Chroma
- Weaviate
- Redis
- OpenSearch
- PostgreSQL (pgvector)
- And more...

### 📊 Observability & Monitoring

- [Langfuse on ECS Fargate](./evaluation-observe/deploy-langfuse-on-ecs-fargate-with-typescript-cdk/) - Deploy Langfuse for observability
- [OpenTelemetry Instrumentation](./evaluation-observe/open-telemetry-instrumentation/) - Distributed tracing
- [Custom Observability Solution](./evaluation-observe/Custom-Observability-Solution/) - Build custom monitoring (Python/JavaScript)

---

## Use Case Recipes

Complete, production-ready solutions for common scenarios.

### 🛍️ Retail & E-Commerce
- [Retail Agent](./agents-and-function-calling/bedrock-agents/use-case-examples/agentsforbedrock-retailagent/) - Product recommendations, inventory management

### 👥 Human Resources
- [HR Assistant](./agents-and-function-calling/bedrock-agents/use-case-examples/hr-assistant/) - Employee onboarding, policy Q&A

### 💼 Customer Relationship Management
- [CRM Agent](./agents-and-function-calling/bedrock-agents/use-case-examples/customer-relationship-management-agent/) - Customer data management, interaction tracking

### 🏥 Insurance
- [Insurance Claim Automation](./agents-and-function-calling/bedrock-agents/use-case-examples/insurance-claim-lifecycle-automation/) - Claim processing, document extraction

### 💾 Data & Analytics
- [Text-to-SQL Agent](./agents-and-function-calling/bedrock-agents/use-case-examples/text-2-sql-agent/) - Natural language database queries
- [Text-to-SQL (CDK Enhanced)](./agents-and-function-calling/bedrock-agents/use-case-examples/text-2-sql-agent-cdk-enhanced/) - Production-ready SQL agent

### 🎯 Marketing
- [Marketing Agent](./agents-and-function-calling/bedrock-agents/use-case-examples/marketing-agent/) - Campaign creation, content generation

### 💰 Finance
- [Investment Research Assistant](./agents-and-function-calling/bedrock-agents/use-case-examples/ai-powered-assistant-for-investment-research/) - Financial analysis, report generation
- [AWS Cost Explorer Agent](./agents-and-function-calling/bedrock-agents/use-case-examples/cost-explorer-agent/) - Cost analysis and optimization

### 🎫 Customer Support
- [Product Review Agent](./agents-and-function-calling/bedrock-agents/use-case-examples/product-review-agent/) - Sentiment analysis, review summarization
- [Event-Driven Ticket Resolution](./agents-and-function-calling/bedrock-agents/use-case-examples/event-driven-ticket-resolution/) - Automated support workflows

### 🔐 Security & Access Control
- [Fine-Grained Access Permissions](./agents-and-function-calling/bedrock-agents/use-case-examples/fine-grained-access-permissions-agent/) - Permission-based agent responses

### 📄 Document Processing
- [Data Automation & BDA](./data-automation-bda/) - Document, image, video, and audio processing workflows

---

## Advanced Techniques

Optimization and sophisticated patterns for experienced developers.

### 🎨 Prompt Engineering
- [Prompt Engineering Guide](./articles-guides/prompt-engineering/) - Best practices and techniques
- [Prompt Decomposition](./articles-guides/prompt-engineering/) - Break down complex prompts
- [Prompt Evaluation](./articles-guides/prompt-engineering/) - Measure prompt effectiveness
- [Prompt Management Flows](./articles-guides/prompt-engineering/) - Advanced prompt workflows

### ⚡ Performance Optimization
- [Model Latency Benchmarking](./model-latency-benchmarking/) - Measure TTFT and tokens/sec
- [Prompt Caching Strategies](./introduction-to-bedrock/prompt-caching/) - Reduce latency and costs
- [Cross-Region Inference](./introduction-to-bedrock/cross-region/) - Failover and load balancing
- [Batch Processing](./introduction-to-bedrock/batch_api/) - Large-scale inference

### 🤝 Multi-Agent Systems
- [Agentic Guardrails with CrewAI](./agents-and-function-calling/agentic-guardrails/) - CrewAI patterns
- [Agentic Guardrails with LangGraph](./agents-and-function-calling/agentic-guardrails/) - LangGraph patterns
- [Agentic Guardrails with Strands](./agents-and-function-calling/agentic-guardrails/) - Strands patterns

### 💰 Cost Optimization
- [Inference Profiles](./poc-to-prod/inference-profiles/) - Configure inference profiles
- [Cost Tracing Dashboard](./poc-to-prod/inference-profiles/) - Monitor costs with Streamlit
- [Prompt Caching](./introduction-to-bedrock/prompt-caching/) - Cache for cost savings

### 🔄 Migration & Evaluation
- [360 Model Evaluation](./migrations/360-eval/) - Comprehensive model profiling and comparison

---

## Responsible AI & Safety

Enterprise-grade safety, compliance, and ethical AI practices.

### 🛡️ Guardrails

**Bedrock Guardrails:**
- [Guardrails API Basics](./responsible_ai/bedrock-guardrails/) - Content filtering and PII redaction
- [Streaming with Guardrails](./responsible_ai/bedrock-guardrails/) - Real-time content filtering
- [LangChain Integration](./responsible_ai/bedrock-guardrails/) - Use guardrails with LangChain
- [Marketplace Integration](./responsible_ai/bedrock-guardrails/) - Third-party guardrails

**Development Approaches:**
- [Test-Driven Guardrails](./responsible_ai/tdd-guardrail/) - TDD approach for guardrails
- [Kiro Code Modality Guardrail](./responsible_ai/kiro-code-modality-guardrail-hook/) - Code safety guardrails

### 🤖 Automated Reasoning

- [Automated Reasoning Checks](./responsible_ai/bedrock-automated-reasoning-checks/) - Policy validation with automated reasoning
- [Response Rewriting](./responsible_ai/bedrock-automated-reasoning-checks/) - Rewrite responses for compliance
- [Test Creation](./responsible_ai/bedrock-automated-reasoning-checks/) - Generate compliance tests
- [Lounge Access Agent Demo](./responsible_ai/bedrock-automated-reasoning-checks/) - Complete example

**Full-Stack Example:**
- [Automated Reasoning Chatbot](./responsible_ai/automated-reasoning-rewriting-chatbot/) - Flask backend + React frontend

### 🔒 Security

- [Securing RAG Applications](./security/securing-rag-apps/) - Security best practices for RAG

---

## Evaluation & Observability

Testing, monitoring, and continuous improvement of your AI applications.

### 📊 Evaluation

**RAG Evaluation:**
- [RAG Evaluation with Synthetic Data](./evaluation-observe/bedrock-rag-evaluation/) - Generate and evaluate with synthetic data
- [Custom Metrics for RAG](./evaluation-observe/bedrock-eval-custom-metrics/) - Domain-specific evaluation

**Model Evaluation:**
- [LLM-as-Judge](./evaluation-observe/bedrock-llm-as-judge-evaluation/) - Use LLMs to evaluate outputs
- [Custom Metrics](./evaluation-observe/bedrock-eval-custom-metrics/) - Build custom evaluation metrics
- [Bring Your Own Inference](./evaluation-observe/bedrock-eval-bring-your-own-inference/) - BYOI evaluation

**Agent Evaluation:**
- [Agent Testing Framework](./agents-and-function-calling/bedrock-agents/test-agent/) - Test agents systematically
- [Synthetic Data Generation](./agents-and-function-calling/bedrock-agents/test-agent/) - Generate test cases
- [LLM Judge for Agents](./agents-and-function-calling/bedrock-agents/test-agent/) - Evaluate agent performance

### 🔍 Observability

**Monitoring Solutions:**
- [Agent Observability](./evaluation-observe/agent-observability/) - Monitor agent behavior
- [Custom Observability (Python/JS)](./evaluation-observe/Custom-Observability-Solution/) - Build custom monitoring
- [OpenTelemetry Integration](./evaluation-observe/open-telemetry-instrumentation/) - Distributed tracing

**Observability Platforms:**
- [Langfuse on ECS Fargate](./evaluation-observe/deploy-langfuse-on-ecs-fargate-with-typescript-cdk/) - Deploy Langfuse with CDK

---

## Production Patterns

Take your POCs to production-ready systems.

### 🏗️ Infrastructure

**Batch Processing:**
- [Bedrock Batch Orchestrator](./poc-to-prod/bedrock-batch-orchestrator/) - CDK stack with Step Functions and EventBridge

**Inference Management:**
- [Inference Profiles](./poc-to-prod/inference-profiles/) - Configure and manage inference profiles
- [Cost Tracing Dashboard](./poc-to-prod/inference-profiles/) - Streamlit dashboard for cost monitoring

### 💰 Cost Management

- [Cost Reporting with Converse API](./cost-reporting/converse-metadata-cost-reporting/) - Track costs using metadata
- [CDK Infrastructure](./cost-reporting/converse-metadata-cost-reporting/) - Deploy cost reporting infrastructure

### 🔄 Best Practices

- [Prompt Caching](./introduction-to-bedrock/prompt-caching/) - Reduce costs and latency
- [Batch API](./introduction-to-bedrock/batch_api/) - Process large volumes efficiently
- [Cross-Region Inference](./introduction-to-bedrock/cross-region/) - High availability patterns

---

## Workshops

Hands-on, structured learning experiences.

### 🎓 Beginner Workshop (L200)
[Open-Source Workshop - Beginner](./workshops/open-source-l200/)
- Contextual text generation
- Retrieval-based applications
- Introduction to agents
- Sample datasets and utilities included

### 🚀 Advanced Workshop (L400)
[Open-Source Workshop - Advanced](./workshops/open-source-l400/)
- Travel planner with LangGraph
- Multi-agent systems
- CrewAI collaborative agents
- Agent evaluation techniques

### 📊 Multimodal Workshop
[Data Automation & BDA Workshops](./data-automation-bda/workshops/)
- Document processing
- Image analysis
- Video understanding
- Audio transcription
- Multimodal RAG

---

## Additional Resources

### 📖 Documentation
- [Amazon Bedrock Documentation](https://docs.aws.amazon.com/bedrock/)
- [Bedrock API Reference](https://docs.aws.amazon.com/bedrock/latest/APIReference/)
- [Bedrock User Guide](https://docs.aws.amazon.com/bedrock/latest/userguide/)

### 🌐 Community
- [AWS re:Post for Bedrock](https://repost.aws/tags/bedrock)
- [GitHub Issues](https://github.com/aws-samples/amazon-bedrock-samples/issues)
- [Contributing Guide](./CONTRIBUTING.md)

### 🎯 Getting Help
- Review the [README](./README.md) for setup instructions
- Check [existing issues](https://github.com/aws-samples/amazon-bedrock-samples/issues) for common problems
- Open a new issue for bugs or feature requests

---

## Recipe Index by Tag

### By Difficulty
- 🟢 **Beginner:** Quickstarts, Basic APIs, Simple use cases
- 🟡 **Intermediate:** RAG, Agents, Multimodal, Fine-tuning
- 🔴 **Advanced:** Multi-agent systems, Custom orchestration, Production patterns

### By Category
- **#agents** - Agent-related recipes
- **#rag** - Retrieval augmented generation
- **#multimodal** - Vision, image, video, audio
- **#evaluation** - Testing and evaluation
- **#production** - Production-ready patterns
- **#security** - Safety and compliance
- **#cost-optimization** - Cost reduction techniques
- **#integration** - Third-party integrations

### By Model
- **Claude** - Anthropic Claude models
- **Titan** - Amazon Titan models
- **Llama** - Meta Llama models
- **Nova** - Amazon Nova models
- **Mistral** - Mistral AI models

---

## Contributing

We welcome contributions! See our [Contributing Guide](./CONTRIBUTING.md) for details on:
- Adding new recipes
- Improving existing examples
- Reporting issues
- Suggesting new use cases

---

## License

This library is licensed under the MIT-0 License. See the [LICENSE](./LICENSE) file.

---

**Last Updated:** February 2026  
**Total Recipes:** 120+  
**Repository:** [amazon-bedrock-samples](https://github.com/aws-samples/amazon-bedrock-samples)
