# 🐀 Tort Rat

Tort Rat is a CLI-based Discord chatbot developed as a side project for SMU's LAW105: Law of Torts course. It leverages Retrieval-Augmented Generation (RAG) to answer questions about key tort law cases and concepts. Trained on a curated set of case summaries, Tort Rat can:

![image](https://github.com/user-attachments/assets/81530b40-986b-4595-9b0c-4358f882f1db)

- 📖 Explain legal doctrines and tests;
- ⚖️ Address basic hypothetical questions; and
- 🧠 Provide concise answers to enhance legal understanding.

## 🛠 Technical Details
- Built using PostgresML and Python

## 🚀 Setup

```sh
pip install pgml-chat
python -m venv {file_path}
```

Clone the `.env` and `ingest` folder from the repository:

```sh
git clone https://github.com/kevanwee/tortrat.git
```

Edit the `.env` file and add the OpenAI API key, PostgresML database link, and Discord bot token:

```sh
OPENAI_API_KEY=<>
DATABASE_URL=<>
DISCORD_BOT_TOKEN=<>
```

## 📥 Data Ingestion

To ingest data, run:

```sh
LOG_LEVEL=DEBUG pgml-chat --root_dir ingest --collection_name tort --stage {file_path/ingest}
```

## 🤖 Running the Bot

To start the Discord bot, use:

```sh
LOG_LEVEL=ERROR pgml-chat --collection_name tort --chat_completion_model gpt-3.5-turbo --stage chat --chat_interface discord
```
