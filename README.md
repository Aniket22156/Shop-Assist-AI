# 🛍️ ShopAssistAI - Your Personalized Laptop Shopping Assistant

ShopAssistAI is a conversational AI-powered shopping assistant designed to simplify the laptop purchasing process. By leveraging large language models (LLMs) and rule-based filtering, it delivers personalized laptop recommendations through a natural dialogue interface.

---

## 📌 Table of Contents

- [Background](#background)
- [Problem Statement](#problem-statement)
- [Dataset](#dataset)
- [Approach](#approach)
- [System Functionalities](#system-functionalities)
- [System Architecture](#system-architecture)
- [Implementation Details](#implementation-details)
- [Setup Instructions](#setup-instructions)
- [Prerequisites](#prerequisites)
- [License](#license)

---

## 🧠 Background

In the modern digital world, shopping for a laptop online can be overwhelming due to the vast number of options and the need for personalized guidance. **ShopAssistAI** solves this by offering a smart chatbot interface that helps users find the most suitable laptops based on their preferences.

---

## ❓ Problem Statement

Given a dataset with product names, specs, and descriptions of laptops, build a chatbot (**ShopAssistAI**) that:
- Understands user needs via natural conversation.
- Recommends the top 3 laptops that match the user's preferences.

---

## 📁 Dataset

The dataset (`laptop_data.csv`) includes rows of laptop specifications and descriptions used for generating relevant, personalized recommendations.

---

## ⚙️ Approach

1. **Conversation and Information Gathering**  
   The chatbot engages the user to understand needs like budget, display, performance, etc.

2. **Information Extraction**  
   Rule-based logic is used to identify the best matches from the dataset.

3. **Personalized Recommendation**  
   Based on the extracted user profile, the chatbot offers top 3 laptop options.

---

## 🧩 System Functionalities

- **User Interface**: Intuitive web UI for seamless interaction.
- **Conversational AI**: Uses OpenAI's chat model for generating smart, guided dialogue.
- **Input Moderation**: Ensures safe and respectful communication using OpenAI's moderation API.
- **User Profile Extraction**: Extracts preferences and converts them into structured JSON using OpenAI Function Calling.

---

## 🏗️ System Architecture

- **Client-Server Model** using Flask.
- Web app communicates with:
  - OpenAI’s APIs (for chat and moderation).
  - An external laptop dataset for recommendations.

---

## 🛠️ Implementation Details

### Key Modules:
- `initialize_conversation()` — Starts the session.
- `get_chat_completions()` — Returns AI-generated responses.
- `moderation_check()` — Ensures content safety.
- `intent_confirmation_layer()` — Verifies user’s profession/needs.
- `dictionary_present()` — Checks if a profile has been created.
- `compare_laptops_with_user()` — Compares user preferences and recommends laptops.
- `initialize_conv_reco()` — Starts recommendation conversation.

---

## 🔧 Setup Instructions

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/ShopAssistAI.git
   cd ShopAssistAI
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Add your OpenAI API key:
   - Save your key in a file named `OpenAI_API_Key` in the root directory.

4. Run the Flask app:
   ```bash
   python app.py
   ```

---

## 📋 Prerequisites

- Python 3.7 or higher
- OpenAI API Key (saved in `OpenAI_API_Key` file)

---

## 📄 License

This project is licensed under the MIT License. See `LICENSE` for more information.
