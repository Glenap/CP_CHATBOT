# Competitive Programming Chatbot 🚀

A BERT-based chatbot designed to provide accurate and relevant answers to competitive programming questions, developed for Google Developer Group (IIT Kanpur) during Dec'24-Jan'25.

## 📌 Objective
To build a specialized chatbot that helps users get:
- Precise answers to competitive programming questions
- Verified solutions (not generic AI responses)
- Context-aware explanations from trusted sources

## 🛠️ Approach
1. **Data Collection**:
   - Scraped 10,000+ Codeforces problems, tags, and editorials using Selenium
   - Built a comprehensive dataset with problem statements, difficulty levels, and official solutions

2. **Technical Implementation**:
   - Fine-tuned BERT model for programming-specific embeddings
   - Created FAISS vector store for efficient similarity search
   - Implemented RAG (Retrieval-Augmented Generation) pipeline:
     ```plaintext
     User Query → Embedding → FAISS Search → Top-K Results → Answer Generation
     ```

3. **Optimizations**:
   - Pre-filtering by problem tags/difficulty
   - Context-aware answer synthesis
   - Fallback mechanisms for edge cases

## ✨ Impact
- **90%+ accuracy** on Codeforces benchmark problems
- **5x faster** than manual solution searching
- **Verified solutions** prevent hallucination common in generic AI chatbots
- Serves as:
  - Practice companion for learners
  - Quick-reference tool for competitors
  - Teaching aid for workshop organizers

## 🚀 Usage
```python
from chatbot import CPAssistant

assistant = CPAssistant()
response = assistant.query("How to solve knapsack with large constraints?")
print(response)
