# BenNumEval: A Benchmark to Assess LLM’s Numerical Reasoning Capabilities in Bengali

**BenNumEval** is a novel benchmark designed to evaluate the numerical reasoning abilities of Large Language Models (LLMs) in the Bengali language. It introduces six diverse task categories and a high-quality dataset containing over 3,200 examples derived from educational and real-world sources.

## 🔍 Motivation

Despite recent advances in LLMs, their performance in numerical reasoning, especially in low-resource languages like Bengali, remains significantly limited. BenNumEval addresses this gap by:

- Providing a structured evaluation framework for Bengali numerical reasoning.
- Highlighting the limitations of LLMs in handling arithmetic, logical, and domain-specific reasoning in a linguistically rich yet underrepresented language.

---

## 📁 Dataset Overview

BenNumEval includes **3,255** curated examples divided into six task types:

| Task Type                      | Description                                                                 | Examples |
|-------------------------------|-----------------------------------------------------------------------------|----------|
| Commonsense + Arithmetic (CA) | Problems combining arithmetic with common-sense knowledge                   | 410      |
| Domain-Specific (DS)          | Problems requiring domain knowledge (e.g., physics, chemistry, CS)          | 705      |
| Commonsense + Quantitative (CQ) | Simple comparisons based on everyday logic                                 | 400      |
| Fill-in-the-Blanks (FiB)      | Arithmetic word problems in fill-in-the-blank style                         | 665      |
| Quantitative NLI (QNLI)       | Natural language inference involving numerical understanding                | 425      |
| Arithmetic Word Problems (AWP)| Real-world word problems requiring arithmetic reasoning                     | 650      |

---

## 🔧 Benchmarking Methodology

### 🧠 Prompting Techniques

We evaluate LLMs using three prompting strategies:

- **BNaP (Bengali Native Prompting)**: Fully Bengali prompts and responses.
- **XLP (Cross-Lingual Prompting)**: Bengali questions, English responses.
- **XCoT (Cross-Lingual Chain-of-Thought)**: Bengali inputs, step-by-step English solutions using CoT reasoning.

### 🧪 Evaluated Models

- GPT-4o
- Gemini-2.0-flash
- Llama-3.3-70B
- DeepSeek-R1-Distill-Llama-70B
- Mathstral-7B

Accuracy is measured using **Exact-Match (EM)**, and we also report human baseline performance for comparison.

---

## 📊 Key Results

- Top models (e.g., GPT-4o, Gemini-2.0-flash) achieve ~70–80% accuracy under cross-lingual prompting.
- Human performance remains significantly higher at ~98%, revealing persistent challenges in LLM numerical reasoning.
- Domain-specific and QNLI tasks remain the hardest across all models and prompts.

---

## 🔍 Error Analysis

We include both:
- `Wrong Format (wf%)`: Output not in the required structure.
- `Wrong Calculation (wc%)`: Incorrect answer despite proper formatting.

Findings show that advanced prompting like XCoT improves reasoning but sometimes increases formatting issues.

---

## 📜 Citation

If you use **BenNumEval** in your work, please cite:

```bibtex
@inproceedings{ahmed-etal-2025-bennumeval,
    title = "{B}en{N}um{E}val: A Benchmark to Assess {LLM}s' Numerical Reasoning Capabilities in {B}engali",
    author = "Ahmed, Kawsar  and
      Osama, Md  and
      Sharif, Omar  and
      Hossain, Eftekhar  and
      Hoque, Mohammed Moshiul",
    editor = "Che, Wanxiang  and
      Nabende, Joyce  and
      Shutova, Ekaterina  and
      Pilehvar, Mohammad Taher",
    booktitle = "Findings of the Association for Computational Linguistics: ACL 2025",
    month = jul,
    year = "2025",
    address = "Vienna, Austria",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2025.findings-acl.915/",
    pages = "17782--17799",
    ISBN = "979-8-89176-256-5",
    abstract = "Large Language Models (LLMs) demonstrate exceptional proficiency in general-purpose tasks but struggle with numerical reasoning, particularly in low-resource languages like Bengali. Despite advancements, limited research has explored their numerical reasoning capabilities in these languages. To address this gap, we present BenNumEval (Bengali Numerical Evaluation), a benchmark designed to assess LLMs on numerical reasoning tasks in Bengali. It comprises six diverse tasks and a total of 3.2k samples curated from real-world problem-solving scenarios. Our extensive evaluations reveal that even with advanced prompting techniques such as Cross-Lingual Prompting (XLP) and Cross-Lingual Chain-of-Thought Prompting (XCoT), LLMs fall notably short of human-level performance, particularly when using Bengali Native Prompting (BNaP). These findings underscore the substantial gap between current LLM capabilities and human expertise in numerical reasoning, highlighting the need for more robust and linguistically inclusive AI models to advance Bengali Language Processing and equitable AI development. The source code for the system and evaluation pipeline is publicly available on GitHub."
}
```

---

## ⚖️ License

BenNumEval is released under the [MIT License].

---

## 🌐 Links

* 📄 [Paper (PDF)](https://aclanthology.org/2025.findings-acl.915/)
* 🤗 [Hugging Face Dataset](https://huggingface.co/datasets/ka05ar/BenNumEval)

