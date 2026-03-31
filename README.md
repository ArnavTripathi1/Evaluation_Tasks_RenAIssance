# RenAIssance OCR Tasks

## Overview

This repo is my submission of evaluation tasks for **Automating text recognition and transcription of historical documents** RenAIssance, HumanAI.

## Notebooks

1. Notebook [RenAIssance_NB1.ipynb](./RenAIssance_NB1.ipynb) contains data parsing, PDF-to-image conversion, and ground-truth alignment.
2. Notebook [RenAIssance_NB2.ipynb](./RenAIssance_NB2.ipynb) contains the core OCR model (TrOCR), rare character analysis, and baseline evaluation.

## Problem Statement

Transliteration of text from centuries-old works represents a research area that is underserved by current tools (e.g., standard PDF OCR). While standard resources perform well on modern sources, they are incapable of extracting textual data from early forms of print and manuscripts. This project applies AI models based on Transformer architectures and LLM integration to recognize text in Spanish printed sources from the seventeenth century.

## Specific Test I. Optical Character Recognition of printed sources

Dataset Parsing and Core Model Training

Dataset: 17th-Century Spanish Printed Sources (Scanned PDFs & `.docx` Transcriptions)

### Notebook 1: Preprocessing
Handles the extraction of transcriptions from `.docx` files, converts multi-page PDF scans into high-resolution `JPEG` images, and aligns the ground truth labels to construct a paired dataset.

### Notebook 2: Core OCR Model
Implements a Transformer-based OCR model (`microsoft/trocr-base-printed`) to decode historical text. Introduces a weighted learning strategy (`RARE_BOOST`) to heavily penalize errors on rare/archaic letterforms and 17th-century Spanish diacritics.

## Specific Test II. Text recognition of handwritten sources

*(Ongoing Work - To be added)*
Will feature an end-to-end LLM/VLM pipeline (e.g., Gemini) embedded throughout the reading, interpretation and spelling correction stages.

## Results

### Specific Test I

### 1. Dataset Statistics

| Feature | Count |
| ------- | ----- |
| Total PDF Sources | 6 |
| Unique Characters (incl. rare/archaic) | > 80 |
| Ground Truth Transcriptions Parsed | ✓ |


## Repository Structure

```text
.
├── RenAIssance_NB1.ipynb
├── RenAIssance_NB2.ipynb
└── README.md
