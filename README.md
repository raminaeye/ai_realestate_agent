# HomeMatch: AI Real Estate Agent

A notebook that recommends homes from a buyer's preferences. An LLM writes sample listings, a Chroma vector store finds the best matches, and the LLM rewrites each match to show how it fits the buyer.

## What's inside

- `HomeMatch.ipynb` is the whole project

## How to run

```bash
pip install "langchain==0.0.305" "openai==0.28.1" "chromadb==0.4.12" tiktoken jupyter
export OPENAI_API_KEY=your-key
jupyter notebook HomeMatch.ipynb
```
