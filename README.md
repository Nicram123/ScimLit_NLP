# ScimLit Text Classification (NLP Project)

This repository contains a deep learning project focused on **scientific literature classification** using **Natural Language Processing (NLP)**.  
The goal of this project is to classify biomedical or scientific abstracts (e.g., from PubMed or Kaggle datasets) into categories such as *background*, *methods*, *results*, or *conclusions*.

The project is inspired by the **ScimLit dataset** from TensorFlow Datasets, and demonstrates a complete workflow — from text preprocessing to model evaluation.

The project has three main parts:

1. **Text Cleaning and Tokenization**  
2. **Embedding and Feature Representation**  
3. **Model Training and Evaluation**

---

## 🧩 Stack

**Python**, **Pandas**, **NumPy**, **Matplotlib**, **Scikit-Learn**, **TensorFlow**, **TensorFlow Hub**, **Keras**

---

## 📊 Text Preprocessing

In this phase, the text data is prepared for neural network training.  
The steps include:

- alphabet = string.ascii_lowercase + string.digits + string.punctuation get all keyboard char   
- Tokenization using TensorFlow / Keras `Tokenizer`  
- Padding and truncation of sequences to a uniform length  
- Optional `TF-IDF` representation for baseline experiments  
- Label encoding of target categories  

This ensures all sequences have consistent shapes and vocabulary coverage.

### Example visualizations:

- **Text length distribution**
  <img width="621" height="376" alt="image" src="https://github.com/user-attachments/assets/c92da00d-fcf0-45d3-95bf-c5108d36bc84" />

- **Word frequency histogram**
<img width="575" height="352" alt="image" src="https://github.com/user-attachments/assets/f38c2d6a-3513-4d35-bf69-98a51cc645fc" />


---

## 🧠 Model use

The model uses a combination of **embedding layers** and **pretrained text encoders**.

## Examples of Experiments: 
1. `model_0` Pipeline is baseline model_0 which give us a fundamentals on the beginning of experiments (`TfidfVectorizer` and `MultinomialNB`)
2. `model_1 ` custom token embedding use `text_vectorizer` with `text\token Embedding` and use `Conv1D` that model is worse that baseline
3. `model_2` use pretrained token embedding `tf_hub_sentence_encoder` 
4. `model_3` use custom char embedding use `char_vectorizer` with `char_embed` and use `Conv1D`
5. `model_4` hybrid char and token embedding combine `Token + Char embedding`
6. `model_5` hybrid char and token model but additional we add line numbers representation 


## Results: 
<img width="795" height="681" alt="image" src="https://github.com/user-attachments/assets/2a7180f7-a2e3-437a-8aee-50057948c0e2" />

