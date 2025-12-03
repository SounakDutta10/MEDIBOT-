# Medical-Chatbot — README

📁 Project Structure
Medical-Chatbot/
│
├── medibot.py                     # Main chatbot runner
├── create_memory_for_llm.py       # Script to generate vector embeddings
├── connect_memory_with_llm.py     # Script linking chatbot with vector memory
│
├── data/                          # Raw data files for vector memory
├── vectorstore/                   # Saved embeddings / FAISS/Chroma DB
│
├── .env                           # Environment variables (API keys etc.)
├── requirements.txt               # Python dependencies
├── run.txt                        # Notes / run instructions (internal)
├── LICENSE
└── .gitignore

🚀 Features

✅ LLM-powered medical query responses

✅ Vector-based memory system for factual context

✅ Persistent vectorstore for faster retrieval

✅ Modular architecture (separate scripts for memory creation, connection, and chatbot execution)

✅ Environment-based configuration

✅ Works with OpenAI / Groq / other LLM providers depending on .env configuration

🔧 Installation
1. Clone the repository
git clone <your-repo-url>
cd Medical-Chatbot

2. Create a virtual environment
python -m venv venv
source venv/bin/activate        # Linux / macOS
venv\Scripts\activate           # Windows

3. Install dependencies
pip install -r requirements.txt

🔑 Environment Variables

Create a .env file (already present) and include:

OPENAI_API_KEY=your_api_key
MODEL_NAME=gpt-4 / gpt-4o / llama3 etc.
VECTOR_STORE_PATH=./vectorstore


Adjust values based on your provider and setup.

🧠 Creating Vector Memory

Before running the bot, you must generate the vector embeddings from the data/ folder.

Run:

python create_memory_for_llm.py


This will:

Process files in data/

Generate embeddings

Save them into vectorstore/

🔗 Connecting the LLM with Memory

To test the memory integration:

python connect_memory_with_llm.py


This script verifies:

Vector store loading

Query + retrieval accuracy

Response quality from LLM

🤖 Running the Medical Chatbot

Start the main chatbot interface:

python medibot.py


Features include:

Natural conversation

Medical question answering

Retrieval-augmented responses

Contextual replies based on stored vector knowledge

📌 Notes

The bot is intended for educational and informational purposes only.
It should not be used as a substitute for professional medical advice.

If you modify/update the data in data/, re-run:

python create_memory_for_llm.py

📜 License

This project is licensed under the MIT License.
See the LICENSE file for details.

## 👥 Contributors
- **Sounak Dutta (22052684)**  
- **Somraj Bose (22052682)**  
- **Ayush Sandilya (22052375)**  
