# LLM & Agent Engineering Learning Path

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

## Stage 3 — Retrieval and RAG

1. [Retrieval Augmented Generation (RAG)](https://www.coursera.org/learn/retrieval-augmented-generation-rag) — Build a full RAG pipeline and justify every design decision in it.
2. 📖 [Contextual Retrieval](https://www.anthropic.com/news/contextual-retrieval) — Why chunks lose meaning and one concrete fix to apply in your project.
3. [Vector Databases: From Embeddings to Applications](https://www.deeplearning.ai/courses/vector-databases-embeddings-applications) — How ANN/HNSW indexing works, so you can defend "why this DB" with engineering reasons.

## Stage 4 — Agent Foundations

1. [Agentic AI](https://www.deeplearning.ai/courses/agentic-ai) — The four agent patterns (reflection, tool use, planning, multi-agent) in plain Python, no framework.
2. 📖 [Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) — When a workflow beats an agent; the judgment call interviews test.
3. [Functions, Tools and Agents with LangChain](https://www.deeplearning.ai/courses/functions-tools-agents-langchain) — Function calling and LCEL, the mechanism under every agent framework.

## Stage 5 — LangGraph and Multi-Agent Systems

1. [AI Agents in LangGraph](https://www.deeplearning.ai/courses/ai-agents-in-langgraph) — Build an agent loop by hand, then rebuild it in LangGraph with state and persistence.
2. [LangChain Academy](https://academy.langchain.com/) — Production-level LangGraph fluency: state, memory, streaming, deployment.
3. [Design, Develop, and Deploy Multi-Agent Systems with CrewAI](https://www.deeplearning.ai/courses/design-develop-and-deploy-multi-agent-systems-with-crewai) — The role-based multi-agent paradigm, a second mental model beyond graphs.
4. 📖 [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) — Planning, memory, and tool use organized into one framework.

## Stage 6 — Memory and MCP

1. [Long-Term Agentic Memory With LangGraph](https://www.deeplearning.ai/courses/long-term-agentic-memory-with-langgraph) — Semantic, episodic, and procedural memory with LangMem; agents that remember across sessions.
2. [Introduction to MCP](https://anthropic.skilljar.com/introduction-to-model-context-protocol) + [MCP: Advanced Topics](https://anthropic.skilljar.com/model-context-protocol-advanced-topics) — Build MCP servers/clients from scratch, then sampling and transports.

## Stage 7 — Evaluation

1. [Generative AI with Large Language Models](https://www.coursera.org/learn/generative-ai-with-llms) — The full LLM lifecycle: pretraining, PEFT/LoRA, RLHF concepts, scaling laws.
2. [Building and Evaluating Advanced RAG](https://www.deeplearning.ai/short-courses/building-evaluating-advanced-rag/) — Measure RAG with the triad: context relevance, groundedness, answer relevance.
3. LangSmith, via [LangChain Academy](https://academy.langchain.com/collections) — Tracing, regression testing, and live scoring for agent pipelines.
4. 📖 "Your AI Product Needs Evals" (Hamel Husain) — Evals as an ongoing process, not a one-time metric.

## Stage 8 — Inference Optimization and Production

1. [Quantization Fundamentals with Hugging Face](https://www.deeplearning.ai/short-courses/quantization-fundamentals-with-hugging-face/) — Shrink models to fit smaller GPUs and know the accuracy cost. (Optional deeper: [Quantization in Depth](https://www.deeplearning.ai/courses/quantization-in-depth).)
2. [Fast & Efficient LLM Inference with vLLM](https://www.deeplearning.ai/courses/fast-and-efficient-llm-inference-with-vllm) — Compress, serve, and benchmark a model; vLLM is named in Cairo postings.
3. [Semantic Caching for AI Agents](https://www.deeplearning.ai/courses/semantic-caching-for-ai-agents) — Two-layer caching that cuts agent cost/latency, wired into LangGraph.
4. 📖 [What We Learned from a Year of Building with LLMs](https://applied-llms.org/) — Practitioner lessons so you spot production pitfalls before hitting them.

## Stage 9 — Internals and Post-Training

1. [Transformers in Practice](https://www.deeplearning.ai/courses/transformers-in-practice) — Connect model behavior to the math to GPU execution; debug by reasoning about internals.
2. 📖 [Illustrating RLHF](https://huggingface.co/blog/rlhf) — The visual map of the RLHF pipeline before going deep.
3. [Fine-Tuning & RL for LLMs: Intro to Post-Training](https://www.deeplearning.ai/courses/fine-tuning-and-reinforcement-learning-for-llms-intro-to-post-training) — SFT, RLHF, and DPO hands-on; shape a base model's behavior.
4. Optional: [Reinforcement Fine-Tuning LLMs with GRPO](https://www.deeplearning.ai/short-courses/reinforcement-fine-tuning-llms-grpo/) — RL with reward functions for reasoning tasks.
