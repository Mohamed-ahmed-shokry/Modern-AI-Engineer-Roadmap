# LLM & Agent Engineering Learning Path

Stages 0, 1, and 2 are preserved from the original roadmap. Follow the remaining core stages in order; optional resources are for targeted reinforcement or specialization.

## Stage 0 — Python Data and Classical NLP Foundations

1. [2026 Python Data Analysis & Visualization Masterclass](https://www.udemy.com/course/python-data-analysis-visualization/) (Colt Steele, Udemy) — Pandas, Matplotlib, Seaborn on text-heavy real datasets.
2. [NLP - Natural Language Processing with Python](https://www.udemy.com/course/nlp-natural-language-processing-with-python/) (Jose Portilla, Udemy) — Classical text processing: regex, NLTK, spaCy, POS/NER, text classification, topic modeling.

## Stage 1 — Transformer Concepts

1. [How Transformer LLMs Work](https://www.deeplearning.ai/courses/how-transformer-llms-work) — Explain the full forward pass: tokens → embeddings → attention → prediction, plus the KV cache.
2. 📖 [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) — The visual mental model of queries, keys, values, and multi-head attention.

## Stage 2 — Build an LLM from Scratch

1. [Attention in Transformers: Concepts and Code in PyTorch](https://www.deeplearning.ai/courses/attention-in-transformers-concepts-and-code-in-pytorch) — Write attention from a blank file in PyTorch, not just call the library.
2. [Let's Build GPT: From Scratch](https://www.youtube.com/watch?v=kCc8FmEb1nY) — Build and train a complete working GPT and know why each component exists.
3. [Let's Build the GPT Tokenizer](https://www.youtube.com/watch?v=zduSFxRajkE) — Implement BPE and understand why tokenization breaks spelling, numbers, and non-English text.

## Stage 3: Pretrained Models and Reliable LLM Applications

1. [Hugging Face LLM Course](https://huggingface.co/learn/llm-course/chapter1/1): focus on Chapters 1–7. Learn Transformers, Datasets, Tokenizers, pretrained-model inference, and basic fine-tuning. Skim concepts already covered in Stages 1–2.
2. [Pydantic for LLM Workflows](https://www.deeplearning.ai/courses/pydantic-for-llm-workflows): structured outputs, schemas, validation, and typed data flowing between application components.
3. 📖 [Your AI Product Needs Evals](https://hamel.dev/blog/posts/evals/): establish task-specific evaluation, trace inspection, and an iterative improvement process before adding complexity.

**Practice:** build a small extraction or classification API using a model SDK directly. Add validated outputs, prompt versioning, streaming where useful, timeouts, bounded retries, and a small evaluation dataset. Validate factual correctness separately from schema correctness.

## Stage 4: Retrieval and RAG

1. [Retrieval Augmented Generation (RAG)](https://www.coursera.org/learn/retrieval-augmented-generation-rag) (Zain Hasan): the main RAG course. Cover BM25, dense and hybrid search, metadata filtering, chunking, reranking, retrieval metrics, and end-to-end evaluation.
2. 📖 [Contextual Retrieval](https://www.anthropic.com/engineering/contextual-retrieval): understand how lost chunk context affects retrieval; test contextualization against your baseline.
3. **Optional:** [Vector Databases: From Embeddings to Applications](https://www.deeplearning.ai/courses/vector-databases-embeddings-applications): reinforce ANN/HNSW and vector-database concepts if the main course leaves gaps.

**Practice:** build a RAG service on your own dataset. Compare BM25, dense retrieval, hybrid retrieval, and reranking. Measure retrieval and answer quality separately. Include citations, unanswerable questions, document updates/deletion, and permission-aware retrieval.

## Stage 5: Agent Foundations and Context Engineering

1. [Agentic AI](https://www.deeplearning.ai/courses/agentic-ai): reflection, tool use, planning, multi-agent patterns, evaluation, and error analysis, starting from first principles in Python.
2. 📖 [Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents): decide when a fixed workflow, a single agent, or a more complex architecture is justified.
3. 📖 [Effective Context Engineering for AI Agents](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents): context selection, tool-result handling, compaction, and managing long-running tasks.

**Practice:** implement a tool-calling loop without an agent framework. Add explicit tool schemas, useful error messages, execution limits, and a deterministic workflow baseline. Compare task success, cost, and latency.

## Stage 6: LangGraph and Agent Evaluation

1. [Introduction to LangGraph](https://academy.langchain.com/courses/intro-to-langgraph): state, persistence, streaming, human feedback, subgraphs, memory, and deployment concepts.
2. [Building Reliable Agents with LangSmith](https://academy.langchain.com/courses/building-reliable-agents): tracing, evaluation datasets, experiments, code-based checks, LLM judges, and pairwise comparisons.
3. 📖 [Demystifying Evals for AI Agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents): evaluate agent behavior and outcomes across multi-step tasks.

**Practice:** rebuild your agent in LangGraph. Test interruptions, tool failures, recovery, and repeated execution. Assess tool arguments and final outcomes; calibrate model-based judges against human judgments.

## Stage 7: Long-Term Memory and MCP

1. [Long-Term Agentic Memory With LangGraph](https://www.deeplearning.ai/courses/long-term-agentic-memory-with-langgraph): semantic, episodic, and procedural memory using LangMem.
2. [Introduction to MCP](https://anthropic.skilljar.com/introduction-to-model-context-protocol): build MCP servers and clients and expose useful tools and resources.
3. **Optional deeper study:** [MCP: Advanced Topics](https://anthropic.skilljar.com/model-context-protocol-advanced-topics): advanced communication, transports, and deployment concepts. Check implementation details against the current specification.
4. 📖 [MCP Security Best Practices](https://modelcontextprotocol.io/docs/tutorials/security/security_best_practices): authorization, token handling, scope minimization, and integration risks.

**Practice:** expose a service through MCP with appropriate authentication and permissions. Keep conversation state separate from long-term memory. Implement memory update, deletion, and user isolation, then measure whether memory improves task performance.

## Stage 8: Production Engineering, Security, and Monitoring

1. [Made With ML: MLOps](https://madewithml.com/courses/mlops/): selected sections on testing, reproducibility, serving, CI/CD, monitoring, and data engineering. Skip foundations you already know.
2. [Monitoring Production Agents](https://academy.langchain.com/courses/production-monitoring): costs, product analytics, latency, errors, quality, and alerts.
3. [Red Teaming LLM Applications](https://www.deeplearning.ai/courses/red-teaming-llm-applications): systematic testing of LLM application vulnerabilities.
4. 📖 [OWASP LLM Top 10](https://genai.owasp.org/llm-top-10/): a reference for reviewing application risks and defenses.

**Practice:** deploy your application with FastAPI, Docker, a persistent database, and CI evaluation. Add authentication, secrets management, background jobs where needed, load testing, rollback, and trace redaction. Test prompt injection and enforce permissions in application code. Prevent duplicate side effects after retries.

## Stage 9: Practical Fine-Tuning and Post-Training

1. [Hugging Face LLM Course](https://huggingface.co/learn/llm-course/chapter1/1): return to Chapters 10–11 for dataset curation and practical LLM fine-tuning.
2. [Fine-Tuning & RL for LLMs: Intro to Post-Training](https://www.deeplearning.ai/courses/fine-tuning-and-reinforcement-learning-for-llms-intro-to-post-training): supervised fine-tuning and the foundations of reinforcement learning and alignment.
3. **Optional focused supplement:** [Post-training of LLMs](https://www.deeplearning.ai/courses/post-training-of-llms): concise practical coverage of SFT, DPO, and online RL.

**Practice:** fine-tune a small model with LoRA/QLoRA for a narrow task. Handle chat templates, loss masking, deduplication, and train/evaluation separation. Compare against prompting and RAG where appropriate. Report quality improvements, regressions, and training/serving costs.

## Stage 10: Inference Optimization and Serving

1. [Transformers in Practice](https://www.deeplearning.ai/courses/transformers-in-practice): focus on model behavior, GPU execution, and deployment-relevant internals; skim introductory overlap.
2. [Quantization Fundamentals with Hugging Face](https://www.deeplearning.ai/short-courses/quantization-fundamentals-with-hugging-face/): reduced precision, memory savings, and quality trade-offs.
3. [Fast & Efficient LLM Inference with vLLM](https://www.deeplearning.ai/courses/fast-and-efficient-llm-inference-with-vllm): optimize, serve, and benchmark an open-weight model.
4. 📖 [What We Learned from a Year of Building with LLMs](https://applied-llms.org/): production lessons on evaluation, reliability, and system design.

**Practice:** benchmark realistic prompt lengths and concurrent requests. Measure time to first token, inter-token latency, throughput, p50/p95 latency, GPU memory, and output quality. Understand prefill versus decode, batching, KV cache, and the differences between prefix caching and response caching.

## Stage 11: Multimodal AI and Document Intelligence

1. [Document AI: From OCR to Agentic Doc Extraction](https://www.deeplearning.ai/courses/document-ai-from-ocr-to-agentic-doc-extraction): extract structured information from PDFs, tables, charts, forms, and document layouts.
2. **Optional deeper study:** [Multi-vector Image Retrieval](https://www.deeplearning.ai/courses/multi-vector-image-retrieval): image-patch representations and fine-grained visual retrieval.

