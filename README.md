# AI Writer 🖋️


![logo](v.png)


A sleek desktop application for AI-assisted writing powered by **Ollama** and built with **PyQt5**. Let your local LLM continue your stories, articles, or documents seamlessly.

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org)
[![PyQt5](https://img.shields.io/badge/PyQt5-5.15+-green.svg)](https://www.riverbankcomputing.com/software/pyqt/)
[![Ollama](https://img.shields.io/badge/Ollama-Local%20LLM-orange.svg)](https://ollama.ai)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## ✨ Features

- **🤖 AI Text Completion** - Continue your writing with local LLM models via Ollama
- **🎨 Light/Dark Theme** - Toggle between beautiful light and dark modes
- **🌡️ Temperature Control** - Adjust creativity vs. focus (0.0 - 2.0)
- **📊 Token Limit** - Control response length (10 - 2000 tokens)
- **📝 Model Selection** - Choose from all your installed Ollama models
- **💾 Multiple Export Formats** - Save as .txt or .docx (Word)
- **🖥️ Modern UI** - Clean, responsive interface with sidebar controls

---

## 📋 Requirements

### System Requirements
- **Python 3.8+**
- **Ollama** installed and running locally
- **Operating System**: Windows, macOS, or Linux

### Python Dependencies
```
PyQt5>=5.15.0
requests>=2.28.0
python-docx>=0.8.11  # Optional, for .docx support
```

---

## 🚀 Installation

### 1. Install Ollama

First, ensure Ollama is installed and running on your system:


**Windows/macOS:**
```bash
# Download from https://ollama.ai
# Then pull a model
ollama pull thewindmom/hermes-3-llama-3.1-8b
```

**Linux:**
```bash
curl -fsSL https://ollama.ai/install.sh | sh
ollama pull thewindmom/hermes-3-llama-3.1-8b
```

### 2. Clone the Repository

```bash
git clone [https://github.com/yourusername/ai-writer.git](https://github.com/Laszlobeer/AI-Writer.git)
cd ai-writer
```

### 3. Create Virtual Environment (Recommended)

```bash
python -m venv venv

# Windows
venv\Scripts\activate

# macOS/Linux
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

Or install manually:
```bash
pip install PyQt5 requests python-docx
```

---

## 🎯 Usage

### Starting the Application

```bash
python ai writer.py
```

### Basic Workflow

1. **Select a Model** - Click the model dropdown and choose an installed Ollama model
2. **Write Your Text** - Start typing in the editor
3. **Click Generate** - Press the ✨ Generate button or use keyboard shortcut
4. **Save Your Work** - Export as .txt or .docx

### Controls

| Control | Description |
|---------|-------------|
| 🌙/☀️ | Toggle Light/Dark theme |
| 🔄 | Refresh available models |
| ✨ Generate | Trigger AI completion |
| 📄 Save .txt | Export as text file |
| 📕 Save .docx | Export as Word document |
| 🌡️ Temperature | Adjust creativity (left=focused, right=creative) |
| 📊 Token Limit | Set maximum response length |

---

## ⚙️ Configuration

### Default Settings

| Setting | Default Value | Description |
|---------|--------------|-------------|
| Temperature | 0.7 | Balance between creativity and coherence |
| Token Limit | 2000 | Maximum tokens in AI response |
| Ollama URL | http://localhost:11434 | Local Ollama server endpoint |

### Customizing Settings

You can modify default values in the source code (`ai_writer.py`):

```python
# In ai_writer.py
OLLAMA_URL = "http://localhost:11434"
DEFAULT_TOKEN_LIMIT = 140
DEFAULT_TEMPERATURE = 0.7
```

### Temperature Guide

- **0.0 - 0.5** 🎯 Focused, deterministic output
- **0.5 - 1.0** ⚖️ Balanced creativity and coherence
- **1.0 - 2.0** 🎨 Highly creative, unpredictable output



---

## 🖼️ Screenshots

### Light Mode
![Light Mode](lightmode.PNG)

### Dark Mode
![Dark Mode](darkmode.PNG)



---

## 🔧 Troubleshooting

### Ollama Connection Error
```
Cannot connect to Ollama. Is it running?
```
**Solution:** Ensure Ollama service is running:
```bash
ollama serve
```

### No Models Found
```
No models available
```
**Solution:** Pull a model:
```bash
ollama run thewindmom/hermes-3-llama-3.1-8b
```

### python-docx Not Available
```
install python-docx for .docx
```
**Solution:** Install the package:
```bash
pip install python-docx
```

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- [Ollama](https://ollama.ai) - Local LLM infrastructure
- [PyQt5](https://www.riverbankcomputing.com/software/pyqt/) - GUI framework

---




