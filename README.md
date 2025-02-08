# AI Research Assistant

An AI-powered research assistant that automatically generates comprehensive reports by searching the web, analyzing content, and synthesizing information using multiple AI services.

## Features

- 🔍 Automated web research using multiple search queries
- 📊 Content extraction and relevance analysis
- 🔄 Iterative search refinement
- 📝 Comprehensive report generation
- 📈 Real-time progress logging
- 🖥️ User-friendly Gradio interface

## Prerequisites

Before you begin, you'll need:

1. **API Keys**:
   - [OpenRouter API](https://openrouter.ai/) - For LLM access
   - [SerpAPI](https://serpapi.com/) - For web searches
   - [Jina AI](https://jina.ai/) - For web content extraction

2. **Conda** installed on your system
   - If you don't have Conda, download and install [Miniconda](https://docs.conda.io/en/latest/miniconda.html)

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/RooseveltAdvisors/OpenDeepResearcher.git
   cd OpenDeepResearcher
   ```

2. **Create and activate the Conda environment**:
   ```bash
   conda env create -f environment.yml
   conda activate jon-open-deep-researcher
   ```

3. **Set up environment variables**:
   ```bash
   # Copy the example environment file
   cp .env.example .env
   ```
   
   Then edit `.env` with your API keys:
   ```env
   OPENROUTER_API_KEY=your_openrouter_api_key_here
   SERPAPI_API_KEY=your_serpapi_api_key_here
   JINA_API_KEY=your_jina_api_key_here
   ```

## Usage

1. **Start the application**:
   ```bash
   python research_assistant.py
   ```

2. **Access the interface**:
   - Open your web browser
   - Navigate to `http://localhost:7860`
   - The interface will also be printed in your terminal

3. **Using the interface**:
   - Enter your research query in the text box
   - Adjust the maximum number of iterations if needed (default: 10)
   - Click "Submit" to start the research process
   - View the generated report and research logs

## How It Works

1. **Query Analysis**: 
   - The system analyzes your query and generates targeted search queries

2. **Iterative Research**:
   - Performs web searches using generated queries
   - Extracts and analyzes content from search results
   - Evaluates relevance of found information
   - Generates new search queries based on findings

3. **Report Generation**:
   - Synthesizes gathered information
   - Generates a comprehensive, well-structured report

## Troubleshooting

### Common Issues

1. **Environment Setup**:
   ```bash
   # If you see conda environment errors:
   conda deactivate
   conda env remove -n jon-open-deep-researcher
   conda env create -f environment.yml
   ```

2. **API Issues**:
   - Verify your API keys in the `.env` file
   - Check API rate limits and quotas
   - Ensure your API keys have the necessary permissions

3. **Runtime Errors**:
   - Make sure all environment variables are set correctly
   - Check your internet connection
   - Verify Python version compatibility (3.8+)

### Getting Help

If you encounter issues:
1. Check the error message in the terminal
2. Review the logs in the Gradio interface
3. Verify all API keys are valid and have sufficient credits

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Security Notes

- Never commit your `.env` file to version control
- Keep your API keys secure and rotate them regularly
- Monitor your API usage to stay within limits

## License

This project is licensed under the MIT License - see the LICENSE file for details.
