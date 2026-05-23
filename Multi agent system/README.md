# Multi-Agent AI Research System with LangChain

A sophisticated multi-agent system that automates research by combining web search, content scraping, AI-powered writing, and critical evaluation. Built with LangChain, Google Gemini, and LangGraph.

## Features

- **🔍 Search Agent**: Finds recent, reliable, and detailed information on any topic using web search
- **📖 Reader Agent**: Scrapes and extracts content from relevant URLs for deeper analysis
- **✍️ Writer Agent**: Generates well-structured, professional research reports
- **🧠 Critic Agent**: Reviews and scores reports with constructive feedback

## Architecture

The system follows a multi-step pipeline:

1. **Search Phase**: The search agent queries the web using Tavily Search API
2. **Scraping Phase**: The reader agent extracts content from the most relevant URLs
3. **Report Generation**: The writer chain synthesizes information into a structured report
4. **Evaluation**: The critic chain reviews the report and provides scoring and feedback

## Requirements

- Python 3.11+
- Google Gemini API key
- Tavily Search API key

## Installation

1. Clone the repository:

```bash
git clone https://github.com/panavkumar717/Multi-Agent-AI-Research-System-with-LangChain.git
cd Multi-Agent-AI-Research-System-with-LangChain
```

2. Create a virtual environment:

```bash
python -m venv .venv
.venv\Scripts\activate  # Windows
source .venv/bin/activate  # macOS/Linux
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Set up environment variables in `.env`:

```
GEMINI_API_KEY=your_gemini_api_key
TAVILY_API_KEY=your_tavily_api_key
```

## Usage

Run the pipeline:

```bash
python pipeline.py
```

Enter a research topic when prompted, and the system will:

1. Search for information
2. Scrape relevant content
3. Generate a comprehensive report
4. Provide critical feedback

Example:

```
Enter a research topic: Artificial Intelligence in Healthcare
```

## Project Structure

```
├── agents.py          # Agent and chain definitions
├── pipeline.py        # Main pipeline execution
├── tools.py           # Tool definitions (search, scraping)
├── requirements.txt   # Python dependencies
├── .env               # Environment variables (API keys)
└── README.md          # This file
```

## Components

### Agents

- **Search Agent**: Uses Tavily Search tool to find relevant information
- **Reader Agent**: Uses web scraping to extract detailed content

### Chains

- **Writer Chain**: Structured prompt that generates research reports
- **Critic Chain**: Evaluates reports on quality, strengths, and areas for improvement

### Tools

- **Web Search**: Finds recent information on any topic
- **URL Scraping**: Extracts content from web pages

## Dependencies

- `langchain` - LLM framework
- `langchain-google-genai` - Google Gemini integration
- `langchain-community` - Community integrations
- `langgraph` - Multi-agent orchestration
- `google-generativeai` - Google Gemini SDK
- `tavily-python` - Web search API
- `beautifulsoup4` - Web scraping
- `requests` - HTTP library
- `python-dotenv` - Environment variable management

## API Keys

You'll need:

1. **Google Gemini API Key**: Get from [Google AI Studio](https://ai.google.dev)
2. **Tavily Search API Key**: Get from [Tavily](https://tavily.com)

## Output Example

The system generates output with:

- **Search Results**: Raw search findings
- **Scraped Content**: Detailed content from selected URLs
- **Research Report**: Structured report with introduction, key findings, and conclusion
- **Critic Feedback**: Score (0-10), strengths, and areas for improvement

## Limitations

- Free tier API quotas may limit requests per day
- Web scraping depends on website structure and robots.txt
- Report quality depends on search result quality

## Future Enhancements

- Add support for academic database searches
- Implement caching for frequently researched topics
- Add PDF report generation
- Support multiple language outputs
- Implement fact-checking against reliable sources

## Contributing

Feel free to fork, improve, and submit pull requests!

## License

This project is open source and available under the MIT License.

## Author

Created by [Panav Kumar](https://github.com/panavkumar717)

---

For issues and feature requests, please open an issue on GitHub.
