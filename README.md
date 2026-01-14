# CauldronSV HiFi ⚗️

**An Integrated Multi-Caller Pipeline for High-Confidence Multi-Sample Structural Variation Discovery Using PacBio HiFi Data.**

[![Status](https://img.shields.io/badge/Status-Coming_Soon-yellow)]()
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

## 🚀 Overview
**CauldronSV HiFi** is a fully automated and reproducible **Snakemake** pipeline designed to generate high-confidence Structural Variant (SV) sets from **PacBio HiFi** data across multiple samples.

Structural variants (SVs) are a major source of genomic diversity and play key roles in gene regulation, adaptation, and phenotypic variation. While Third-Generation Sequencing (TGS) enables the study of these polymorphisms, SV discovery remains challenging due to caller-specific biases, symbolic allele usage, and heterogeneous output formats.

**CauldronSV HiFi solves these challenges by integrating four complementary SV callers:**
1.  **Sniffles2**
2.  **cuteSV**
3.  **SVIM**
4.  **pbsv**

The pipeline is optimized for HiFi read characteristics and optionally combines read-based and assembly-based calling (**cuteSV/SVIM-asm**) to improve the detection of larger genomic variants while maximizing parallelism.

**(Poster presented at PAG33, 2026)**

## ✨ Key Features

### 🛠️ Multi-Caller Integration & Harmonization
* **VCF Harmonization Layer:** Resolves inconsistencies across callers and standardizes output formats.
* **Advanced Merging:** Automatically merges single-caller results through **SURVIVOR** and **Truvari** to obtain a superior consensus callset.
* **Sequence Integrity:** Maintains linkage between representative and collapsed variants, reconstructs symbolic ALT alleles, and ensures every retained variant is associated with a proper sequence.

### 📊 Multisample & Population Analysis
* **Scalability:** The unified callset can be expanded to the multisample level, allowing users to analyze the presence and distribution of variants across populations.
* **Companion Benchmark:** Automatically produces a **Sniffles multisample-only** callset for direct quality comparison.
* **Comprehensive Statistics:** Generates detailed summary statistics at both single-sample and multisample levels.

### 🧬 Specialized Detection
* **Translocation Merging:** Includes an optimized strategy to preserve breakpoint orientation across multi-caller and multisample stages.
* **TE Discovery:** High-quality SVs serve as an excellent substrate for Transposable Element (TE) discovery. The pipeline facilitates the clustering of SVs with similar breakpoints to reconstruct consensus TE families.

## 🏆 Performance
This optimized multi-caller approach results in **substantial gains in accuracy, precision, and recall**, with significant reductions in false positives and false negatives compared to any single caller alone.

* **Benchmarked against:** The long-read SV calling framework released by *Zook et al. (Nature Biotechnology, 2020)*.
* **Validated on:** An internal *Oryza sativa* dataset.

## 📅 Release Roadmap
The source code and documentation are currently being finalized for public release.
**Expected Release Date:** Late January 2026.

> **Want to be notified?** Click the **Star ⭐** and **Watch 👁️** buttons at the top right of this page!

## 📬 Contact
For early access or inquiries:
* **Name:** [Leonardo Fabbian]
* **Email:** [leonardo.fabbian@gmail.com]
* **Lab:** [Wing Lab - KAUST]
