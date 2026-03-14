<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a0a0f,30:0d1b2a,60:1a1a2e,100:16213e&height=220&section=header&text=Maru%20Sathvik%20Reddy&fontSize=58&fontColor=e2e8f0&fontAlignY=36&desc=I%20build%20AI%20systems%20that%20think%2C%20plan%2C%20and%20act%20autonomously&descAlignY=58&descSize=16&descColor=94a3b8" width="100%"/>
</div>

<br/>

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0a66c2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/maru-sathvik-reddy-)&nbsp;&nbsp;
[![Gmail](https://img.shields.io/badge/Gmail-ea4335?style=flat-square&logo=gmail&logoColor=white)](mailto:marusathvikreddy@gmail.com)&nbsp;&nbsp;
[![GitHub](https://img.shields.io/badge/GitHub-161b22?style=flat-square&logo=github&logoColor=white)](https://github.com/Sathvik33)&nbsp;&nbsp;
![Visitors](https://komarev.com/ghpvc/?username=Sathvik33&style=flat-square&color=6366f1&label=profile+views)

</div>

<br/>

```
  areas of focus   →  agentic systems · inference engineering · local LLM deployment
  how I work       →  understand the internals before building on top of them
  what I build     →  multi-agent pipelines, transformers from scratch, production ML systems
```

<br/>

## `> identity`

```python
sathvik = {
    "status"      : "CS Undergrad @ LPU — building things that matter",
    "obsession"   : ["Agentic AI", "Multi-Agent Systems", "Local LLMs", "ML from scratch"],
    "principle"   : "Don't call the API. Understand what's inside it.",
    "open_to"     : ["AI/ML internships", "Research roles", "Agentic AI engineer positions"],
}
```

<br/>

## `> weapons of choice`

<table>
<tr>
<td valign="top" width="50%">

**Core Intelligence**
```
PyTorch         ████████████  transformers, attention, CUDA
LangGraph       ████████████  stateful agent orchestration  
LangChain       ███████████   tool-calling, RAG, routing
HuggingFace     ██████████    embeddings, tokenizers, models
Scikit-learn    █████████     classical ML, ensembles
OpenCV          ████████      vision preprocessing
```

</td>
<td valign="top" width="50%">

**Systems & Infrastructure**
```
FastAPI         ████████████  async backend, background tasks
Redis Stack     ███████████   vector search, caching, pub/sub
Docker + Nginx  ██████████    containerized deployment
Ollama          █████████     local LLM inference
Streamlit       ████████      rapid ML frontends
PostgreSQL      ███████       relational data
```

</td>
</tr>
</table>

<br/>

## `> systems I've built`

> sorted by technical depth — not by stars

<br/>

### `[01]` — ResearchForge AI
> **The one that changed how I think about agent design**

A fully local multi-agent research system. Five specialized agents collaborate through a LangGraph state machine — Supervisor routes, Planner decomposes, Researcher scrapes the web in parallel, Analyst synthesizes, Writer generates. The interesting parts: a 3-layer Redis Stack cache (prompt-level + versioned reports + HNSW vector similarity search), hybrid report generation that merges cached context with fresh data, an agentic chat layer that detects intent and calls tools on demand, and SHA256-derived thread IDs for MemorySaver crash recovery.

**Zero OpenAI. Zero paid APIs. 100% local.**

`LangGraph` `LangChain` `FastAPI` `Redis Stack` `all-MiniLM-L6-v2` `Qwen2.5:7b` `Ollama` `Docker` `Nginx` `Streamlit`

[![ResearchForge](https://img.shields.io/badge/→_ResearchForge_AI-6366f1?style=flat-square)](https://github.com/Sathvik33/ResearchForge-AI)

---

### `[02]` — OmniMind — Multimodal RAG
> **Ask questions over documents, images, and videos. Timestamp-aware.**

*"What was being discussed at the 1:30 mark?"* — that's a query OmniMind can answer. Built a multi-modal RAG pipeline with document ingestion, image understanding via LLaVA, and frame-differencing for video. ChromaDB vector indexing, batched GPU embeddings, streaming token responses. The hard part was making all three modalities share the same retrieval interface without hacking it together.

`PyTorch` `LLaVA` `LLaMA3` `ChromaDB` `Sentence-Transformers` `FastAPI` `OpenCV` `Streamlit` `Docker`

[![OmniMind](https://img.shields.io/badge/→_OmniMind-0ea5e9?style=flat-square)](https://github.com/Sathvik33/OmniMind)

---

### `[03]` — PyPilot — GPT-style Code Generator
> **Built every single layer. No shortcuts.**

Decoder-only transformer for Python code generation — written entirely in PyTorch from scratch. Causal self-attention, rotary positional embeddings, token embeddings, and a next-token prediction head. Trained on the CodeParrot dataset with GPT-style tokenization. The reason I built this: most people use transformers without understanding attention. I wanted to understand attention.

`PyTorch` `Transformer Decoder` `Causal Self-Attention` `GPT Tokenization` `CUDA` `HuggingFace`

[![PyPilot](https://img.shields.io/badge/→_PyPilot-10b981?style=flat-square)](https://github.com/sathvik33/pypilot)

---

### `[04]` — StyleGAN — Conditional Face Generation
> **Built from scratch. Not fine-tuned. Not wrapped.**

Conditional face generation with age, gender, and ethnicity control — trained on UTKFace. Implemented the full StyleGAN architecture: Mapping Network, AdaIN normalization, progressive growing, R1 gradient penalty, and EMA weight averaging. Every component written from scratch to understand why StyleGAN produces sharper faces than vanilla GANs.

`PyTorch` `GANs` `StyleGAN` `AdaIN` `CUDA` `UTKFace`

[![StyleGAN](https://img.shields.io/badge/→_StyleGAN-f59e0b?style=flat-square)](https://github.com/Sathvik33)

---

### `[05]` — Multimodal AI Platform
> **Three heavy models on one GPU — without VRAM conflicts**

Chat, image generation, and visual Q&A on a single GPU using a custom `ModelRegistry` that hot-swaps models. The problem: loading all three simultaneously causes VRAM overflow. The solution: a registry that evicts and loads on-demand. Full-stack — React frontend, FastAPI backend with JWT auth, PostgreSQL, and LLaVA + Stable Diffusion + LLaMA3 sharing one GPU.

`React` `FastAPI` `LLaVA` `Stable Diffusion` `LLaMA3` `PostgreSQL` `JWT` `PyTorch`

[![Platform](https://img.shields.io/badge/→_Multimodal_Platform-8b5cf6?style=flat-square)](https://github.com/Sathvik33)

---

### `[06]` — Road Accident Risk Predictor
> **Global Rank 588 — Top 15% on Kaggle**

XGBoost ensemble with 8 models stacked, 80+ engineered features, and Optuna hyperparameter tuning. R² = 0.886 on road safety telemetry data. The interesting engineering: feature interaction terms that captured non-linear risk relationships that single-model approaches missed entirely.

`XGBoost` `Optuna` `Scikit-learn` `Feature Engineering` `Ensemble Methods` `Streamlit`

[![Kaggle](https://img.shields.io/badge/→_Accident_Risk_Predictor-ef4444?style=flat-square)](https://github.com/Sathvik33/Road_Accident_Risk)

<br/>

👉 **[All repositories →](https://github.com/Sathvik33?tab=repositories)**

<br/>

## `> numbers`

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=Sathvik33&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=6366f1&icon_color=6366f1&text_color=94a3b8&ring_color=6366f1"/>
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Sathvik33&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=6366f1&text_color=94a3b8"/>

</div>

<div align="center">

![Streak](https://github-readme-streak-stats.herokuapp.com/?user=Sathvik33&theme=github-dark-blue&hide_border=true&background=0d1117&ring=6366f1&fire=6366f1&currStreakLabel=6366f1&sideLabels=94a3b8&currStreakNum=e2e8f0&sideNums=e2e8f0&dates=64748b)

</div>

<br/>

## `> certifications`

```
Generative AI, LLM & RAG     GeeksforGeeks          Feb 2026
Foundational ML Concepts      AWS ML Exam Basics      Oct 2025  
ML with Data Science          Cipher Schools          Jul 2025
Deep Learning with TensorFlow IBM Cognitive Class     Mar 2025
```

<br/>

---

<div align="center">

```
currently open to: AI/ML internships · Agentic AI roles · Research positions
```

**→ [marusathvikreddy@gmail.com](mailto:marusathvikreddy@gmail.com)**

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:16213e,50:1a1a2e,100:0a0a0f&height=100&section=footer" width="100%"/>

</div>
