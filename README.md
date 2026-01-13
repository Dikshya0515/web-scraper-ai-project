cat > README.md << 'EOF'
# 🌐 Website Summarizer with OpenAI

An intelligent Python-based tool that automatically fetches website content and generates concise summaries using OpenAI's GPT-3.5-turbo model.

![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--3.5-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

## ✨ Features

- 📡 Fetches content from any public website
- 🤖 AI-powered summaries using OpenAI GPT-3.5-turbo
- 🔒 Secure API key management with `.env` file
- 📊 Handles both single and multiple website summarization
- 🧹 Automatic text cleaning and preprocessing
- ⚡ Fast and efficient with proper error handling

## 🛠️ Technologies Used

- **Python 3.x**
- **OpenAI API** - For generating summaries
- **BeautifulSoup4** - For web scraping
- **Requests** - For HTTP requests
- **python-dotenv** - For environment variable management

## 📋 Prerequisites

- Python 3.7 or higher
- OpenAI API key ([Get one here](https://platform.openai.com/api-keys))
- Active OpenAI account with credits/billing set up

## 🚀 Installation

1. **Clone the repository:**
```bash
git clone https://github.com/Dikshya0515/web-scraper-ai-project.git
cd web-scraper-ai-project
```

2. **Install required packages:**
```bash
pip install openai requests beautifulsoup4 python-dotenv
```

Or in Jupyter notebook:
```python
!pip install openai requests beautifulsoup4 python-dotenv
```

3. **Set up your API key:**

Create a `.env` file in the project root:
```bash
echo "OPENAI_API_KEY=your-api-key-here" > .env
```

**⚠️ IMPORTANT:** Never commit your `.env` file to GitHub! It's already in `.gitignore`.

## 💻 Usage

### **Using Jupyter Notebook**

Open `my first AI project.ipynb` and run the cells in order:

1. **Cell 1:** Install packages (run once)
2. **Cell 2:** Create `.env` file (run once, then comment out)
3. **Cell 3:** Load the main code with functions
4. **Cell 4:** Test with a single website
5. **Cell 5:** Test with multiple websites

### **Example: Single Website**
```python
url = "https://en.wikipedia.org/wiki/Artificial_intelligence"
summary = website_summarizer(url)
```

### **Example: Multiple Websites**
```python
websites = [
    "https://en.wikipedia.org/wiki/Python_(programming_language)",
    "https://en.wikipedia.org/wiki/Machine_learning",
    "https://en.wikipedia.org/wiki/Data_science"
]

for url in websites:
    website_summarizer(url)
    print("\n\n")
```

## 📖 Example Output
```
======================================================================
                    WEBSITE SUMMARIZER
======================================================================

📡 Fetching content from https://en.wikipedia.org/wiki/Artificial_intelligence...
✓ Fetched 212374 characters

⚠️ Text truncated to 3000 characters
🤖 Generating summary with OpenAI...
✓ Summary generated!

======================================================================
                            SUMMARY
======================================================================

Artificial Intelligence (AI) refers to the simulation of human 
intelligence in machines programmed to think and learn like humans. 
The field encompasses machine learning, natural language processing, 
robotics, and computer vision...

======================================================================
```

## 🔧 Configuration

Customize the summarization by modifying parameters in `summarize_text()`:
```python
def summarize_text(text, max_length=3000):
    # Adjust these parameters:
    max_length = 3000        # Max characters to process
    max_tokens = 300         # Max tokens in summary
    temperature = 0.5        # Creativity (0-1)
    model = "gpt-3.5-turbo"  # OpenAI model
```

## 🐛 Troubleshooting

| Error | Cause | Solution |
|-------|-------|----------|
| **403 Forbidden** | Website blocking requests | Code includes User-Agent headers ✅ |
| **429 Insufficient Quota** | No OpenAI credits | Add billing at [platform.openai.com](https://platform.openai.com/account/billing) |
| **API Key Not Found** | Missing `.env` file | Create `.env` with `OPENAI_API_KEY=your-key` |
| **Import Error** | Missing packages | Run `pip install` command again |

## 💰 Cost Estimate

Using GPT-3.5-turbo:
- Single website summary: **~$0.001 - $0.01** (less than 1 cent)
- 100 summaries: **~$0.10 - $1.00**

Very affordable for regular use! 💵

## 📁 Project Structure
```
web-scraper-ai-project/
│
├── my first AI project.ipynb    # Main Jupyter notebook
├── .env                          # API keys (NOT committed)
├── .gitignore                    # Git ignore file
├── README.md                     # Documentation
└── requirements.txt              # Dependencies
```

## 🤝 Contributing

Contributions are welcome! Here's how:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

**Dikshya**
- GitHub: [@Dikshya0515](https://github.com/Dikshya0515)

## 🙏 Acknowledgments

- OpenAI for providing the GPT API
- BeautifulSoup4 for web scraping capabilities
- The Python community for excellent libraries

## ⚠️ Disclaimer

This tool is for educational purposes. Always respect:
- Website terms of service
- robots.txt files
- Rate limits and API costs
- Data privacy and copyright laws

## 🚀 Future Enhancements

- [ ] Add support for PDF summarization
- [ ] Implement caching to reduce API costs
- [ ] Add GUI interface
- [ ] Support for other AI models (Claude, Gemini)
- [ ] Batch processing with progress bars
- [ ] Export summaries to PDF/DOCX

---

**Made with ❤️ and Python**

⭐ Star this repo if you found it helpful!
EOF