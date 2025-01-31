# Audio Based Emotion Detection
**Deep Learning Based Classification for Enhanced Emotion Recognition**  

## Overview  
Emotion detection plays a crucial role in **human-computer interaction, mental health assessment, and marketing**. This project focuses on developing an **audio-based deep learning model** to recognize human emotions from speech recordings.  

## Objective  
To enhance emotion recognition capabilities by training a **Convolutional Neural Network (CNN)** on audio data, classifying emotions into **six categories**:  
- **Sad**  
- **Surprised**  
- **Fearful**  
- **Disgusted**  
- **Happy**  
- **Angry**  

## Approach  

### 1. Dataset Selection & Preprocessing  
We utilized a **combined dataset** for better generalization:  
- **SAVEE** (Surrey Audio-Visual Expressed Emotion)  
- **RAVDESS** (Ryerson Audio-Visual Database of Emotional Speech and Song)  
- **CREMA-D** (Crowd-sourced Emotional Multimodal Actors Dataset)  

**Preprocessing steps included:**  
- Removing "Unknown" emotions.  
- Merging "Calm" with "Neutral."  
- Standardizing waveforms to **66150 samples**.  

### 2. Feature Extraction  
- **Mel spectrograms** were extracted using the **Librosa** library, providing a frequency-based representation of audio signals.  

### 3. Deep Learning Model  
A **CNN-based architecture** was used for emotion classification:  
- **Convolutional layers** with ReLU activation for feature extraction.  
- **Max pooling layers** for dimensionality reduction and overfitting prevention.  
- **Dropout layers** to improve model generalization.  
- **Dense output layer** with softmax activation for final emotion classification.  

### 4. Training & Validation  
- Dataset split:  
  - **56% Training**  
  - **14% Validation**  
  - **30% Testing**  
- **Data Augmentation:** Applied **Gaussian noise and background noise** to 40% of training data to improve robustness.  
- **Early Stopping & Model Checkpointing:**  
  - Training stops if validation accuracy does not improve for **6 consecutive epochs**.  
  - Best-performing model is saved after each epoch.  

## Results  
| Metric | Accuracy |
|--------|---------|
| Training Accuracy | **69%** |
| Validation Accuracy | **38%** |
| Test Accuracy | **37%** |

## Future Improvements  
To enhance accuracy, the following optimizations could be explored:  
- **Expanding the dataset** to cover more diverse emotional expressions.  
- **Hyperparameter tuning** for better model performance.  
- **Using transformer-based architectures** like **Wav2Vec** or **HuBERT** for improved speech emotion recognition.  
