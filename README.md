# AI Text Analysis Tool

## Project Overview

This project demonstrates the practical application of **Generative AI and Transformer-based models** to build a real-world AI-powered text analysis tool. The application provides two core features:

-  Text Summarization — Automatically condenses long articles into concise bullet-point summaries
-  Question Answering — Extracts precise answers to user questions from a given document

The tool is built entirely using free, open-source models from **Hugging Face** and features an interactive web interface powered by **Gradio**.

---

## Models Used

### 1. BART (facebook/bart-large-cnn) — Summarization
**BART** (Bidirectional and Auto-Regressive Transformer) is a sequence-to-sequence model developed by Facebook AI. It was pre-trained on a large corpus and fine-tuned specifically on the CNN/DailyMail news dataset for summarization tasks.

- **Architecture:** Encoder-Decoder Transformer
- **Task:** Text Summarization
- **How it works:** The encoder reads and understands the full input text. The decoder then generates a shorter, coherent summary word by word.
- **Why we chose it:** It produces high-quality, fluent summaries and is freely available on Hugging Face.

### 2. RoBERTa (deepset/roberta-base-squad2) — Question Answering
**RoBERTa** (Robustly Optimized BERT Pretraining Approach) is an optimized version of BERT developed by Facebook AI. This version is fine-tuned on the SQuAD2.0 dataset — a large reading comprehension benchmark.

- **Architecture:** Encoder-only Transformer
- **Task:** Extractive Question Answering
- **How it works:** Given a document and a question, the model identifies the exact span of text in the document that answers the question.
- **Why we chose it:** Excellent accuracy on QA tasks, lightweight, and free to use.

---

##  Prompt Examples & Demo Results

### Example 1 — Summarization

**Input Text:**
> *"Climate change is one of the most serious threats facing our planet today. Rising temperatures caused by greenhouse gas emissions are melting polar ice caps, causing sea levels to rise and threatening coastal cities around the world..."*

**Output Summary:**
> • Climate change is one of the most serious threats facing our planet. Rising temperatures caused by greenhouse gas emissions are melting polar ice caps. Extreme weather events such as floods, droughts, and wildfires are becoming more frequent and more destructive.
>
> • In Nepal, the effects of climate change are already visible. Glaciers in the Himalayas are melting at an alarming rate. Farmers are experiencing unpredictable monsoon seasons.

---

### Example 2 — Question Answering

**Document:** *(Same climate change article)*

| Question | Answer |
|---|---|
| What is the main cause of climate change? | burning of fossil fuels like coal and oil |
| What is happening to glaciers in Nepal? | melting at an alarming rate |
| What is the solution to climate change? | solar and wind power |
| What is the goal for carbon emissions? | net zero by 2050 |

---
