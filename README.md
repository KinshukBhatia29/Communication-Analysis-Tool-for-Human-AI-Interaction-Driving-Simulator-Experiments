# **Communication Analysis Tool for Human-AI Interaction Driving Simulator Experiments**

## **1. Overview**
This project analyzes human-AI interaction in a driving simulator by processing audiovisual communication data. It involves:
- **Speech-to-text transcription**
- **Speaker diarization**
- **Sentiment analysis**
- **Visualization of conversation dynamics**

The project consists of **two Jupyter Notebook files**:
1. **`transcription_sentiment.ipynb`** – Extracts audio, transcribes speech, segments speakers, applies sentiment analysis, and saves results in a CSV file.
2. **`visualization.ipynb`** – Reads the processed CSV and generates visualizations for speaker interaction and sentiment trends.

---

## **2. Requirements**

### **2.1 System Requirements**
- OS: Windows 10+, macOS, Linux (Ubuntu recommended)
- Python 3.8+
- Minimum 8GB RAM (16GB+ recommended for large videos)

### **2.2 Required Python Libraries**
To install dependencies, run:
```bash
pip install -r requirements.txt
```
#### **Dependencies**
There are two `requirements.txt` files:
- **For transcription & sentiment analysis (`requirements_transcription.txt`)**:
  ```
  ffmpeg-python
  numpy
  pandas
  nltk
  pyannote.audio
  whisper
  openai
  ```
- **For visualization (`requirements_visualization.txt`)**:
  ```
  matplotlib
  seaborn
  pandas
  ```

To install them separately:
```bash
pip install -r requirements_transcription.txt
pip install -r requirements_visualization.txt
```

---

## **3. Installation & Setup**

### **3.1 Installing Dependencies**
Ensure `pip` is up-to-date and install the required libraries:
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### **3.2 Hugging Face Authentication**
Some models require authentication with a **Hugging Face token**.
1. Visit: [https://huggingface.co/settings/tokens](https://huggingface.co/settings/tokens)
2. Generate a **READ token**.
3. Authenticate:
```python
from huggingface_hub import login
login("YOUR_HUGGINGFACE_TOKEN")
```


## **4. Testing & Validation**

### **4.1 Functional Testing**
1. **Small Sample Test:** Run a short (1-min) test video and check if:
   - The transcription is accurate.
   - The timestamps match.
   - The speaker diarization is correct.
2. **Edge Cases:**
   - Multiple overlapping speakers.
   - Background noise interference.
   - Short, unclear words.

### **4.2 Performance Testing**
- Measure **processing time** for different video sizes.
- Check **memory usage** during execution.


---

## **6. Conclusion**
This tool provides **automated speech analysis** for driving simulations, offering **detailed insights into communication trends**. Future improvements can include **real-time analysis** and **more advanced NLP models** for better speaker attribution and emotion detection.

---

## **7. Contributors & Acknowledgments**
**Author:** Kinshuk Bhatia  
**Project Goal:** Submission for Google Summer of Code (GSoC)  

For questions, please contact **[bhatiakinshuk29@gmail.com]**.

