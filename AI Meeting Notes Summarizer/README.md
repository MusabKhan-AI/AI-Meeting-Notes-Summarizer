# AI Meeting Notes Summarizer for a Real Estate Agency

## Project Overview

This project is a working prototype of an AI Meeting Notes Summarizer for a real estate agency.

The system uses Retrieval-Augmented Generation (RAG) to retrieve relevant information from meeting notes and generate answers to user questions.

## My Role

Member 6 – Vector Database

## Technologies Used

- Python
- Sentence Embeddings
- FAISS
- NumPy
- Groq LLM
- Gradio
- Google Colab

## How It Works

Meeting Notes
↓
Text Chunks
↓
Embeddings
↓
FAISS Vector Database
↓
User Question
↓
Question Embedding
↓
Similarity Search
↓
Relevant Meeting Information
↓
Groq LLM
↓
Final Answer
↓
Gradio Interface

## Vector Database

The meeting notes were divided into 19 text chunks.

Each chunk was converted into a 384-dimensional embedding.

The embeddings were stored in a FAISS IndexFlatL2 vector index.

Total vectors stored: 19.

## Testing

The system was tested using 10 questions based on the sample real estate meeting data.

Result:

10/10 test cases passed on the sample test set.

Sample question:

"Where does Sara Ahmed want a property?"

Answer:

"Lahore"

## Error Handling

The system checks for empty questions and returns a message asking the user to enter a valid question.

## Challenges

One challenge was selecting an available Groq model. The initially selected model was unavailable, so an available model, `openai/gpt-oss-20b`, was used.

Another challenge occurred when one question produced an incomplete answer. The test question was made more precise to clearly ask for both the location and facility.

## Conclusion

The prototype successfully demonstrates semantic search using FAISS and answer generation using a Groq LLM. The Gradio interface provides a simple way for users to ask questions about the meeting information.
