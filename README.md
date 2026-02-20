# 🐾 Conser-Vision: Wildlife Image Classification

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1BFT6Bs6LAmnId9woAffZF_dpoFicxeON?usp=sharing)

## 📌 Project Overview
This project was developed for the DataDriven "Conser-Vision" competition. The objective is to build a Machine Learning model that automatically classifies camera trap images from a wildlife conservation project into one of 8 categories (7 distinct species and 1 "Blank" category). 

## 💼 Business Impact & Use Case
Currently, classifying these trail camera images requires significant manual effort from conservation employees. By automating this image classification process, the model:
* **Reduces Labor Costs:** Significantly cuts down the man-hours spent on manual data entry.
* **Reallocates Resources:** Allows conservation staff to refocus their time on high-value tasks like fieldwork, gathering data, and implementing strategies.
* **Directs Conservation Efforts:** Helps rapidly identify vulnerable species in the forest to better direct organizational resources.

## 🧰 Tech Stack
* **Language:** Python
* **Deep Learning Frameworks:** TensorFlow / Keras / PyTorch 
* **Model Architectures:** Feed Forward Neural Network, EfficientNet (Transfer Learning), Convolutional Neural Network (CNN)
* **Environment:** Google Colab

## 🧠 Methodology & Model Evaluation
The study evaluated three distinct neural network architectures to identify the most effective solution for processing grid-like image data:

1. **Baseline Feed Forward Model:** Flattens input data into a single list, which destroyed the spatial structure of the pixels.
2. **EfficientNet (Transfer Learning):** Utilized a base network pre-trained on a large image dataset. The top layers were replaced with a global pooling layer, dense layers, and a softmax output to adapt to our specific classes. 
3. **Custom CNN (Winning Model):** Preserved spatial hierarchies using learnable filters (kernels) to detect local patterns like fur textures or snouts. 
   * *Hyperparameters:* Batch size of 64, 20 epochs, Average Pooling, and the Adam optimizer.

## 📈 Results
The custom CNN emerged as the optimal solution, significantly outperforming the pre-trained EfficientNet model.

| Model | Accuracy Score |
| :--- | :--- |
| Feed Forward (Baseline) | 25.71% |
| EfficientNet | 82.42% |
| **Convolutional Neural Network (CNN)** | **96.68%** |

**Competition Performance:** This model was submitted to the DataDriven platform, achieving a Log Loss score of **2.9475** and ranking **#472**.

## 🔮 Future Improvements
While the CNN achieved near-perfect classification capabilities, future iterations could explore:
* Conducting broader testing with Max Pooling compared to Average Pooling.
* Experimenting with different optimizers beyond "Adam" to potentially increase accuracy in higher epoch models.

---
**Author:**
Shubh Parekh
* MS in Business Analytics | Data Analyst
* [LinkedIn](https://www.linkedin.com/in/shubhparekhwsb/) | [GitHub](https://github.com/Shubh-3012)
