# QR Code Authentication: Detecting Original vs. Counterfeit Prints

## **Project Overview**
This project focuses on building a machine learning model to classify QR codes as either **"first print" (original)** or **"second print" (counterfeit)** based on subtle differences in print quality, microscopic patterns, and degradation. The model utilizes both **traditional machine learning (SVM)** and **deep learning (CNN)** approaches to detect counterfeit QR codes effectively.

## **Dataset Description**
The dataset consists of:
- **First Prints**: Original QR codes with embedded Copy Detection Patterns (CDPs).
- **Second Prints**: Counterfeit versions created by scanning and reprinting the first prints.

📌 **Dataset Link**: [Google Drive](https://drive.google.com/drive/folders/1pPeWT1zntlKXnuY_yHmpI-ZzKl4nLgQS?usp=drive_link)


## **Steps to Run the Project**
### **1. Data Exploration & Preprocessing**
- Load images
- Visualize first and second prints
- Extract key features (ORB, SIFT, pixel differences)

![image](https://github.com/user-attachments/assets/c1b032d9-8988-4067-aba9-fef2eb3db537)

### **2. Train Machine Learning Model (SVM)**
- Extracts image features
- Trains an **SVM classifier**
- Evaluates using accuracy, precision, recall, and F1-score

### **3. Train Deep Learning Model (CNN)**
- Converts images into grayscale
- Trains a **Convolutional Neural Network (CNN)**
- Evaluates model performance

### **4. Evaluate & Compare Models**

- Confusion matrix and classification reports are saved.

## **Results & Evaluation**
📌 **Final Model Accuracy**: **100% on test data**  
📌 **Metrics:**
```
              precision    recall  f1-score   support

           0       1.00      1.00      1.00        21
           1       1.00      1.00      1.00        19

    accuracy                           1.00        40
   macro avg       1.00      1.00      1.00        40
weighted avg       1.00      1.00      1.00        40
```
📌 **Confusion Matrix:**
```
[[21  0]
 [ 0 19]]
```

## **5. Deployment Considerations**
- **Optimize the model for real-world usage** (e.g., TensorFlow Lite, ONNX).
- **Handle different scanning conditions** (noise, distortions, etc.).
- **Integrate with a QR code scanner for real-time authentication.**


## **License**
This project is licensed under the MIT License.

