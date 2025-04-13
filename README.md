# Summary

This repository demonstrates approaches to maintaining conversation history for context-aware responses in Large Language Models (LLMs). It compares the traditional Chat Completions API with OpenAI's Responses API, highlighting their trade-offs in terms of memory retention, token usage, and cost.

## Key Insights

- **User Expectations**: Users expect LLMs to retain conversation history for context-aware responses.  
- **Chat Completions API**: Achieves memory by appending past exchanges to the context window, but incurs higher token costs as conversations grow longer.  
- **Responses API**: Simplifies memory retention using `previous_response_id`, reducing boilerplate code but still incurring costs as the number of prompts increases.  
- **Alternative Approach**: A Retrieval-Augmented Generation (RAG) system can embed and retrieve relevant interactions, avoiding full conversation replay.

## Repository Contents

- **Code Examples**: Demonstrates both Chat Completions API and Responses API with memory retention.  
- **Token Usage Analysis**: Visualizes token usage over conversations for both APIs.  
- **Comparative Analysis**: Highlights the trade-offs between the two approaches.  

## Getting Started

1. Install dependencies:
    ```bash
    pip install python-dotenv
    pip install --upgrade openai
    ```

2. Set up your `.env` file with your `OPENAI_API_KEY`.

3. Run the provided scripts to explore memory retention techniques and analyze token usage.

## Conclusion

While the Responses API reduces boilerplate code, enterprises should consider cost implications as conversations grow longer. A RAG system may offer a more scalable solution for maintaining context without replaying entire conversation histories.

