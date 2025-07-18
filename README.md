# 🤖 Sentiment Analysis with Deep Learning using BERT

This project demonstrates how to fine-tune a pretrained BERT model using PyTorch for multi-class sentiment analysis on Twitter data. It covers every step of building an NLP pipeline, including data preprocessing, model customization, training, evaluation, and performance visualization.

---

## 📂 Project Structure

Sentiment-Analysis-BERT/

│

├── data/

│ └── smile-annotations-final.csv # SMILE Twitter Emotion dataset

│

├── main.py # Main script for data preprocessing, training, and evaluation

├── README.md # Documentation and project overview


---

## 📊 Dataset

We use the **SMILE Twitter Emotion Dataset**, which contains annotated tweets labeled with various emotions:  

- **Emotions:** happiness, sadness, anger, disgust, surprise, fear  
- Dataset size: ~6,600 tweets

📖 Dataset Reference:  
Wang, Bo; Tsakalidis, Adam; Liakata, Maria; Zubiaga, Arkaitz; Procter, Rob; Jensen, Eric (2016): *SMILE Twitter Emotion Dataset*. [DOI Link](https://doi.org/10.6084/m9.figshare.3187909.v2)  

---

## 🛠 Features

✅ **Preprocessing & Tokenization**  
- Cleaned text data and converted categorical labels to numerical encodings.  
- Used HuggingFace’s `BertTokenizer` for tokenizing and encoding tweet data.  

✅ **Model Building**
- Loaded `bert-base-uncased` pretrained model from HuggingFace Transformers.  
- Adjusted architecture for multi-class classification.  

✅ **Training & Optimization**
- Customized optimizer (AdamW) and learning rate scheduler for efficient fine-tuning.  
- Built reusable training and evaluation loops to monitor model performance and save checkpoints.  

✅ **Evaluation**
- Computed weighted **F1-score** and per-class accuracy for model assessment.  
- Saved and reloaded fine-tuned models for later use.

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/Sentiment-Analysis-BERT.git
   cd Sentiment-Analysis-BERT
2. Install dependencies
   ```bash
   pip install torch transformers scikit-learn pandas tqdm
   ```
3. Run the main script
   ```bash
   python main.py
4. (Optional) Use GPU if available for faster training.
