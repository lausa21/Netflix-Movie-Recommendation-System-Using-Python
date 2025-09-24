# 🎬 Netflix Movie Recommendation System
Recommendation systems are a critical feature for streaming platforms like Netflix, helping users navigate the vast library of content. This project addresses the common challenge of "choice overload" by building a **content-based filtering** recommendation system.
The system takes a movie title as input and suggests five similar titles based on shared attributes like type, genre, rating, and country of origin. The core of this project is the **TF-IDF (Term Frequency–Inverse Document Frequency)** methodology for feature weighting, and the final model is deployed as an interactive web application using **Streamlit**.
This project developed for a Model Deployment course in my 4th-semester.

---

### 📊 Dataset 
* **Source:** **[Netflix Movies and TV Shows Dataset on Kaggle](https://www.kaggle.com/datasets/anandshaw2001/netflix-movies-and-tv-shows)**

---

### ⚙️ Methodology
The recommendation engine works by quantifying the "content" of each title and measuring the similarity between them.
* **Feature Engineering:** Key attributes (`title`, `type`, `country`, `rating`, `listed_in`) were combined into a single text feature to create a comprehensive profile for each title.
* **TF-IDF Vectorization:** The text profiles were converted into numerical vectors using the **TF-IDF (Term Frequency-Inverse Document Frequency)** method. 
* **Cosine Similarity:** The similarity between any two titles was calculated using **Cosine Similarity**, which measures the angle between their TF-IDF vectors. This results in a score from 0 (dissimilar) to 1 (identical).
* **Recommendation:** When a user inputs a title, the system returns the five titles with the highest cosine similarity scores.

---

### 🎯 Results & Analysis
The system effectively generates relevant and context-aware recommendations. For instance:
* An input like **"The Irishman"** yields recommendations that are also `Dramas` ``Movie` from the `United States`, including other thematically similar crime films.
<img width="859" height="474" alt="image" src="https://github.com/user-attachments/assets/317ed919-3627-45cc-adf8-c218a209f946" />

---

### 🚀 Deployment with Streamlit
The recommendation model was deployed as an interactive web app to ensure ease of use.
* **Live Application:** **[Deployment Project on Streamlit](https://projectmodep.streamlit.app/)**

---

### 🖋 Author
* Caroline Ang
* Evelyn Caristy Untariady
* Laurel Evelina Widjaja
