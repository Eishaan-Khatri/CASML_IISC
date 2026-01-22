# Bridging the Gap: Enhancing and Evaluating Zero-Cost LLMs for Scientific Question Answering

[![Conference](https://img.shields.io/badge/Conference-CASML%202025-blue)](https://www.casml.cc)
[![Status](https://img.shields.io/badge/Status-Accepted%20(Poster)-success)](https://www.casml.cc)
[![Venue](https://img.shields.io/badge/Venue-IISc%20Bangalore-red)](https://iisc.ac.in)

**Authors:** Mahule Roy\*, Snehal Rakshit, Shinjini Mondal, Rahul Jaisy, Varun Ramanathan Alagappan, Eishaan Khatri, Vedant Vijay Patil, Archishman Banerjee, Mariane Desiree C. Avendaño, Yashika Sharma, Nanditha Immidi, Theo Fraser, Emanuel Espinoza Prado, Gayathri Aishwarya E, Akash Kanji, Oviya.

*\*Corresponding Author: [mahule.roy@kellogg.ox.ac.uk](mailto:mahule.roy@kellogg.ox.ac.uk)*

---

## 📢 News
*   **[November 2025]** Our paper has been accepted for a **Poster Presentation** at the **2nd Conference on Applied AI and Scientific Machine Learning (CASML 2025)** at IISc Bangalore!
*   **[December 2025]** We will be presenting our findings on **December 8-11, 2025**.

---

## 📄 Abstract

Large language models (LLMs) accessible at zero monetary cost (via open-source platforms or public APIs) have democratized access to AI but often lack factual accuracy and domain-level reasoning in scientific applications. General models tend to distort facts, abuse scientific jargon, and fail to adhere to physicochemical constraints.

In this work, we present an end-to-end framework to analyze and improve free-tier LLMs for scientific contexts. Our approach integrates:
1.  **Dense Retrieval:** Fetching contextually relevant documents.
2.  **Structured Grounding:** Utilizing a scientific knowledge graph.
3.  **Unsupervised Trend Analysis:** Extracting insights from live literature (e.g., arXiv).

By feeding both unstructured and structured contexts to the LLM via sophisticated prompting (Chain-of-Thought), we significantly enhance performance.

**Key Result:** Our approach reduces hallucinations by **68%** and continuously enhances the scientific basis of model outputs.

---

## 🏗️ Methodology & Architecture

We introduce a two-stage improvement pipeline designed to move beyond simple retrieval.

### The Pipeline
1.  **Entity Extraction & Retrieval:** For every question, the system determines applicable entities and fetches contextually relevant documents using Dense Passage Retrieval (DPR).
2.  **Knowledge Graph Grounding:** We utilize a specific Scientific Knowledge Graph to enforce structured reasoning.
3.  **Live Trend Analysis:** An unsupervised clustering algorithm analyzes research trends from papers (e.g., Nature, Science, arXiv) to ensure the model is up-to-date.
4.  **Neuro-Symbolic Prompting:** The system combines the retrieved literature (unstructured) and graph data (structured) into a cohesive prompt using Chain-of-Thought (CoT) reasoning.

### Evaluation Metrics
We introduce three domain-specific metrics to evaluate scientific rigor beyond standard NLP benchmarks:
*   **FC-PS (Factual Correctness in Physical Sciences):** Accuracy of discrete claims vs. authoritative sources.
*   **QPCS (Quantified Physicochemical Constraints Score):** Adherence to deterministic physicochemical laws.
*   **Literature Alignment:** Assessing how well the output aligns with current research trends.

---

## 📊 Results

We benchmarked free-tier models including **QWEN**, **BARD/GEMINI**, and **ChatGPT** against a validated dataset of questions in materials science and physics.

*   **Accuracy:** QWEN and BARD surpassed ChatGPT in factual accuracy (FC-PS) and constraint observance (QPCS).
*   **Reasoning:** BARD exhibited the highest scientific groundedness (SGS).
*   **Hallucinations:** Our enhancement pipeline reduced hallucinations by **68%** compared to baseline zero-shot performance.

---

## 👥 The Team & Affiliations

This project is a collaborative effort across multiple international institutions:

*   **University of Oxford, UK** (Mahule Roy)
*   **IIT Kharagpur** (Snehal Rakshit, Vedant Vijay Patil)
*   **IISER Pune** (Shinjini Mondal)
*   **RGIPT Jais** (Eishaan Khatri)
*   **IISER Tirupati** (Varun Ramanathan Alagappan)
*   **TU Delft** (Mariane Desiree C. Avendaño)
*   **NUS Singapore** (Oviya)
*   **St. Xavier’s College, Kolkata** (Archishman Banerjee)
*   **AEC, Guwahati** (Rahul Jaisy)
*   **MAIT Delhi** (Yashika Sharma)
*   **IACS Kolkata** (Nanditha Immidi)
*   **The Open University** (Theo Fraser)
*   **UCR** (Emanuel Espinoza Prado)
*   **Jadavpur University** (Akash Kanji)
*   **Independent Researcher** (Gayathri Aishwarya E)

---

## 📍 Conference Details

**CASML 2025: Conference on AI for Scientific Machine Learning**
*   **Date:** December 8-11, 2025
*   **Venue:** A V Rama Rao Auditorium, Chemical Sciences Building, Indian Institute of Science (IISc), Bangalore, India.
*   **Organized By:** Computational and Data Sciences (CDS), IISc.

---

## 📝 Citation

If you find this work useful, please cite our CASML 2025 paper:

```bibtex
@inproceedings{roy2025bridging,
  title={Bridging the Gap: Enhancing and Evaluating Zero-Cost LLMs for Scientific Question Answering},
  author={Roy, Mahule and Rakshit, Snehal and Mondal, Shinjini and Khatri, Eishaan and Patil, Vedant Vijay and others},
  booktitle={2nd Conference on Applied AI and Scientific Machine Learning (CASML 2025)},
  year={2025},
  organization={IISc Bangalore}
}
