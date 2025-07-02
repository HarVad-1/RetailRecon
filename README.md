## 🛍️ Retail Recon
Retail Recon is a Gradio-based web application that serves as the interactive interface for an autonomous multi-agent framework that hunts the internet for the best online deals. This system intelligently scrapes, filters, analyzes, and notifies users about high-value discounts using machine learning, vector search, and LLMs.

## 🚀 Features
🎯 Autonomous Agent System to find, evaluate, and recommend online deals.

🧠 ML-Powered Price Estimation using Random Forest and fine-tuned LLaMA 3.1.

📬 Real-time Deal Alerts via Twilio-based push notifications and SMS.

🧾 Interactive Deal Visualization with detailed logs and user interface in Gradio.

🔍 RAG + GPT-4o mini for smart product similarity and price prediction.

## 🧩 Agents Overview
🗂️ agent.py
Logs all messages from the agent framework, acting as a central terminal output monitor.

📰 deals.py
Scrapes fresh online deals using BeautifulSoup and RSS feeds from [dealnews.com] via Pydantic validation.

🧠 ensemble_agent.py
Estimates product prices using an ensemble of regression models:

🌲 Random Forest Agent

🧑‍🔬 Specialist Agent

🚀 Frontier Model

🛸 frontier_model.py
Finds similar products using Vector DB + RAG, then prompts GPT-4o mini to predict the ideal price.

📲 messaging_agent.py
Uses Twilio API to send SMS and push notifications for attractive or time-sensitive deals.

🗺️ planning_agent.py
Scans for new deals, estimates value, ranks top 5, and automatically picks and notifies the best unseen deal.

🌲 random_forest_agent.py
Predicts product pricing using Random Forest Regression for robust price modeling.

🕵️ scanning_agent.py
Fetches new deals via RSS, filters already seen items using memory, and constructs prompts for downstream LLMs.

🧑‍⚕️ specialist_agent.py
Runs a quantized fine-tuned LLaMA 3.1 model (trained with QLoRA, Hugging Face, and BitsAndBytes) on Modal for specialized price predictions.

## 💻 Technologies Used
🐍 Python, Gradio

📡 RSS Feeds, BeautifulSoup, Pydantic

🌲 Scikit-learn (Random Forest), Ensemble Regression

🔍 FAISS / Vector DB + RAG

🤖 LLaMA 3.1 (Quantized with QLoRA, hosted on Modal)

✉️ Twilio API for Messaging

💬 OpenAI GPT-4o mini

## 📬 Notifications
Make sure to configure your TWILIO_ACCOUNT_SID, AUTH_TOKEN, and phone number in your .env file to receive SMS notifications!

## ✨ Future Enhancements
Add voice-based interaction with deals

Extend to other deal websites like Amazon, Flipkart, etc.

Add user-specific deal preferences
## 🧠 Credits

Developed by an autonomous multi-agent system powered by LLMs, machine learning, and a lot of caffeine ☕ — built under the guidance and mentorship of [@ed-donner](https://github.com/ed-donner). 🙌
