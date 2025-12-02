# 🛡️ Security Layer for LLMs

A lightweight **Safety & Security Layer** designed to detect and block unsafe prompts before reaching any **Large Language Model (LLM)**.
This system enhances output safety, prevents harmful content, and maintains user trust without relying on expensive APIs.



## 📌 Overview

Large Language Models sometimes generate **unsafe content** (offensive, biased, or harmful).
This project introduces a **Security Layer** that filters prompts before they reach the LLM, reducing:

* User dissatisfaction
* Reputation risk
* Policy violations



## 🚨 Problem Definition

LLMs learn from large internet datasets that may contain toxic or misleading examples, causing unsafe outputs such as:

* Offensive language
* Biased responses
* Harmful instructions

A safety layer is required to block such content at the **prompt level** before the model produces a response.



## 🧠 Proposed Solution

We built a multi-stage **Security Layer** that:

* Classifies user prompts as SAFE or UNSAFE
* Blocks harmful content before reaching the LLM
* Ensures policy-aligned, responsible, and trustworthy outputs
* Maintains high accuracy through hybrid modeling

The system uses:

* **Machine Learning** (Logistic Regression)
* **Deep Learning** (BiLSTM)
* A **Hybrid Model** combining both for optimal performance



## ⚙️ Implementation Details

### 📊 Dataset

* **180,000+ real prompts** collected from multiple diverse sources
* **1,000 synthetic prompts** to improve rare-case and adversarial coverage
* **44,000+ real prompts** in the test set
* Balanced and diverse to ensure reliable evaluation



## 🤖 Model Training

### **1. Logistic Regression (TF-IDF)**

* Captures keyword patterns
* Strong baseline classifier
* Accuracy: **93.2%**

### **2. BiLSTM Deep Learning Model**

* Embedding layer
* Bidirectional LSTM for contextual understanding
* Dropout + Normalization to reduce overfitting
* Accuracy: **89.3%**

### **3. Hybrid Model (LR + BiLSTM)**

Combining strengths of both models improved robustness.
**Final accuracy: 93.40%**



## 🧪 Model Testing

* LR excels at general text pattern detection
* BiLSTM excels at sequential meaning and deeper context
* Combined model delivers higher stability and accuracy across all unsafe categories



## 🖥️ User Interface

The UI includes:

### **Chat Interface**

* Light-blue bubble for user messages
* Dark bubble for model responses
* Icons:

  * 🛡️ SAFE
  * ⚠️ UNSAFE
* Displays:

  * LR prediction
  * BiLSTM prediction
  * Final decision
  * Confidence score

### **Spelling Correction Panel**

* ✏️ Edit button beside each user message
* Inline text editor with suggested corrections
* "Resend corrected" button

### **Additional Features**

* New Chat reset
* Light/Dark theme switch
* Clean header with “Secure LLM” subtitle



## 🎥 Demo

(Add demo GIF or video link here)



## 💰 Market Value

A **cost-effective, high-impact** safety solution:

* Lightweight and optimized
* No reliance on expensive API calls
* Fully customizable
* Easy to deploy (local or cloud)
* Suitable for startups, enterprises, and public sector organizations



## 🚧 Challenges & Solutions

### **1. Unbalanced Dataset**

* Combined multiple datasets → improved accuracy to 92%
* Added 1,000 synthetic prompts → accuracy increased to 93%

### **2. Sequential Understanding**

* Implemented BiLSTM → boosted performance to **93.40%**



## 🔮 Future Work

* Generate more synthetic data for specific safety scenarios
* Integrate higher-quality embeddings
* Build a bilingual (English + Arabic) dataset
* Improve real-time detection
* Conduct deeper error analysis



## 👥 Team Members

* **Haitham Alsaloumi**
* **Rana Alsulami**
* **Danah Alsarrani**
* **Ghadi Bakhshwain**



## 🛠️ Team Workflow

We used:

* **Kanban board** (To Do → In Progress → Review → Done)
* Shared documentation for notes, experiments, and updates
* Continuous model testing and iteration



## ✔️ Conclusion

This project delivers an effective **Security Layer for LLMs**, ensuring safe and responsible interactions.
With hybrid modeling, synthetic data generation, and UI integration, the system provides reliable protection and forms the foundation for future multilingual safety systems.



## 🙏 Acknowledgments

SDA — WCD Generative AI / LLM Bootcamp
Instructors: Ricardo Alamo, Pankti Shah, Shaohua Zhang, Faiqa Mehboob
