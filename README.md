# NLP_SentimentAnalysis

# 🛒 E-commerce Product Review Sentiment Analysis

## 📌 Overview
This project analyzes **customer sentiments** from e-commerce product reviews using **Natural Language Processing (NLP)**. The goal is to classify product reviews as **Positive, Negative, or Neutral** using **TextBlob** and visualize the sentiment distribution.

### 🔥 Features:
- ✅ **Sentiment Analysis** using TextBlob
- ✅ **Automated Sentiment Labeling**
- ✅ **Interactive UI with Gradio** (No coding required to use!)
- ✅ **Visualizations:** Pie Chart & Word Cloud
- ✅ **Ready-to-Use Dataset** (E-commerce product reviews)
- ✅ **Runs on Google Colab or Jupyter Notebook**

---

## 📊 Dataset
I created a **synthetic dataset** of 30+ e-commerce product reviews across different product categories (Shoes, Bags, Phones, etc.).

### **Sample Data:**
| Product   | Review                                       | Sentiment |
|-----------|---------------------------------------------|-----------|
| Shoes     | Absolutely love these shoes! Super comfy. | Positive  |
| Bag       | The bag quality is terrible, not worth it. | Negative  |
| Phone     | Amazing phone with great battery life.    | Positive  |
| Headphones| Sound is okay but not noise-cancelling.   | Neutral   |

---

## 🛠 Tech Stack
| Task                   | Library  |
|------------------------|---------|
| Text Processing       | `TextBlob` |
| Data Manipulation     | `pandas` |
| Data Visualization    | `matplotlib`, `wordcloud` |
| Interactive UI        | `Gradio` |

---

## 📈 Visualizations
### **📊 Sentiment Distribution (Pie Chart)**
Shows the proportion of **positive, negative, and neutral reviews**.

### **🌟 Word Cloud for Positive & Negative Reviews**
Highlights the most frequently used words in **positive** and **negative** reviews.

---

## 🚀 How to Run
### **Option 1: Google Colab** *(Recommended)*
1. Open this project in **Google Colab** *(link pending)*
2. Run all cells – it will install required libraries and execute the code
3. The Gradio UI will generate a public link for interaction

### **Option 2: Local Jupyter Notebook**
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/ecommerce-sentiment-analysis.git
   cd ecommerce-sentiment-analysis
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebook or execute `app.py` for the Gradio interface

---

## 🎭 Gradio Interactive Sentiment Analysis
💡 **Want to test sentiment analysis without coding?** Just enter any product review and get instant feedback!

To launch:
```python
import gradio as gr
from textblob import TextBlob

def analyze_review(text):
    polarity = TextBlob(text).sentiment.polarity
    if polarity > 0:
        return "Sentiment: Positive 😊"
    elif polarity < 0:
        return "Sentiment: Negative 😠"
    else:
        return "Sentiment: Neutral 😐"

gr_interface = gr.Interface(
    fn=analyze_review,
    inputs=gr.Textbox(label="Enter a Product Review"),
    outputs=gr.Textbox(label="Sentiment Analysis Result"),
    title="E-commerce Review Sentiment Analyzer",
    description="Enter a product review and find out if it's Positive, Negative, or Neutral!",
)
gr_interface.launch(share=True)
```

---

## 📜 Future Enhancements
🚀 Improve accuracy using **machine learning models (Logistic Regression, LSTMs, Transformers)**.

🤖 Train on a **larger dataset** from Kaggle.

🎨 Deploy as a **full-fledged Ib app** using Streamlit.

---

## 📢 Contribute
Pull requests are Ilcome! Feel free to **fork** this repo and contribute.

---

## 📄 License
This project is licensed under the **MIT License**.

---

💡 **Like this project?** Don't forget to ⭐ star the repo!

