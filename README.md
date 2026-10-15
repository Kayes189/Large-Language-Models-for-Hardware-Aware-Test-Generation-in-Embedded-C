# Large Language Models for Hardware-Aware Test Generation in Embedded C
### A Systematic Review of Peripheral Dependencies, Interrupts, and Execution Validation

## 📖 Overview
This repository contains the final manuscript and supporting artifacts for a systematic literature review (SLR) investigating how Large Language Models (LLMs) are used for hardware-aware test generation in Embedded C. 

The review synthesizes findings across **9 research questions (RQ1–RQ9)**, joining two previously disconnected literatures: non-LLM firmware re-hosting/fuzzing and LLM-driven test generation. It strictly adheres to the **PRISMA 2020 reporting format** (without claiming formal compliance) and includes a transparent audit trail of the review process.

**Authors:** Abu Kayes Huda, Jaidul Islam, MD Sakib Hasan, Majumdar Nahidul Hasan, Mohammad Mostafejur Rahaman
*(Note: Affiliations and funding details are placeholders pending final submission).*

## 🔍 Key Findings
*   **Test Type Bimodality:** Reported test types are strictly bimodal—Unit (2/4) and HIL/system-level (2/4)—with Integration (0/4) and Regression (0/4) testing completely absent. Only 1/4 of studies emit C test code.
*   **LLM Strategies:** Zero-shot prompting (6/7), RAG (5/7), and agentic workflows (4/7) dominate, but only 1/7 fine-tunes the generation LLM.
*   **Hardware Context Gap:** While software context (code/repo) is provided to LLMs in 8/8 studies, hardware documentation (register maps, datasheets, MCU specs, HAL/driver code) is supplied at inference time in **0/8** studies.
*   **Dependency Handling:** Dependency handling is delegated, not generated. In 5/6 studies, the LLM produces no dependency-handling artifacts; behaviorally faithful test doubles (register/timing/interrupt semantics) are 0/27 configurations.
*   **Execution & Validation:** Execution is universally emulator-bound (6/6; QEMU in 5/6). Real hardware is used as the *primary* execution environment in **0/6** studies. Loops close universally (5/5) on software signals, but hardware/peripheral feedback is only 1/5.
*   **The "Missing Middle":** No study in the verified corpus is simultaneously LLM-based, test-generating, embedded-C-source-level, and hardware-aware. The review identifies this as a **pre-paradigm intersection**, not a failing literature.

## 📂 Repository Contents
*   `LLM'S FOR EMBEDDED.html` – The complete, interactive final manuscript. Includes:
    *   Full text (Abstract, Introduction, Methodology, Results, Discussion, Conclusion).
    *   **15 interactive SVG Figures** (PRISMA flow, RQ counts, gap matrices, overlap matrices).
    *   **5 detailed Tables** (Exclusion codes, Counting layers, Cohorts, Denominators, Type I/II zero definitions).
    *   **References** (Parts A, B, C).
    *   **Appendices A–G**: Search protocol, Eligibility criteria, Study characteristics, Metadata conflicts, Unresolved issues, Supplementary materials, and Factual claims provenance.

*(Note: Associated data extraction spreadsheets and verification PDFs are referenced within the text but not included in this repository).*

## 🛠️ Methodology & Rigor
This review is characterized by extreme transparency regarding its limitations and evidence strength:
*   **Strict Counting Rules:** Distinguishes between *records* (46), *reports* (29), and *studies* (28) to prevent double-counting.
*   **Cohort Demarcation:** Studies are split into LLM-construct (N=13), Contextual non-LLM (N=8), General-SE comparator (N=4), and Grey-zone (N=3).
*   **Type I vs. Type II Zeros:** Differentiates between "method not used in this dataset" (Type I) and "not discussed as a limitation" (Type II), preventing false gap claims from silence.
*   **Unresolved Conflicts:** All metadata conflicts (C1–C12) and unresolved issues (U1–U12) are printed side-by-side rather than silently resolved, ensuring full auditability.

## ⚠️ Important Disclaimers
*   **PRISMA 2020 Format:** The manuscript is reported in the *format* of PRISMA 2020 but does **not** claim formal compliance.
*   **Search Limitations:** The original search documentation is incomplete (no bibliographic database search was documented; only a 59-record DeepSeek export is evidenced). The supplementary search (Scopus, IEEE, ACM) was **proposed but not executed**.
*   **Evidence Base:** Findings are bounded to the verified dataset (N=4–8 per RQ). No prevalence claims about the wider literature are made.

## 📄 How to View
Simply download or clone this repository and open `LLM'S FOR EMBEDDED.html` in any modern web browser. 

The file is completely self-contained (no external CDN, CSS, or internet connection required). It includes interactive navigation, a reading progress bar, and a toggle to switch between full-size and compact figures for easier reading.

## 📜 Citation
If you reference this work, please cite the manuscript as:

> Huda, A. K., Islam, J., Hasan, M. S., Hasan, M. N., & Rahaman, M. M. (2026). *Large Language Models for Hardware-Aware Test Generation in Embedded C: A Systematic Review of Peripheral Dependencies, Interrupts, and Execution Validation*. [Systematic Literature Review Manuscript].

---
*Note: This repository is intended for academic and research purposes. The data notes (N1–N8) and Threats to Validity (Section 7) should be read carefully before citing any specific percentage.*
