\# 🤖 Web Scraper + AI Summarizer



My first LLM Engineering project! This tool automatically scrapes websites and uses local AI (Ollama) to summarize the content.



\## ✨ Features



\- 🕷️ Scrapes any public website automatically

\- ✂️ Extracts clean text from messy HTML

\- 🤖 AI-powered summarization using Ollama (runs locally!)

\- ⚠️ Smart error handling for blocked websites

\- 📊 Character count tracking

\- 🔒 Privacy-focused (all AI runs on your computer)



\## 🛠️ Prerequisites



Before you start, make sure you have:



\- Python 3.8 or higher

\- Git installed

\- Ollama installed (\[Download here](https://ollama.ai))



\## 📦 Installation



\### Step 1: Clone the Repository



```bash

git clone git@github.com:Dikshya0515/web-scraper-ai-project.git

cd web-scraper-ai-project

```



\### Step 2: Install Python Dependencies



```bash

pip install requests beautifulsoup4 ollama

```



\### Step 3: Install and Start Ollama



1\. Download Ollama from \[ollama.ai](https://ollama.ai)

2\. Install it on your system

3\. Pull the AI model:



```bash

ollama pull llama3.2:1b

```



4\. Start Ollama (if not running):



```bash

ollama serve

```



\## 🚀 Usage



\### Open the Jupyter Notebook



```bash

jupyter notebook

```



Then open `my first AI project.ipynb` (or your notebook name)



\### Run the Scraper



```python

\# Example 1: Scrape and summarize a website

scrape\_and\_summarize("https://techcrunch.com")



\# Example 2: Scrape Wikipedia

scrape\_and\_summarize("https://en.wikipedia.org/wiki/Artificial\_intelligence")



\# Example 3: Test with simple site

scrape\_and\_summarize("https://example.com")

```



\## 📋 How It Works



1\. \*\*Fetches Website\*\* - Downloads the HTML content

2\. \*\*Extracts Text\*\* - Uses BeautifulSoup to remove HTML tags

3\. \*\*Trims Content\*\* - Limits to 1000 characters for AI processing

4\. \*\*AI Summarization\*\* - Sends to Ollama (llama3.2:1b model)

5\. \*\*Returns Summary\*\* - Displays clean, concise summary



\## 🔧 Configuration



\### Change AI Model



Edit the model name in the notebook:



```python

response = ollama.generate(

&nbsp;   model='llama3.2:latest',  # Change this

&nbsp;   prompt=f"Summarize this: {text}"

)

```



\### Adjust Text Length



Change the character limit:



```python

text = text\[:2000]  # Increase from 1000 to 2000

```



\### Add Custom Headers



For websites that block scrapers:



```python

headers = {

&nbsp;   'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36'

}

response = requests.get(url, headers=headers, timeout=10)

```



\## 🐛 Troubleshooting



\### Error: "model 'llama3.2:1b' not found"

\*\*Solution:\*\* Pull the model first

```bash

ollama pull llama3.2:1b

```



\### Error: "Status code 403"

\*\*Solution:\*\* Website is blocking you. Add User-Agent headers (see Configuration section)



\### Error: "Connection refused on port 11434"

\*\*Solution:\*\* Start Ollama server

```bash

ollama serve

```



\### Error: "Module not found"

\*\*Solution:\*\* Install missing packages

```bash

pip install requests beautifulsoup4 ollama

```



\## 📚 Project Structure



```

web-scraper-ai-project/

│

├── my first AI project.ipynb    # Main Jupyter notebook

├── README.md                     # This file

├── .gitignore                    # Git ignore rules

└── .git/                         # Git repository data

```



\## 🎯 Future Improvements



\- \[ ] Add support for multiple websites at once

\- \[ ] Save summaries to a file

\- \[ ] Create a simple web interface

\- \[ ] Add different summarization styles

\- \[ ] Support for PDFs and documents

\- \[ ] Create a command-line version



\## 🤝 Contributing



Feel free to fork this project and submit pull requests!



1\. Fork the repository

2\. Create your feature branch (`git checkout -b feature/AmazingFeature`)

3\. Commit your changes (`git commit -m 'Add some AmazingFeature'`)

4\. Push to the branch (`git push origin feature/AmazingFeature`)

5\. Open a Pull Request



\## 📝 License



This project is open source and available under the \[MIT License](LICENSE).



\## 👩‍💻 Author



\*\*Dikshya Khadka\*\*



\- GitHub: \[@Dikshya0515](https://github.com/Dikshya0515)

\- Project: \[web-scraper-ai-project](https://github.com/Dikshya0515/web-scraper-ai-project)



\## 🙏 Acknowledgments



\- \[Ollama](https://ollama.ai) for providing local AI models

\- \[BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/) for HTML parsing

\- \[Requests](https://requests.readthedocs.io/) for HTTP requests



\## 📧 Contact



Have questions or suggestions? Feel free to open an issue on GitHub!



---



⭐

