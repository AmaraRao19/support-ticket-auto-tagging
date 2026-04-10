 **Objective of the Task**

The objective of this project is to automatically classify and tag customer support tickets using a Large Language Model (LLM). The system analyzes the textual content of each ticket and assigns the most relevant categories, reducing the need for manual labeling and improving efficiency in support systems.

---

 **Methodology / Approach**

This project uses Natural Language Processing (NLP) techniques with **Hugging Face Transformers**.

The following approaches were implemented:

* **Zero-shot Learning**:
  A pre-trained transformer model (`facebook/bart-large-mnli`) is used to classify tickets into predefined categories without any additional training.

* **Few-shot Learning**:
  Example-based prompts are provided to guide the model and improve classification accuracy.

* **Multi-label Classification**:
  For each ticket, the model predicts multiple possible categories and returns the **top 3 most probable tags**.

Steps followed:

1. Load dataset (CSV file)
2. Preprocess text data
3. Define possible labels (categories)
4. Apply zero-shot classification
5. Enhance results using few-shot prompting
6. Extract top 3 predicted tags
7. Save results for analysis

---

## 📊 **Key Results / Observations**

* The model successfully categorized support tickets without requiring heavy training.
* **Zero-shot learning** provided good baseline results for most tickets.
* **Few-shot learning** improved prediction accuracy for ambiguous or complex queries.
* The system was able to generate **top 3 relevant tags**, making it more flexible than single-label classification.
* The approach is lightweight and works efficiently on Google Colab without requiring high GPU resources.

---
