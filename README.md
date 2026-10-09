# HomeMatch: AI Real Estate Agent

An AI agent that recommends apartments and houses based on a user's preferences. It generates realistic listings with an LLM, stores them in a Chroma vector database, interviews the user about what they are looking for, and returns personalized recommendations.

## How it works

1. Generate realistic apartment listings with an LLM and save them to `Listings.txt`.
2. Load the listings into a Chroma vector database with OpenAI embeddings.
3. Capture the user's preferences: either through LLM-generated follow-up questions or a manual Q&A list.
4. Summarize the conversation into a query describing the user's preferences.
5. Retrieve the top 5 semantically similar listings from the database.
6. Rewrite each listing description to emphasize how it matches the user's preferences.

## Repo structure

- `HomeMatch.ipynb` - the full walkthrough, from listing generation to personalized recommendations.
- `Listings.txt` - pre-generated sample listings so the notebook can run without regenerating them.
- `requirements.txt` - Python dependencies.

## How to run

1. Install dependencies: `pip install -r requirements.txt`
2. Set your OpenAI API key as an environment variable (required; the notebook raises a clear error if it is missing):
   ```
   export OPENAI_API_KEY="your-key-here"
   ```
   If you use an OpenAI-compatible proxy instead of the official API, also set `OPENAI_API_BASE`.
3. Open `HomeMatch.ipynb` and run the cells in order.

## What you learn

- Prompt engineering for structured text generation (listings with a fixed schema).
- Storing and searching documents with a vector database (Chroma + OpenAI embeddings).
- Building a simple preference-elicitation loop with LangChain.
- Retrieval-augmented personalization: grounding LLM rewrites in real listing facts.
