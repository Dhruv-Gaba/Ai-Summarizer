# Summarization Tool

## Overview
The Summarization Tool is a web-based application that uses a **Large Language Model (LLM)** to summarize text documents. Users can upload files or input text, select a summarization style, and receive concise or detailed summaries in their preferred language. The application supports various text formats and languages, providing a flexible and interactive experience for users.

---

## Features
- **File Uploads**: Supports text and PDF files for summarization.
- **Text Input**: Paste text directly into the input box.
- **Customizable Summaries**:
  - Four response styles: List, One Sentence, Concise, and Detailed.
  - Multiple language options, including English, Spanish, German, and more.
- **Model Flexibility**:
  - Handles large inputs using a "map-reduce" approach for efficient summarization.
  - Supports smaller inputs for direct summarization.
- **Real-Time Interaction**: Processes requests interactively using a Gradio interface.

---

## Tech Stack
- **Programming Language**: Python
- **Frontend**: Gradio (Interactive UI)
- **Backend**:
  - LangChain for chaining LLM prompts.
  - LlamaCpp for running the Mistral-7B OpenOrca model locally.
  - Text processing via RecursiveCharacterTextSplitter.
- **Model**: Mistral-7B OpenOrca (Local LLM model).

---

## Prerequisites
- Python 3.8+
- Required Python libraries:
  - `langchain`
  - `gradio`
  - `llama-cpp-python`
  - `PyPDFLoader`
- A compatible hardware setup to run the **Mistral-7B OpenOrca** model.

---

## Installation
1. **Clone the Repository**:
   ```bash
   git clone <repository_url>
   cd summarization-tool
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Download the Model**:
   Place the `mistral-7b-openorca.Q5_K_M.gguf` model file in the `models/` directory.

4. **Run the Application**:
   ```bash
   python app.py
   ```

5. **Access the UI**:
   Open your browser and navigate to `http://127.0.0.1:7860/`.

---

## Usage
1. Upload a text or PDF file, or paste text into the input box.
2. Select the desired summarization style and language.
3. Click the **Generate Summary** button.
4. View the summary and diagnostic information in the output boxes.

---

## File Structure
```
.
├── app.py                 # Main application file.
├── models/                # Directory for storing LLM models.
├── requirements.txt       # List of required Python libraries.
├── README.md              # Documentation.
```

---

## Supported Languages
- English
- Spanish
- French
- German
- Polish
- Turkish
- Czech
- Portuguese

---

## Known Limitations
- Model performance depends on hardware capabilities.
- Summaries for extremely large documents might take longer to process.
- Limited support for languages not listed above.

---

## Future Improvements
- Add support for more file formats (e.g., Word documents).
- Enhance UI with more customization options.
- Integrate cloud-based LLMs for users without high-performance hardware.

---

## Credits
- **Mistral-7B OpenOrca**: Model by Mistral.
- **LangChain**: Framework for building LLM-powered applications.
- **Gradio**: Library for creating interactive UIs.

