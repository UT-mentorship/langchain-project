# Chatbot with Llama 2

A Jupyter Notebook–based conversational AI application powered by Meta’s Llama 2 model. This project demonstrates loading a Llama 2 model, tokenizing user inputs, and generating human‑like responses in an interactive notebook environment.

## 🚀 Features

- **Interactive Chat Interface**: Ask questions directly in the notebook and receive streamed or batched responses.
- **Llama 2 Integration**: Leverages Hugging Face’s `transformers` library to load and run Llama 2 (7B / 13B parameters).
- **Custom Prompt Templates**: Easily modify system and user prompt templates for personality and behavior tuning.
- **GPU Acceleration**: Supports CUDA‑enabled GPUs for faster inference (or CPU fallback).
- **Extensible Code Cells**: Breaks down model loading, tokenization, generation, and streaming into reusable notebook cells.

## 🔧 Prerequisites

- **Python 3.8+**
- **git** (to clone the repo or download the notebook)
- **Hugging Face API Token** (if loading gated Llama 2 weights)

## 📦 Installation

1. **Clone this repository** (or download `chatbot_with_llama2.ipynb`)

   ```bash
   git clone <your-repo-url>
   cd <your-repo-directory>
   ```

2. **Create and activate a virtual environment** (recommended)

   ```bash
   python3 -m venv venv
   source venv/bin/activate    # Windows: venv\Scripts\activate
   ```

3. **Install dependencies**

   ```bash
   pip install transformers torch sentencepiece
   ```

## ⚙️ Configuration

1. **Set your Hugging Face token** (if required)

   ```bash
   export HUGGINGFACE_TOKEN="your_token_here"
   ```

2. **Select a model checkpoint**

   - In the notebook’s first cell, update `model_name` to one of:
     - `meta-llama/Llama-2-7b-chat-hf`
     - `meta-llama/Llama-2-13b-chat-hf`

## 🚀 Usage

1. **Launch Jupyter Notebook**

   ```bash
   jupyter lab   # or jupyter notebook
   ```

2. **Open **``

3. **Run cells in order**:

   - **Model loading**: Downloads and initializes the Llama 2 tokenizer and model.
   - **Prompt setup**: Defines the system and user message templates.
   - **Chat loop**: Enter messages in the input cell and execute to get responses.

4. **Customize prompts**

   - Modify the system message (e.g., personality, formatting rules).
   - Adjust generation parameters: `max_new_tokens`, `temperature`, `top_p`, etc.

## 🛠️ How It Works

1. **Tokenizer & Model Loading**:
   - Uses `AutoTokenizer` and `AutoModelForCausalLM` from `transformers`.
2. **Prompt Assembly**:
   - Concatenates system and user messages into a single tokenized prompt.
3. **Text Generation**:
   - Calls `model.generate()` with streaming or non‑streaming options.
4. **Response Decoding**:
   - Converts token IDs back into human‑readable text.

## 🤝 Contributing

Contributions are welcome! Feel free to:

- Experiment with different Llama 2 variants (e.g., 70B).
- Integrate a web or CLI frontend.
- Add caching or memory for multi‑turn conversations.
- Implement evaluation metrics or user feedback loops.

Please open issues or submit pull requests for improvements.

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

