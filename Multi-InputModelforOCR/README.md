# Multi-Input Model for OCR — Insurance Code Classification

## Overview

This project explores building a multi-input, multimodal OCR system to extract and classify insurance codes from scanned documents. The emphasis is on using both image and text signals, practical model design, and evaluation strategies that make automated extraction reliable and actionable for downstream workflows.

This README focuses on the project purpose, what you learn from it, and key considerations — not low-level implementation details.

## What you will learn

- How to reason about multimodal inputs (scanned image + extracted text) for robust information extraction.
- How to design training and evaluation pipelines for OCR plus classification tasks (data curation, augmentation, labeling strategies).
- How to evaluate model performance not just by accuracy, but by downstream utility (precision for critical codes, recall for safety-critical items).
- Skills exercised: OCR intuition, multimodal model design, feature engineering for scanned documents, training/validation discipline, and deployment-aware thinking (latency, cost, and privacy).

## Why it matters

Insurance documents are often noisy: scanned pages, varied layouts, and handwritten notes. Combining visual cues (layout, font, position) with textual cues (extracted OCR text, NER) improves robustness. Reliable extraction reduces manual tagging, speeds processing, and lowers human error in billing and claims workflows.

## Contents

- `notebook.ipynb` — the narrative exploration with sample data, model sketches, evaluation examples, and experiments.
- `project_utils.py` — utility functions used by the notebook (data helpers, preprocessing, visualization helpers).

## Model & evaluation notes

- Multimodal approach: combine a visual encoder (for layout and image features) with a text encoder (on OCR output) and fuse the representations for classification.
- Consider layout-aware models (e.g., region-based features or document-layout transformers) when document structure is important.
- Evaluate at multiple levels: token-level extraction accuracy, code-level classification precision/recall, and end-to-end throughput on representative scanned images.
- Track error types: OCR noise, layout variation, ambiguous handwriting — use error analysis to prioritize fixes.