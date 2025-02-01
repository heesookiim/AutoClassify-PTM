# AutoClassify-PTM

This project was developed as part of a research initiative at Purdue University, in collaboration with Cisco and NSF.  

I worked as a core contributor, designing and implementing a **contrastive learning-based classification system** to improve the identification of pre-trained model architectures (PTMs) in open-source machine learning platform like HuggingFace.  

Currently, the research team is building a more refined system on top of my initial implementation. Due to the ongoing nature of the project, the full code cannot be shared at this time. However, this repository provides an overview of the methodology, results, and future directions.  

## Overview  

Misclassification of pre-trained models in open-source repositories leads to inefficiencies in deep learning development. This project introduces an **AI-driven classification system** using contrastive learning, significantly improving accuracy and reliability in organizing PTMs.  

### Key Achievements
- Achieved **96.55% classification accuracy** across **107 architectures** (e.g., BERT, GPT, YOLO, Wav2Vec).  
- Improved PTM reusability by reducing misclassification errors.  
- Applied **contrastive learning** to refine embedding space and improve model separability.  

### Key Technologies Used
- Deep Learning: Contrastive learning, NT-Xent loss
- Natural Language Processing (NLP): RoBERTa tokenizer, text embeddings
- Machine Learning: Multiclass classification for PTM categorization
- Software & Data Processing: OpenAI API, PostSQL for large-scale dataset handling


## Research Poster  

![VIP Poster](https://github.com/user-attachments/assets/766423c0-63bf-44a3-80b4-edc3ebbc6477)  

## Key Contributions  

- **Contrastive Learning for Model Representation**  
  - Designed and implemented a contrastive learning-based classifier.  
  - Used NT-Xent loss to improve clustering and model separability.  

- **Pretrained Model Embeddings with RoBERTa**  
  - Processed model descriptions using RoBERTa tokenizer.  
  - Applied a structured 512-token input format for consistency.  

- **Scalable Multiclass Classification System**  
  - Categorized PTMs into 107 architecture labels.  
  - Improved classification accuracy through fine-tuning.  

- **Large-Scale Dataset Processing & AI Model Deployment**  
  - Processed PTM metadata extracted from Hugging Face.  
  - Developed a scalable approach for automated PTM classification.
  
## Methodology  

1. **Data Collection & Preprocessing**  
   - Extracted metadata (model name, architecture, task, and layers) using the Hugging Face API.  

2. **Text Embedding with RoBERTa**  
   - Encoded PTM descriptions into numerical embeddings.  
   - Applied structured tokenization with padding for uniformity.  

3. **Contrastive Learning for Model Representation**  
   - Used NT-Xent loss to refine embedding space.  
   - Ensured models of similar architectures clustered together while dissimilar architectures remained distinct.  

4. **Multiclass Classification for PTM Prediction**  
   - Assigned PTMs to one of 107 architecture labels.  
   - Fine-tuned classifier to optimize accuracy.  

## Results  

The trained classifier achieved **96.55% accuracy** on 107 model architectures.  

| Method                | Precision | Recall | F1-score | Threshold |
|-----------------------|-----------|--------|----------|-----------|
| No Fine-Tuning       | 0.6751    | 0.3778 | 0.4845   | 0.78      |
| Fine-Tuning          | 0.8134    | 0.6869 | 0.7448   | 0.97      |
| Contrastive Learning | 0.8795    | 0.9434 | 0.9103   | 0.51      |

## Future Work  

- **Expansion to PeaTMOSS Dataset**  
  - Training on 281,638 PTMs with detailed metadata.  
  - Improving classification for both architecture and task labels.  

- **Deployment to Hugging Face**  
  - Reducing PTM misclassification in open-source repositories.  
  - Suggesting model architecture and task labels for newly uploaded PTMs.  

## Research Team  

This research was conducted at Purdue University, supported by Cisco and NSF.  

**Authors:**  
- Heesoo Kim  
- Mingyu Kim  
- Wenxin Jiang  
- Advisor: Prof. James C. Davis (ECE, Purdue University)  

## Why This Project Matters  

This project showcases expertise in:  
- **Deep Learning** – Contrastive learning, representation learning, NT-Xent loss  
- **NLP & Text Processing** – RoBERTa embeddings, metadata analysis  
- **Machine Learning Model Deployment** – Scalable AI classification  
- **Large-Scale Data Handling** – Processing 281K+ PTMs efficiently  
- **AI Research & Industry Applications** – Improving model reuse and reliability  
