#  EvalForge
### Agent Evaluation and Failure Discovery Framework for LLM Systems

EvalForge is a lightweight yet extensible evaluation framework designed for **LLM-based Agent systems**.

It provides a complete pipeline for:
- Multi-task evaluation (QA / Recognition / Detection)
- Multi-model benchmarking (Docker / API)
- LLM-as-a-Judge evaluation
- Slice-aware failure analysis and badcase discovery

---

##  Motivation

Most LLM projects focus on building agents, but lack:

-  Reliable evaluation pipelines  
-  Ground truth construction  
-  Failure analysis mechanisms  

EvalForge addresses this by building a **closed-loop evaluation system**:

```

Task → Prediction → Evaluation → Failure Analysis → Optimization

```

---

##  Core Features

### 1. Multi-task Evaluation

- Unified task abstraction:
  - QA
  - Recognition
  - Detection
- Extendable via `task_registry`

---

### 2. Multi-model Execution

- Docker-based model runner  
- OpenAI-compatible API runner  
- Parallel inference scheduler  

---

### 3. Evaluation System

- LLM-as-a-Judge scoring  
- Edit Distance metrics  
- Task-aware evaluation pipelines  

---

### 4. Failure Discovery Engine (Core)

- Badcase mining  
- Slice-based evaluation  
- Error pattern analysis  
- Risk region discovery  

Key modules:

```

evalforge/analysis/
├── error_patterns.py
├── failure_discovery/
├── slice.py
├── risk_region.py

```

---

##  Project Structure

```

evalforge/
├── tasks/              # Task abstraction (QA / detection / recognition)
├── metrics/            # Metrics (edit distance / LLM judge)
├── model_registry/     # Model runners (Docker / API)
├── runner/             # Evaluation pipelines
├── scheduler/          # Parallel execution
├── analysis/           # Failure analysis
├── datasets/           # Dataset loaders
├── reports/            # Reports and visualization

````

---

##  Quick Start

### 1. Install dependencies

```bash
pip install -r requirements.txt
````

---

### 2. Run benchmark

```bash
python run_eval.py --config configs/benchmark_eval.yaml
```

---

### 3. Run leaderboard

```bash
python run_eval.py --config configs/leaderboard_eval.yaml
```

---

### 4. Run real LLM evaluation

```bash
export DEEPSEEK_API_KEY=your_api_key
python run_eval.py --config configs/real_llm_benchmark.yaml
```

---

##  Example Output

```
=== EvalForge Benchmark Summary ===
benchmark: omnidocbench
num_models: 2
edit_distance=0.47
llm_judge=0.81
invalid_outputs=10
```

---

##  Design Philosophy

EvalForge is not just an evaluation tool.

It is designed as a:

>  Failure Discovery Engine for LLM Systems

Its goal is to:

* Identify systematic failure patterns
* Analyze performance under different data slices
* Support model and agent optimization

---

## Roadmap

* [ ] Real model integration (DeepSeek / OpenAI / VLM)
* [ ] Agent-level evaluation (Tool-Use / multi-step reasoning)
* [ ] Automated data generation pipeline
* [ ] Visualization dashboard

---

##  Author

* Liu Yiming
* GitHub: [https://github.com/dimpleoVo](https://github.com/dimpleoVo)

---

## ⭐ Star this repo if you find it useful!

````

---

