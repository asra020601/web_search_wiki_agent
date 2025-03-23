# Web Search Wiki Agent

A research assistant tool built using Langchain that leverages web search and Wikipedia APIs to help generate research responses. It uses an OpenAI chat model to process queries, call external tools, and return a structured answer containing a topic summary, sources, and details about the tools used.

## Features

- **Integrated Tools:**  
  - **DuckDuckGo Search:** Query the web for the latest information.  
  - **Wikipedia Lookup:** Retrieve summarized content from Wikipedia.  
  - **Save to File:** Save the structured research output to a text file.
- **Structured Response:**  
  Uses a Pydantic model to format the output with fields for topic, summary, sources, and tools used.
- **Langchain-Powered Agent:**  
  Utilizes Langchain's tool-calling agent framework to orchestrate the different tools in response to user queries.
- **OpenAI LLM Integration:**  
  Uses an OpenAI chat model (via the `langchain_openai` package) to generate detailed and structured research outputs.

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/asra020601/web_search_wiki_agent.git
   cd web_search_wiki_agent
   ```

2. **Install dependencies:**

   Ensure you have Python 3.7 or later installed, then install the required packages:

   ```bash
   pip install -r requirements.txt
   ```

3. **Environment Variables:**

   Create a `.env` file in the root directory to store your API keys and any other sensitive configuration (e.g., OpenAI API keys). The project uses `python-dotenv` to load these variables.

   Example `.env` file:
   ```env
   OPENAI_API_KEY=your_openai_api_key_here
   # Add other keys as needed
   ```

## Usage

To run the research assistant:

1. Open a terminal in the project directory.
2. Run the main script:

   ```bash
   python main.py
   ```

3. When prompted with:
   ```
   What can i help you research?
   ```
   enter your research query. The agent will then:
   - Use the web search tool to fetch relevant information.
   - Query Wikipedia for summaries.
   - Optionally save the research output to a text file.

4. The structured response will be printed to the console.

## File Structure

- **main.py:**  
  The main entry point for the agent. It sets up the Langchain prompt, loads the environment, and initializes the research assistant agent.
- **tools.py:**  
  Contains definitions for the integrated tools (DuckDuckGo search, Wikipedia query, and saving research output to file).
- **requirements.txt:**  
  Lists the Python packages required to run the project.

## Dependencies

This project depends on several packages including:
- **langchain** – For agent and tool orchestration.
- **wikipedia & langchain-community** – For Wikipedia queries.
- **langchain-openai** – To integrate with OpenAI’s chat models.
- **python-dotenv** – To load environment variables.
- **pydantic** – For structured response validation.
- **duckduckgo-search** – For web search functionality.

## Contributing

Contributions are welcome! If you’d like to improve the project:
1. Fork the repository.
2. Create a new branch with your feature or bug fix.
3. Submit a pull request with a clear description of your changes.

