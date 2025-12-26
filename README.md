# **EmotionSense AI: Speech Emotion Recognition (SER)**

### **What is this project?**

i built this project to detect human emotions from audio files. instead of reading text, the AI listens to the **tone, pitch, and energy** of the voice to figure out if someone is Happy, Sad, Angry, or Calm.

---

### **1. The Dataset**

i used the **RAVDESS** (Ryerson Audio-Visual Database of Emotional Speech and Song).

* it has **1,440 files**.
* 24 professional actors (12 male, 12 female).
* 8 different emotions: Neutral, Calm, Happy, Sad, Angry, Fearful, Disgust, and Surprised.

---

### **2. How I Processed the Sound**

computers can't "hear" mp3 or wav files directly, so i had to extract the features:

* **Librosa:** i used this library to load the audio.
* **MFCC (Mel-frequency cepstral coefficients):** i extracted these because they represent the "shape" of the human voice.
* **Data Augmentation:** i added some noise and shifted the pitch to make the model stronger so it doesn't fail on low-quality audio.

---

### **3. The AI Brain (CNN Architecture)**

i used a **Convolutional Neural Network (CNN)**. usually, CNNs are for pictures, but they work great on audio "fingerprints" (MFCCs).

* **Conv1D Layers:** to find patterns in the sound waves.
* **Dropout Layers:** i used these to stop the model from memorizing the data (overfitting).
* **Softmax Activation:** to give a percentage score for each emotion.

---

### **4. Results & Performance**

* **Accuracy:** the model performs well across all categories.
* **Best at:** catching **Angry** and **Sad** tones because they have very specific pitch patterns.
* **Tools Used:** Python, Keras/TensorFlow, Librosa, and Matplotlib.

---

### **5. How to use it**

1. **Extract:** run the feature extraction cell to turn audio into numbers.
2. **Train:** run the CNN training cell.
3. **Predict:** upload your own `.wav` file and the model will tell you the emotion.

---

### **Conclusion**

this project shows that AI can understand human feelings just by listening. this can be used in call centers to see if customers are angry or in healthcare to monitor a patient's mental state.
