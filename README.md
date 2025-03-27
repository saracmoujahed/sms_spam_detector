# sms_spam_detector
Here's a **README.md** file for your project:  

---

## 📱 SMS Spam Detector  

### 🚀 Overview  
This project is a **SMS Spam Detector**, where an SMS text classification solution is refactored into a function that constructs a **linear Support Vector Classification (SVC) model**. The model is trained on SMS data and deployed using **Gradio**, allowing users to test text messages and determine whether they are classified as **spam** or **not spam**.  

---

### 📂 Project Structure  
- **`gradio_sms_text_classification.ipynb`** – Main Jupyter Notebook containing the Gradio app and refactored model.  
- **`sms_text_classification_solution.ipynb`** – Starter solution for SMS classification.  
- **`SMSSpamCollection.csv`** – Dataset containing SMS messages labeled as "spam" or "ham" (not spam).  

---

### 🛠️ Installation & Setup  
1. **Clone the repository:**  
   ```bash
   git clone https://github.com/yourusername/sms_spam_detector.git
   cd sms_spam_detector
   ```
2. **Install dependencies:**  
   ```bash
   pip install -r requirements.txt
   ```
   *(Ensure Python and pip are installed on your system.)*  
3. **Run the Jupyter Notebook:**  
   ```bash
   jupyter notebook
   ```
4. **Launch the Gradio app (inside Jupyter Notebook):**  
   ```python
   gr.Interface(fn=sms_prediction, inputs="textbox", outputs="textbox").launch()
   ```

---

### 📊 Model Development  

#### 1️⃣ **SMS Classification Function**  
- Extracts features (SMS text) and target labels ("ham" or "spam").  
- Splits the data into **training (67%)** and **testing (33%)** sets.  
- Transforms and normalizes the text data.  
- Builds and trains a **Support Vector Classifier (SVC)** model.  
- Returns the trained model for classification.  

#### 2️⃣ **SMS Prediction Function**  
- Takes a new text message as input.  
- Predicts whether it is **"spam"** or **"ham"**.  
- Returns a user-friendly message indicating the classification.  

#### 3️⃣ **Gradio Interface**  
- Simple web-based UI for testing SMS messages.  
- Accepts user input in a textbox.  
- Displays classification results in real time.  

---

### 🎯 Example Usage  
#### ✅ Not Spam  
**Input:**  
```  
"Hey, are we still meeting for coffee at 3?"  
```  
**Output:**  
```  
The text message: "Hey, are we still meeting for coffee at 3?", is not spam.  
```  

#### ❌ Spam  
**Input:**  
```  
"Congratulations! You've won a free iPhone. Click here to claim now."  
```  
**Output:**  
```  
The text message: "Congratulations! You've won a free iPhone. Click here to claim now.", is spam.  
```  

---

### 🎥 Demo  
[🔗 Live Gradio App](https://ea2df1f0ee507fde38.gradio.live/) *(Add link when deployed)*  

---

### 💡 Future Improvements  
- Implement **deep learning (LSTM)** for better accuracy.  
- Deploy on **Streamlit** or **Flask** for more flexibility.  
- Integrate with **WhatsApp API** for real-time SMS filtering.  

---

### 🤝 Contributing  
Want to improve this project? Follow these steps:  
1. **Fork** the repo.  
2. **Create a new branch** (`feature-xyz`).  
3. **Commit your changes** and **push**.  
4. **Submit a pull request!**  

---

### 📝 License  
This project is licensed under the **MIT License**.  
