# ⚡ Riya - The Witty AI Personal Assistant

**Riya** is a lightweight, personality-driven AI chatbot built using **Modern LangChain (LCEL)** and **Gradio**. 

Unlike standard robotic assistants, Riya is designed with a specific persona: a 21-year-old, witty, and enthusiastic companion. This project demonstrates a **stateless, closed-loop architecture** where conversation history is managed dynamically between the frontend (Gradio) and the backend (LangChain).

## 🚀 Features
* **Persona-Driven:** Custom prompt engineering gives Riya a distinct, youthful, and witty personality.
* **Modern LCEL Architecture:** Uses the latest **LangChain Expression Language (LCEL)** for clean, pipe-based logic (`Prompt | Model | Parser`).
* **Context Awareness:** Retains conversation history to answer follow-up questions accurately.
* **Web Interface:** Fully interactive chat UI provided by **Gradio**.
* **Clean Dependency Management:** Uses `langchain-core` without legacy/deprecated packages.

## 🛠️ Tech Stack
* **Language:** Python 3.10+
* **Framework:** [LangChain](https://python.langchain.com/) (Modern LCEL)
* **UI Library:** [Gradio](https://www.gradio.app/)
* **Model Provider:** OpenAI (GPT-3.5-turbo)

## ⚙️ Installation & Setup
 1. Clone the Repository
```
git clone [https://github.com/yourusername/riya-chatbot.git](https://github.com/yourusername/riya-chatbot.git)
cd riya-chatbot
```
2. Install Dependencies
```
pip install langchain langchain-openai gradio
```
3. Set Up API Key
```
export OPENAI_API_KEY="<your key goes here>"
```
4. Run the App

---

## 🧠 Engineering Architecture: The "Feedback Loop"
This project utilizes a Stateless Control System approach rather than traditional memory objects.
* **Input Signal:** The user types a message in the Gradio UI.
* **Feedback Injection:** The full conversation history is injected from the UI into the processing chain.
* **Signal Conditioning:** A Python logic layer converts the raw list data into a formatted string block.
* **Processing (Transfer Function):** The Prompt Template structures the input.
* **Output:** The response is returned to the UI, closing the loop and updating the state.
