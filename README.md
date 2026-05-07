# 🩺 TeleMedi – Intelligent Medical Chatbot

> **An AI-powered medical conversational assistant built using Trie-based dialogue mapping and Levenshtein distance for fuzzy matching.**  
> The system interacts with users through natural conversation and suggests possible remedies based on symptoms.

---

## 🌟 Overview

**TeleMedi** is a healthcare-focused chatbot that allows users to describe their symptoms in simple text.  
Using a **Conversational Trie** and **Levenshtein Distance algorithm**, it intelligently identifies the closest medical condition and provides **appropriate remedies or next-step advice**.

It’s designed as a **Spring Boot application** with a clean, modular backend architecture and can be integrated with a frontend UI or chat interface.

---

## ⚙️ Features

✅ Dynamic symptom detection using Trie-based search  
✅ Fuzzy input matching via Levenshtein distance (handles typos)  
✅ Interactive dialogue flow with multiple health branches  
✅ Provides remedies and medical advice for each detected condition  
✅ Extensible structure for adding new diseases/symptoms  
✅ Simple, modular codebase for educational or clinical use  

---

## 🧠 Core Logic

The chatbot builds a **conversation tree (Trie)**, where:
- Each **node** represents a medical condition or user response.
- Children represent **next questions or outcomes**.
- Each node can hold:
  - A **prompt/question**
  - A list of **suggestions**
  - A **remedy or advice**
  - A flag indicating if it’s an **end node**

### 🔍 Input Handling
When a user enters a message:
1. The system searches for an **exact keyword match**.
2. If not found, it tries **partial/multi-word matches**.
3. If still not found, it uses the **Levenshtein distance algorithm** to find the *closest* word (tolerating typos and small mistakes).

### 🧩 Example
If user types:
"fevar" → Levenshtein distance = 1 → closest match = "fever"

yaml
Copy code
Bot replies accordingly with fever-related questions/remedies.

---

## 🏗️ Tech Stack

| Layer | Technology |
|-------|-------------|
| **Backend Framework** | Spring Boot (Java) |
| **Algorithmic Core** | Trie data structure + Levenshtein Distance |
| **Data Handling** | Java Collections |
| **Frontend (optional)** | React / HTML (for chatbot UI) |
| **Build Tool** | Maven / Gradle |
| **IDE** | IntelliJ IDEA / VS Code / Eclipse |

---

## 📁 Project Structure

TeleMedi/
├── src/
│ ├── main/java/com/example/Telemedi/
│ │ ├── controller/ # REST controllers (if any)
│ │ ├── model/
│ │ │ ├── ConversationalTrie.java
│ │ │ └── TrieNode.java
│ │ └── service/ # Optional logic layer
│ └── resources/
│ ├── static/ # Frontend files (if any)
│ └── application.properties
└── README.md

yaml
Copy code

---

## 🧮 Algorithms Used

### 1. **Trie (Prefix Tree)**
Used to store medical dialogues and responses hierarchically.

### 2. **Levenshtein Distance**
Used to calculate minimum edit distance between user input and known symptom keywords.  
Handles spelling errors and fuzzy matches efficiently.

Formula:  
`distance = number of insertions + deletions + substitutions`

---

## 🧑‍💻 Example Interaction

**Bot:** Hello! I'm your medical assistant. How are you feeling today?  
**User:** I have a hedache.  
**Bot:** You mentioned a headache. Can you describe the type of pain?  
**User:** throbbing  
**Bot:** A throbbing headache noted. Do you experience sensitivity to light or sound?  
**User:** yes  
**Bot:** This sounds like a migraine headache.  
**💊 Remedy:** Take Sumatriptan 50mg or Ibuprofen 400mg. Rest in a dark, quiet room. Apply cold compress.

---

## 💾 Data Backup

All user interactions can be stored for:
- Chat history
- Medical case review
- Future AI model training

Can be integrated with:
- MySQL / MongoDB (for persistent storage)
- Local JSON/CSV (for demo)

---

## 🚀 Future Scope

🔹 Integrate with LLMs for more natural language understanding  
🔹 Add symptom severity detection via NLP  
🔹 Voice-based interaction  
🔹 Connect with real doctors through Telemedicine APIs  
🔹 Mobile app integration (React Native / Flutter)

---

## 🎓 Ideal For

- Students learning **Data Structures (Trie + DP)**  
- Healthcare startups building **telemedicine assistants**  
- Projects in **AI-driven symptom analysis**

---
👥 Team Collaboration & My Contribution

TeleMedi was developed through a collaborative effort of the team. My contributions added value in the following areas:

📚 Improved documentation for clarity and accessibility

🧪 Conducted testing and provided feedback on symptom detection logic

🎓 Crafted clear educational explanations of Trie and Levenshtein algorithms

These efforts enhanced the project’s usability, strengthened its educational focus, and aligned with the team’s vision of building an intelligent healthcare assistant.

---

## 🧾 License

This project is open-source under the **MIT License**.  
Feel free to use, modify, and expand the code for educational or personal use.

---

## ⭐ Support

If you like this project, please consider giving it a ⭐ on GitHub — it helps others discover it!

---

> _“Technology can’t replace doctors, but it can empower patients.”_
