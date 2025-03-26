# 🚀 Echo Mind- Smart Recommendation System

## 📌 Table of Contents

- [Introduction](#introduction)
- [Demo](#demo)
- [Inspiration](#inspiration)
- [What It Does](#what-it-does)
- [How We Built It](#how-we-built-it)
- [Challenges We Faced](#challenges-we-faced)
- [How to Run](#how-to-run)
- [Tech Stack](#tech-stack)
- [Team](#team)

---

## 🎯 Introduction

'Echo Mind- Smart Recommendation System' is an AI-powered solution that leverages Generative AI to analyze customer data, including profiles, social media activity, purchase history, sentiment analysis, and demographic details, to deliver tailored recommendations for products, services, or content.

## 🎥 Demo

🔗 [Live Demo](#)
https://www.loom.com/share/1145a694dd8e4cc9bc7fa3a0509b0073?sid=593dc6ee-a862-4f79-8613-0ab4cd41e29d
📹 [Video Demo](#) (if applicable)  
🖼️ Screenshots:

![Screenshot 1](link-to-image)

## 💡 Inspiration

The demand for hyper-personalization is growing rapidly as customers expect experiences tailored to their unique preferences. Leading companies like Netflix, Amazon, and Spotify have set the benchmark by leveraging AI to offer personalized recommendations that drive engagement and customer satisfaction.

However, many businesses struggle to implement such sophisticated AI-driven personalization due to challenges like data silos, lack of real-time insights, and limited AI adoption.

RecomAI was inspired by the need to bridge this gap by creating a scalable, AI-powered recommendation system that not only personalizes customer experiences but also provides businesses with valuable insights to enhance customer engagement and retention.

By combining Generative AI, deep learning, and sentiment analysis, our solution aims to redefine hyper-personalization, ensuring businesses can deliver the right content, product, or service to the right customer at the right time.

## ⚙️ What It Does

For AI driven hyper-personalization and recommendations, we have created two models with different approaches.

1. Smart Recommendation System
   We have leveraged the electronics section of Amazon Reviews 2023 dataset to create a LightGCN model. LightGCN is an embedding-based model, which means it attempts to find the optimal embeddings (vectors) for users and items. In addition, it also seeks the optimal scoring function, denoted as f. This function assigns scores to new user-item pairs, and items with higher scores are recommended.

   Once the user chooses items, we extract the embedding for those items from the model’s item embeddings, average out the embeddings of those items and compute cosine similarity of the averaged out embedding with the embeddings of all other items. and we recommend the top 5 items with the highest cosine similarity scores are recommended by the LightGCN model.

2. GenAI Financial Recommendation Engine
   This project builds a Retrieval-Augmented Generation (RAG) based QA system that recommends company products based on open-source company product data, demographic (DEMOG) data, and bureau (BUREAU) data. It leverages LangChain, Hugging Face embeddings, and the Zephyr 7B LLM for intelligent recommendations.

## 🛠️ How We Built It

For AI driven hyper-personalization and recommendations, we have created two models with different approaches.

1. Smart Recommendation System
   We have leveraged the electronics section of Amazon Reviews 2023 dataset to create a LightGCN model. LightGCN is an embedding-based model, which means it attempts to find the optimal embeddings (vectors) for users and items. In addition, it also seeks the optimal scoring function, denoted as f. This function assigns scores to new user-item pairs, and items with higher scores are recommended.

   Once the user chooses items, we extract the embedding for those items from the model’s item embeddings, average out the embeddings of those items and compute cosine similarity of the averaged out embedding with the embeddings of all other items. and we recommend the top 5 items with the highest cosine similarity scores are recommended by the LightGCN model.

2. GenAI Financial Recommendation Engine
   This project builds a Retrieval-Augmented Generation (RAG) based QA system that recommends company products based on open-source company product data, demographic (DEMOG) data, and bureau (BUREAU) data. It leverages LangChain, Hugging Face embeddings, and the Zephyr 7B LLM for intelligent recommendations.

Components:

1. Data Ingestion & Preprocessing:
   o Load open-source company product, DEMOG, and BUREAU data.
   o Preprocess the data (cleaning, normalization, feature engineering).
   o Save the processed data into a CSV file.
2. Embedding & Vector Database:
   o Load the preprocessed CSV.
   o Convert text-based data into embeddings using a Hugging Face Embedding Model.
   o Store embeddings in a Vector Database (e.g., FAISS, ChromaDB, Pinecone).
3. Retrieval-Augmented Generation (RAG) Pipeline:
   o Utilize LangChain to retrieve relevant data from the vector DB.
   o Process queries using the Zephyr 7B LLM to generate contextual responses.
4. Evaluation of Recommended Products:
   o Check if the recommended products align with customer needs.
   o Validate outputs against business logic and predefined evaluation metrics.

GenAI Financial Recommendation System

Project Methodology
This Project using the Open Source Data of Company Products information with their DEMOG and BUREAU data.
Using Python, that load data and then pre-processed and saved in CSV File.
Loading that same CSV file to insert into Vector DB using Embedding Model from Hugging Face.
Building RAG QA Chain using Langchain and building the RAG architecture using Zypher 7B LLM (Open Source).
Checking Recommended product response from LLM.

Due to CPU limitations for running a Large Language Model locally, we have leveraged Google Colab GPU for running our LLM Model. On providing customer information from the synthetic dataset we created earlier, the LLM will analyze and generate banking product recommendations.

https://colab.research.google.com/drive/1ZiHMN2Ss0XRRBow5phQhqYNZaAg1G9DY?usp=sharing

Open the Colab Notebook.
Run each cell.

3️⃣ Building the Recommendation Engine

Applied collaborative filtering and content-based filtering techniques.

Fine-tuned the LLM using domain-specific customer behavior data.

4️⃣ User Interface & Deployment

Developed an interactive UI using Streamlit for businesses to explore recommendations and insights.

Designed a real-time dashboard for businesses to monitor engagement and optimize personalization strategies.

By integrating LLMs with powerful data processing tools and an intuitive interface, RecomAI provides a scalable, AI-driven recommendation system that enhances customer engagement and business insights.

## 🚧 Challenges We Faced

During the development of RecomAI, we encountered several challenges that pushed us to optimize our approach and refine our solution.

🔹 Data Collection & Integration – Aggregating and processing customer data from multiple sources (social media, purchase history, sentiment analysis) while ensuring data consistency and accuracy was challenging.

🔹 Finding the Right LLM -

🔹 Selecting the right dataset was crucial for training RecomAI to generate accurate and meaningful hyper-personalized recommendations. We needed datasets that contained diverse customer interactions, purchase behavior, sentiment data, and demographic details to build a robust AI model.

## Run below step 1 and step 2

## 🏃 Step 1 : How to Run Smart Recommendation System

1. Clone the repository
   ```sh
   git clone https://github.com/ewfx/aidhp-echo-mind.git
   ```
2. Install dependencies

   ```sh
   pip install streamlit
   pip install pandas
   pip install -r requirements.txt (for Python)
   ```

3. Run the project

   ```sh
   streamlit run app.py

   python app.py
   ```

## 🏃 Step 2: How to Run GenAI Financial Recommendation Engine

4. Clone the repository
   ```sh
   git clone https://github.com/ewfx/aidhp-echo-mind.git
   ```
5. Install dependencies

   ```sh
   https://colab.research.google.com/drive/1ZiHMN2Ss0XRRBow5phQhqYNZaAg1G9DY?usp=sharing

   Open the Colab Notebook.
   Run each cell to install dependencies
   ```

6. Run the project

   ```sh
   https://colab.research.google.com/drive/1ZiHMN2Ss0XRRBow5phQhqYNZaAg1G9DY?usp=sharing

   Open the Colab Notebook.
   Run each cell.

   ```

## 🏗️ Tech Stack

🚀 Programming Language: Python

📊 Data Processing: Pandas, NumPy, Scikit-learn
Vector DB, ChromaDB

🧠 AI & Machine Learning: Embedding Model Hugging Face, RAG Framework LangChain,
LLM Model Zephyr 7B

📈 Data Visualization & UI: Streamlit

## 👥 Team

- Annapurna - [AnnapurnaBichala](#)
- Krettika - [krettika](#)
- Shayan Halder - [xraptorgg](#)
- Nalini - [vnalinii](#)
- Krishnakanth - [krishnakanthnarava](#)
