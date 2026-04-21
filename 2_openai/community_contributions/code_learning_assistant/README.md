# 📚 AI Code Learning Assistant

An intelligent AI-powered system that helps you **learn**, **understand**, and **document** code in any programming language. Built with OpenAI's Agents SDK and Gradio.

![Python](https://img.shields.io/badge/python-3.9+-blue.svg)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4o-green.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## 🌟 Features

### 🎓 Language Learning
- **Deep concept explanations** with real code examples
- **Analogies and comparisons** to other languages (Python, JavaScript, etc.)
- **Common pitfalls** and best practices
- **Pro tips** from experienced developers

### 🔍 Code Understanding
- **Step-by-step walkthroughs** of how code works
- **Data flow visualization** (input → process → output)
- **Design decision explanations** (the "why" behind the code)
- **Big picture context** before diving into details

### 📝 Documentation Generation
- **PR-ready documentation** with structured sections
- **Technical implementation** details
- **Testing strategies** and risk assessment
- **Alternative approaches** considered

### 📜 Git History Analysis
- **Commit history** showing file evolution over time
- **Diff analysis** with line-by-line change breakdown
- **Connect commits to code** - understand WHY changes were made
- **Development patterns** and team collaboration insights

## 🚀 Quick Start

### Prerequisites

- Python 3.9+
- OpenAI API key
- Git (for history analysis features)

### Installation

1. **Clone the repository:**
```bash
git clone https://github.com/gkeskar/gen-ai.git
cd gen-ai
```

2. **Install dependencies:**
```bash
pip install -r requirements.txt
```

3. **Set up environment variables:**

Create a `.env` file in your project root directory:
```bash
OPENAI_API_KEY=your_openai_api_key_here

# Optional: Use a custom OpenAI gateway (defaults to https://api.openai.com/v1)
# OPENAI_BASE_URL=https://your-custom-gateway.com/v1
```

> 💡 The application automatically searches upward from its location to find the `.env` file, so it works from any directory structure.

### Usage

1. **Start the application:**
```bash
python code_assistant.py
```

2. **Open your browser:**
Navigate to `http://127.0.0.1:7860`

3. **Analyze code:**
   - Enter the file path (relative or absolute)
   - Optionally add a task description
   - Check "Git Diff" to see what changed
   - Check "Commit History" to see how the file evolved
   - Click "🚀 Analyze Code"

## 📖 Example Usage

### Learning a New Language

**Scenario:** You're a Python developer learning Ruby

```
File Path: /path/to/ruby/orchestrator.rb
Task Description: Understanding Ruby ETL pipeline implementation
Options: ☐ Git Diff  ☐ Commit History
```

**Output includes:**
- Ruby language concepts explained with Python comparisons
- How classes, modules, and instance variables work
- Common Ruby patterns and idioms
- Detailed code walkthrough

### Documenting for Pull Requests

**Scenario:** You need to create PR documentation

```
File Path: app/services/payment_processor.py
Task Description: Added Stripe payment integration
Options: ☑ Git Diff  ☐ Commit History
```

**Output includes:**
- Summary of changes
- Technical implementation details
- Testing recommendations
- Risk assessment

### Understanding Code Evolution

**Scenario:** Understanding how a critical file evolved

```
File Path: core/authentication.js
Task Description: Review authentication system changes
Options: ☑ Git Diff  ☑ Commit History
```

**Output includes:**
- Timeline of how the file changed
- Key development milestones
- Why changes were made (from commit messages)
- Recent diff analysis with historical context

## 🏗️ Architecture

### Modular Design

```
code_learning_assistant/
├── code_assistant.py          # Gradio UI
├── learning_manager.py        # Orchestration logic
├── specialist_agents.py       # AI agent definitions
├── tools.py                   # File reading, git, saving tools
├── test_modules.py           # Module testing script
├── test_simple.py            # Simple validation script
└── learning_docs/            # Generated documentation
```

### AI Agents

1. **Documentation Manager** - Orchestrates the entire analysis
2. **Language Teacher** - Explains programming concepts in depth
3. **Code Explainer** - Breaks down how code works step-by-step
4. **Change Documenter** - Creates PR-ready documentation
5. **Git Diff Analyzer** - Analyzes code changes and history

### Technologies

- **OpenAI Agents SDK** - Multi-agent orchestration
- **GPT-4o** - High-quality analysis and explanations
- **Gradio** - Beautiful web interface
- **Python asyncio** - Concurrent agent execution

## 🎨 UI Features

- **Real-time status updates** - See what's happening as agents work
- **Clean markdown rendering** - Beautiful formatted output
- **File download** - Save documentation with timestamps
- **Professional theme** - Modern, responsive design
- **Error handling** - Helpful error messages with tips

## 📊 Output Quality

The AI agents are configured to provide **high-quality, detailed output**:

### Language Teacher
- ✅ Minimum 400 words
- ✅ 8-10 code snippets with line numbers
- ✅ 5+ concepts explained in depth
- ✅ 3+ analogies
- ✅ 3+ language comparisons

### Code Explainer
- ✅ Minimum 350 words
- ✅ 10+ code snippets
- ✅ 5+ functions/methods explained
- ✅ Data flow diagrams with arrows

### Git Diff Analyzer
- ✅ Minimum 300 words
- ✅ 3+ commit messages quoted (if history enabled)
- ✅ 5+ diff blocks analyzed
- ✅ Connections between commits and changes

## 🔧 Configuration

### Environment Variables

```bash
# Required
OPENAI_API_KEY=your_api_key

# Optional (for custom OpenAI endpoint)
OPENAI_BASE_URL=https://your-gateway.com/v1
```

### Customization

**Change AI models** (`specialist_agents.py`):
```python
language_teacher = Agent(
    name="Language Teacher",
    instructions=language_teacher_instructions,
    model="gpt-4o"  # Change to gpt-4o-mini for faster/cheaper
)
```

**Adjust output requirements** (`specialist_agents.py`):
```python
QUALITY REQUIREMENTS:
- Output should be AT LEAST 400 words  # Adjust minimum
- Include MINIMUM 8-10 actual code snippets  # Change count
```

## 🧪 Testing

**Test all modules:**
```bash
python test_modules.py
```

**Simple validation:**
```bash
python test_simple.py
```

## 📝 Generated Documentation Format

```markdown
# [filename] - Learning Documentation

## 📚 Language Concepts Explained
[Deep dive into programming language features]

## 🔍 How The Code Works
[Step-by-step code walkthrough]

## 📝 Implementation Documentation
[PR-ready documentation]

## 📜 Code Evolution & History (if enabled)
[Commit history and diff analysis]
```

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 📄 License

This project is licensed under the MIT License.

## 🙏 Acknowledgments

- Built with [OpenAI Agents SDK](https://github.com/openai/openai-agents-python)
- UI powered by [Gradio](https://gradio.app/)
- Inspired by the need to make code learning more accessible

## 📧 Contact

For questions or feedback, please open an issue on GitHub.

---

**Made with ❤️ for developers learning new languages and codebases**
