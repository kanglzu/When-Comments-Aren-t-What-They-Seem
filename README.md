# Zhihu Toxic Comment Dataset for ICL-DiTox

This repository contains a curated dataset extracted from the social media platform **Zhihu**, which was used in the paper:

> **When Comments Aren’t What They Seem: The Social Media Comment Toxicity Detector for Understanding Contextual Comments**  
> *Zichen Song, Xiaopeng Fan, Yutong Wang, Feixuan Yan, Zijin Wu, Zhongfeng Kang*  
> *Lanzhou University, 2025*

---

## 📘 Overview

This dataset is part of a broader benchmark proposed in the **ICL-DiTox** framework, designed to simulate user interactions and perform **context-aware toxicity detection**. It specifically contains **single-turn user comments from Zhihu**, annotated with toxicity labels and contextual metadata.

The goal is to enable fine-grained evaluation of **context-independent toxicity classification**, serving as the initial input layer before multi-level interaction simulation (see Section 5.2.1 in the paper).

---

## 📁 Dataset Structure

The dataset is provided as an Excel file: `知乎单条.xlsx`.

| Column             | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| `id`               | Unique comment identifier                                                   |
| `comment`          | Raw user comment text (Chinese)                                             |
| `platform`         | Platform name (constant: Zhihu)                                             |
| `toxicity_label`   | Binary label (`1` for toxic, `0` for non-toxic)                             |
| `sarcasm_label`    | Indicates whether sarcasm is suspected (`1` for yes, `0` for no)            |
| `homophone_label`  | Whether the comment uses homophones for implicit toxicity                   |
| `length`           | Length of the comment (number of characters)                                |

> 📌 Annotation was performed manually by three annotators with social media moderation experience. Inter-annotator agreement: **Cohen’s κ = 0.89**.

---

## 🧪 Benchmark Use Case

This dataset supports evaluation for:

- Zero-context toxicity detection baselines
- Sarcasm/homophone detection in isolated comment scenarios
- Dialogue simulation seed inputs for the ICL-DiTox framework

In the paper, this dataset highlighted the challenges of identifying subtle toxicity in knowledge-centric forums like Zhihu.

---

## 📊 Statistics

- Total comments: **1,000**
- Toxic: **395** (39.5%)
- Sarcastic: **163**
- Implicit toxicity via homophones: **108**
- Average comment length: **43.2 characters**

---

## 🧠 Citation

If you use this dataset in your research, please cite our paper:

```bibtex
@article{song2025iclditox,
  title={When Comments Aren’t What They Seem: The Social Media Comment Toxicity Detector for Understanding Contextual Comments},
  author={Song, Zichen and Fan, Xiaopeng and Wang, Yutong and Yan, Feixuan and Wu, Zijin and Kang, Zhongfeng},
  journal={Expert Systems with Applications},
  year={2025}
}

