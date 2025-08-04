
# Solved Problem: Q&A Document-Based Chatbot System

This file describes how a Q&A chatbot responds successfully with information find in a document which it was trained:

- **Gradio** for user interaction
- **PyPDF** for document ingestion
- **Hugging Face Transformers** with model **quantization**
- **Google Colab** as the runtime environment
- Support for **easy switching between multiple models**
- Integration using `pipeline`, `AutoTokenizer`, and `AutoModelForCausalLM`

---

## ✅ Problem Statement

Design and implement an interactive Q&A chatbot that:
- Accepts PDF documents as input
- Extracts context from the documents
- Allows users to ask questions related to the content
- Supports multiple model backends for Q&A
- Runs efficiently in a Google Colab environment using quantized models

---

## ✅ Key Components and Solutions

### 1. PDF Document Handling with PyPDF
- Used **PyPDF** to extract text from user-uploaded PDFs.

### 2. Q&A Pipeline with Transformers
- Used `pipeline(task="text-generation" or "text2text-generation)` to create the Q&A functionality.
- Leveraged **AutoTokenizer** and **AutoModelForCausalLM** for model loading.

### 3. Quantization for Efficient Inference
- Quantized models using `bitsandbytes` or pre-quantized versions (e.g., int8, ggml) were used to reduce memory usage.
- Enabled chatbot deployment within Colab’s limited VRAM/GPU resources.

### 4. Interactive UI with Gradio
- Built a dynamic interface using Gradio for:
  - Model selection dropdown
  - Question input and chatbot responses
- Integrated loading logic for dynamic model switching.

### 5. Multiple Model Support
- Models (e.g., `Qwen`, `Llama`, `gemma`, etc.) were mapped in a dictionary.
- User can switch models via a dropdown without reloading the page.
- Each model initialized using `AutoTokenizer` + `AutoModelForCausalLM` combination.

## ✅ Outcome

- Users can upload a document, select a model, and ask context-specific questions via a web interface.
- The chatbot runs reliably in Google Colab and supports switching between multiple interactive models.
- Efficient quantization ensures performance within Colab’s compute limits.

---

## 🔧 Tools & Libraries

- `gradio`
- `pypdf2`
- `transformers`
- `torch`, `bitsandbytes` (for quantization)
- `google.colab` (runtime environment)

---

## 📌 Future Enhancements

- Add RAG (Retrieval-Augmented Generation) pipeline support.
- Integrate OCR for scanned PDFs.
