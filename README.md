<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=200&section=header&text=Sathvik%20Maru&fontSize=60&fontColor=ffffff&fontAlignY=38&desc=AI%20Engineer%20%7C%20ML%20Systems%20Builder%20%7C%20CS%20Undergrad&descAlignY=58&descSize=18&descColor=a78bfa" width="100%"/>

</div>

<br/>

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/maru-sathvik-reddy-)
[![Gmail](https://img.shields.io/badge/Gmail-%23EA4335.svg?style=for-the-badge&logo=gmail&logoColor=white)](mailto:marusathvikreddy@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-%23181717.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Sathvik33)

</div>

---

## `$ whoami`

```python
class Sathvik:
    role        = "CS Undergrad → AI/ML Engineer"
    focus       = ["Agentic AI", "Generative AI", "Deep Learning", "ML Systems"]
    building    = "end-to-end AI products — from architecture to deployment"
    philosophy  = "Don't use the API. Understand what's inside it."
```

> I don't just use AI models — I build them from scratch, architect multi-agent pipelines,
> and ship production-grade ML systems. Every project here is a working system, not a tutorial clone.

---

## ⚡ Featured Projects

<br/>

### 🧠 [OmniMind](https://github.com/Sathvik33/OmniMind) — *Multi-Modal RAG Engine · Documents · Images · Video*

> *"Ground your AI answers in real data — not hallucinations."*

A production-grade **multi-modal Retrieval Augmented Generation engine** that ingests PDFs, DOCX, images, and videos — then answers questions strictly from your uploaded content. The standout capability: **timestamp-aware video retrieval** — ask *"what was said in the first 30 seconds?"* and it filters, retrieves, and streams an answer grounded in that exact segment.

```
Upload (PDF / Image / Video)
  → Ingestion Layer (LLaVA vision captioning · OpenCV frame diff deduplication)
  → all-MiniLM-L6-v2 GPU batch embeddings → ChromaDB (with modality + timestamp metadata)
  → Semantic retrieval + temporal filtering → Context Assembly
  → LLaMA3 streaming generation → FastAPI SSE → Streamlit UI
```

**Stack:** `FastAPI` `ChromaDB` `LLaVA 1.5-7B (4-bit quantized)` `LLaMA3 / Ollama` `SentenceTransformers` `OpenCV` `Streamlit`  
**Highlights:** Cross-modal retrieval (text + image + video in one query) · Natural language temporal filters · `cv2.absdiff` frame dedup (60–80% fewer LLaVA calls) · VRAM: 14GB → ~5GB via `bitsandbytes` · Non-blocking background ingestion · Token streaming < 1s first token · Fully offline

---

### 🤖 [Financial Helper Agent](https://github.com/Sathvik33/financial-helper-agent) — *Agentic AI · Real-Time Market Intelligence*

> *"Just type what you want. The agent handles the rest."*

A fully autonomous multi-agent financial analysis system powered by a **locally running Llama 3** model. No API keys. No cloud. No hallucinated numbers — every figure is sourced live.

```
Prompt → Extraction Agent → Ticker Resolution → Market Data + News
       → LLM Reasoning (Llama 3) → Confidence-Scored Recommendation
```

**Stack:** `LangChain` `Ollama / Llama 3` `yfinance` `DuckDuckGo Search` `Streamlit`  
**Highlights:** Tool-augmented LLM architecture · 5-stage agentic pipeline · Fully local inference · Real-time Yahoo Finance data

---

### 🎨 [Imagine Studio](https://github.com/Sathvik33) — *Stable Diffusion · Text-to-Image & Image-to-Image*

> *Production-ready AI image generation with a clean full-stack architecture.*

A complete AI image studio supporting both **Text-to-Image** and **Image-to-Image** workflows. Built around Stable Diffusion with a custom singleton engine, FP16 inference, and a responsive Vanilla JS frontend.

```
Prompt / Input Image → VAE Encoder → U-Net Denoising (DPM Solver)
                     → VAE Decoder → Output (512×512, ~5s GPU)
```

**Stack:** `FastAPI` `HuggingFace Diffusers` `PyTorch` `Stable Diffusion` `HTML/CSS/JS`  
**Highlights:** Attention slicing + VAE slicing · FP16 CUDA inference · Strength-controlled img2img · ~5–9s generation

---

### 🧠 [Multimodal AI Platform](https://github.com/Sathvik33) — *Text · Vision · Image Generation*

> *Three heavy AI models. One GPU. Zero VRAM conflicts.*

A production full-stack AI platform integrating **TinyLlama** (chat), **LLaVA-7B** (VQA), and **DreamShaper** (image gen) — orchestrated by a custom **ModelRegistry** that dynamically swaps models in/out of VRAM on demand.

```
User Request → ModelRegistry → [Unload current] → [Load requested]
             → TinyLlama | DreamShaper | LLaVA → Response
```

**Stack:** `FastAPI` `React + Vite` `TailwindCSS` `PostgreSQL` `SQLAlchemy` `JWT Auth` `BitsAndBytes (8-bit)`  
**Highlights:** Dynamic GPU resource management · 8-bit quantized LLaVA · Full auth system with JWT · REST API + Swagger docs

---

### 🤖 [PyPilot](https://github.com/sathvik33/pypilot) — *GPT-Style LLM Built From Scratch*

> *Not a wrapper. Not a fine-tune. A transformer, built layer by layer.*

A decoder-only GPT-2 style transformer for Python code generation — implemented entirely from scratch in PyTorch. Every component (Causal Attention, AdaIN-style norms, positional embeddings) is hand-coded and documented.

```
Token Embeddings + Positional Embeddings
→ [Causal Self-Attention → FFN → Residual + LayerNorm] × N layers
→ Linear Head → Vocabulary Distribution
```

**Stack:** `PyTorch` `HuggingFace Datasets` `GPT-2 Tokenizer` `CUDA`  
**Config:** 256-dim · 8 heads · 4 layers · 1024 ctx · codeparrot-clean-train (50k samples)  
**Highlights:** Weight tying · Greedy + top-k sampling · Checkpoint resume · Full training loop with gradient clipping

---

### 🎭 [StyleGAN — Conditional Face Generation](https://github.com/Sathvik33) — *Generative Adversarial Networks*

> *Style-based conditional generation on Age, Gender, and Ethnicity.*

A from-scratch PyTorch implementation of **StyleGAN** with a Mapping Network (Z→W), AdaIN-based style injection, and a Projection Discriminator — trained on the UTKFace dataset with R1 gradient penalty and EMA weight averaging.

```
Z (noise) + Attributes → Mapping Network (8-layer MLP) → W
W → StyleConv blocks (AdaIN modulation) + Noise Injection → 64×64 Image
```

**Stack:** `PyTorch` `HuggingFace Datasets (UTKFace)` `CUDA`  
**Highlights:** Custom AdaIN, PixelNorm, NoiseInjection layers · EMA generator · R1 regularization · Conditional on age/gender/ethnicity

---

### 🚗 [Accident Risk Predictor](https://github.com/Sathvik33/Road_Accident_Risk) — *ML · Feature Engineering · XGBoost Ensemble*

> *R² = 0.886. RMSE = 0.003. 80+ engineered features.*

An advanced road safety telemetry system using an **8-model XGBoost ensemble** with Optuna hyperparameter tuning (200 trials). The feature engineering pipeline alone generates 80+ derived features — interaction terms, polynomial transforms, risk scores, binary indicators.

```
Raw Features → Feature Engineering (80+) → SelectKBest
→ Optuna Tuning (200 trials, 3-fold CV) → 8-Model Ensemble
→ Blended Prediction (50% main + 30% mean + 20% median)
```

**Stack:** `XGBoost` `Scikit-learn` `Optuna` `Streamlit` `Plotly` `Pandas`  
**Performance:** R² = 0.886 · RMSE = 0.003 · MAE = 0.044  
**Highlights:** Optuna HPO · Ensemble blending strategy · Speedometer-style Plotly gauge UI · Racing-themed dark dashboard

---

### 🔗 [LangChain + Ollama ChatBot](https://github.com/Sathvik33) — *Local LLM · LangServe · FastAPI*

> *100% offline. No API keys. No limits.*

A complete local LLM application with a **FastAPI + LangServe** backend and **Streamlit** frontend. Exposes essay and poem generation endpoints, all powered by Llama 3 running on-device via Ollama.

**Stack:** `FastAPI` `LangChain` `LangServe` `Ollama / Llama 3` `Streamlit`

---

## 🗂️ More Projects

| Project | Tech | Description |
|---|---|---|
| 🎬 [Movie Recommendation System](https://github.com/Sathvik33/Movie_recommendation) | K-Means · Streamlit | Genre-cluster-based movie recommendations |
| 🧬 [Liver Cancer Prediction](https://github.com/Sathvik33/Liver-Cancer-Prediction) | Scikit-Learn · Streamlit | Tumor malignancy classifier |
| 📈 [Apple Stocks Predictor](https://github.com/Sathvik33/Apple-Stocks-Predictor) | LSTM · TensorFlow · yFinance | Time-series stock price forecasting |
| 🐜 [ACO Wireless Routing](https://github.com/Sathvik33/ACO-wireless-routing) | Ant Colony Optimization | Intelligent routing simulation |
| 🧠 [Virtual Memory Optimizer](https://github.com/Sathvik33/Virtual-Memory-Optimization) | OS Concepts | Paging & fragmentation visualizer |

👉 [View all repositories →](https://github.com/Sathvik33?tab=repositories)

---

## 🛠️ Tech Stack

```
Languages       Python · Java · C++
ML / DL         PyTorch · TensorFlow · Scikit-learn · HuggingFace · XGBoost
Generative AI   Stable Diffusion · StyleGAN · GPT-style LLMs · Ollama
Agentic AI      LangChain · LangServe · Multi-Agent Systems · RAG · ChromaDB
Backend         FastAPI · SQLAlchemy · PostgreSQL · JWT Auth
Frontend        React · Streamlit · Tailwind CSS · HTML/CSS/JS
Tools           Git · VS Code · CUDA · Optuna · Docker (learning)
```

---

## 📊 GitHub Stats

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=Sathvik33&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=a78bfa&icon_color=a78bfa&text_color=c9d1d9"/>
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Sathvik33&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=a78bfa&text_color=c9d1d9"/>

</div>

<div align="center">

![Streak](https://github-readme-streak-stats.herokuapp.com/?user=Sathvik33&theme=tokyonight&hide_border=true&background=0d1117&ring=a78bfa&fire=a78bfa&currStreakLabel=a78bfa)

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=120&section=footer" width="100%"/>

*Open to collaborations, research internships, and full-time AI/ML roles.*  
**Let's build something that matters. → [marusathvikreddy@gmail.com](mailto:marusathvikreddy@gmail.com)**

</div>
