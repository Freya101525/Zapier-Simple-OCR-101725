# 🤖 Agentic PDF Processing System

A beautiful, intelligent PDF processing system powered by multiple AI agents (Gemini, OpenAI, Grok) with OCR capabilities and stunning themed UI.

## ✨ Features

- 🎨 **8 Beautiful Themes**: Blue Sky, Snow White, Deep Ocean, Sparkling Galaxy, Alp Forest, Flora, Ferrari, Fendi Casa
- 🤖 **Multi-Agent AI Processing**: Leverages Gemini, OpenAI, and Grok APIs
- 📄 **Advanced PDF Processing**: Text extraction, OCR support, page range selection
- 🔍 **Keyword Highlighting**: Automatically highlights important terms
- 📊 **Multiple Analysis Types**: Summarization, extraction, translation, sentiment analysis
- 💾 **Export Results**: Download processed results as text files
- 🚀 **Real-time Processing**: See your documents transform in real-time

## 🚀 Quick Start for Hugging Face Spaces

### 1. Create a New Space

1. Go to [Hugging Face Spaces](https://huggingface.co/spaces)
2. Click "Create new Space"
3. Choose **Streamlit** as the SDK
4. Name your space (e.g., `pdf-agent-processor`)

### 2. Upload Files

Upload these files to your space:
- `app.py` (main application)
- `agents.yaml` (agent configurations)
- `requirements.txt` (dependencies)
- `README.md` (this file)
- `packages.txt` (system packages - see below)

### 3. Create `packages.txt`

Create a file named `packages.txt` with these system dependencies:

```
poppler-utils
tesseract-ocr
tesseract-ocr-eng
tesseract-ocr-chi-tra
```

### 4. Set Up Secrets

In your Space settings, add these secrets:

```
GEMINI_API_KEY=your_gemini_api_key_here
OPENAI_API_KEY=your_openai_api_key_here
GROK_API_KEY=your_xai_api_key_here
```

**Getting API Keys:**

- **Gemini**: Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
- **OpenAI**: Visit [OpenAI Platform](https://platform.openai.com/api-keys)
- **Grok**: Visit [xAI Console](https://console.x.ai/)

### 5. Deploy

Your space will automatically build and deploy! 🎉

## 🎨 Available Themes

1. **Blue Sky** - Calm and professional sky-inspired design
2. **Snow White** - Clean, minimalist white elegance
3. **Deep Ocean** - Dark, mysterious underwater aesthetic
4. **Sparkling Galaxy** - Vibrant purple and pink cosmic theme
5. **Alp Forest** - Fresh green nature-inspired design
6. **Flora** - Feminine pink and purple floral style
7. **Ferrari** - Bold red racing-inspired theme
8. **Fendi Casa** - Luxurious gold and beige sophistication

## 🤖 Available AI Agents

1. **Document Summarizer** - Creates comprehensive summaries
2. **Key Information Extractor** - Extracts dates, names, numbers, and action items
3. **Question Generator** - Generates comprehension and critical thinking questions
4. **Translation Assistant** - Detects language and translates content
5. **Sentiment & Tone Analyzer** - Analyzes emotional content and tone
6. **Action Item Generator** - Creates actionable task lists
7. **Content Quality Checker** - Evaluates document quality and clarity
8. **Comparative Analyzer** - Identifies contrasts and synthesizes perspectives

## 📝 Usage Instructions

1. **Select Your Theme**: Choose from 8 beautiful themes in the sidebar
2. **Choose AI Provider**: Select Gemini, OpenAI, or Grok
3. **Select Model**: Pick the specific model variant
4. **Upload PDF**: Drop your PDF file in the upload area
5. **Configure Options**:
   - Select specific page ranges (optional)
   - Enable OCR for scanned documents
   - Add keywords to highlight
6. **Process**: Click "🚀 Process PDF with AI"
7. **Review Results**: Expand each agent's results
8. **Download**: Save individual agent outputs

## 🛠️ Local Development

```bash
# Clone the repository
git clone <your-space-url>
cd <your-space-name>

# Install dependencies
pip install -r requirements.txt

# Install system packages (Ubuntu/Debian)
sudo apt-get update
sudo apt-get install -y poppler-utils tesseract-ocr

# Set environment variables
export GEMINI_API_KEY="your_key_here"
export OPENAI_API_KEY="your_key_here"
export GROK_API_KEY="your_key_here"

# Run the app
streamlit run app.py
```

## 🔧 Customization

### Adding New Agents

Edit `agents.yaml` to add custom agents:

```yaml
- name: "Your Custom Agent"
  api: "Gemini"  # or OpenAI, Grok
  model: "gemini-2.5-flash"
  prompt: |
    Your custom prompt here with {input_text} placeholder
  parameters:
    temperature: 0.7
    max_tokens: 1500
```

### Creating New Themes

Add to the `THEMES` dictionary in `app.py`:

```python
"Your Theme": {
    "primary": "#HEX_COLOR",
    "secondary": "#HEX_COLOR",
    "background": "#HEX_COLOR",
    "text": "#HEX_COLOR",
    "accent": "#HEX_COLOR"
}
```

## 📊 Supported Models

### Gemini Models
- gemini-2.5
