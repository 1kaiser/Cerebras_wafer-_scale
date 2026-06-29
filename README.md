# Cerebras_wafer📀_scale


---

#  SwarmSearch ERP

### Wafer-Scale Parallel Multi-Agent Research Browser & Knowledge Graph Visualizer

SwarmSearch ERP is a next-generation multi-agent autonomous framework engineered to conquer dense, multi-intent document searches. Powered by **Gemma 4 31B** on **Cerebras' wafer-scale inference engine**, the app splits compound enterprise queries into decoupled, parallelized research workflows. It bypasses traditional multi-agent latency bottlenecks by dropping execution speeds down to instantaneous, real-time responses.

```text
📦 Project Architecture Layout
└── 📑 visual_foraging_agent.py  <-- Thread-safe parallel worker backend
└── 💿 Wafer_Scale_Reader.ipynb   <-- Active notebook runtime environment
└── 💾 trajectory_graph.json      <-- Live-updating knowledge graph state
└── 📁 runs/                       <-- Session-isolated directories
    └── 🔒 memory_scope_[slug].txt <-- Folder-bound persistent long-term memory

```

---

## 🚀 Key Architectural Features

### 🧵 Concurrent Multi-Orchestration Engine

Traditional multi-agent frameworks stall because agents complete tasks sequentially. SwarmSearch ERP uses a high-concurrency `ThreadPoolExecutor` and optimized regular-expression tokens to split compound tasks (e.g., *"Solve question 9 from chapter 10 AND question 12 from chapter 4"*) instantly. It deploys multiple parent orchestration lines simultaneously, which then dynamically spawn parallel **Swarm Child Agents** to analyze specific targets.

### 💾 Folder-Isolated Long-Term Memory

To allow generalized searches across multiple completely unrelated document repositories, memory is tightly coupled to the directory pathway (`EXTRACT_DIR`). Changing the target directory automatically initializes or context-swaps to a specialized memory block, preventing cross-contamination of academic or enterprise knowledge fields.

### 📊 Real-Time Token HUD & D3.js Visual Tracker

The search path is translated on the fly into an elegant, light-gradient interactive trajectory map. It includes a floating **Session Token Usage HUD** that increments node-by-node during playback animations, providing perfect transparency over prompt, completion, and cumulative data metrics.

---

## 🛠️ Installation & Setup

1. **Clone the Repository:**
```bash
git clone https://github.com/your-username/swarmSearch-erp.git
cd swarmSearch-erp

```


2. **Install Dependencies:** Ensure your execution environment has the required software packages installed:
```bash
pip install cerebras-cloud-sdk jupytext ipython

```


3. **Provide API Credentials:** Set up your Cerebras environment variable:
```bash
export CEREBRAS_API_KEY="your-cerebras-api-key-here"

```



---

## ⚙️ Configuration Parameters

The orchestration script can be parameterized via Papermill or run natively inside your Jupyter notebook cell configurations:

| Parameter | Type | Default Value | Description |
| --- | --- | --- | --- |
| `CEREBRAS_API_KEY` | `String` | `"PLACEHOLDER"` | Falls back to system environment variables if left blank. |
| `MODEL_ID` | `String` | `"gemma-4-31b"` | The underlying vision-language foundational model identity. |
| `EXTRACT_DIR` | `String` | `"/content"` | The directory path holding target corporate/textbook PDFs. |
| `SEARCH_QUERY` | `String` | `"Organic Molecules"` | The raw, multi-intent prompt text block input. |

---

## 🕹️ Running the Simulation

Execute the main workflow loop inside your terminal or notebook wrapper:

```python
from visual_foraging_agent import run_foraging_simulation

# The engine auto-scans documents, applies page-translation formulas,
# and spins up parallel workspace threads concurrently.
run_foraging_simulation()

```

Once the run completes, spin up the companion visualizer cell within your notebook to watch the sequence replay with interactive zoom controls, hover tooltips, and real-time token tracking metrics.

---

## ⚖️ License

Distributed under the MIT License. See `LICENSE` for more information.
