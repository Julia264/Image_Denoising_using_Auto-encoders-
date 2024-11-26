
# Image Denoising Using Autoencoders  

This project demonstrates how autoencoders can be used for image denoising. It leverages deep learning techniques to remove noise from images, effectively reconstructing clean versions.  

## Table of Contents  
1. [Introduction](#introduction)  
2. [Dataset](#dataset)  
3. [Methodology](#methodology)  
4. [Model Architecture](#model-architecture)  
5. [Training Details](#training-details)  
6. [Results](#results)  
7. [How to Run the Project](#how-to-run-the-project)  
8. [Dependencies](#dependencies)  
9. [References](#references)  

---

## Introduction  
Image denoising is a fundamental task in computer vision. This project uses **autoencoders**, a type of neural network, to learn representations of clean images and remove noise effectively.  

Autoencoders are trained to map noisy images as inputs to clean images as outputs, achieving denoising without requiring handcrafted filters or algorithms.  

---

## Dataset  
The dataset consists of clean and noisy image pairs. The noisy versions were generated by adding synthetic noise (Gaussian, salt-and-pepper, etc.) to clean images.  

## Methodology  
1. **Data Preparation:**  
   - Clean images are augmented with noise to create input-output pairs.  
   - Data is normalized and resized for consistency.  

2. **Model Training:**  
   - The autoencoder learns to reconstruct clean images by minimizing the Mean Squared Error (MSE) loss between output and target images.  

3. **Evaluation:**  
   - Performance is evaluated using metrics such as Peak Signal-to-Noise Ratio (PSNR) and Structural Similarity Index (SSIM).  

---

## Model Architecture  
The autoencoder consists of:  
- **Encoder:** Convolutional layers to capture essential features while compressing the image representation.  
- **Decoder:** Transposed convolutional layers to reconstruct the clean image from the encoded representation.  

### Summary:  
- Encoder: Conv2D → BatchNorm → ReLU → MaxPooling  
- Decoder: Conv2DTranspose → BatchNorm → ReLU → Output  

---

## Training Details  
- **Loss Function:** Mean Squared Error (MSE)  
- **Optimizer:** Adam (learning rate: 0.001)  
- **Epochs:** 50  
- **Batch Size:** 32  

---

## Results  
### Sample Outputs:  

 
| ![image](image.png)  |  

### Metrics:  
- PSNR: **X dB**  
- SSIM: **Y**  

---

## How to Run the Project  
1. Clone the repository:  
   ```bash  
   git clone https://github.com/yourusername/Image_Denoising_using_Autoencoders.git  
   cd Image_Denoising_using_Autoencoders  
   ```  

2. Install dependencies:  
   ```bash  
   pip install -r requirements.txt  
   ```  

3. Train the model:  
   ```bash  
   python train.py  
   ```  

4. Test the model:  
   ```bash  
   python test.py  
   ```  

---

## Dependencies  
- Python 3.8+  
- TensorFlow/Keras  
- NumPy  
- Matplotlib  
- OpenCV  



---

## References  
- **Autoencoders:** [Deep Learning by Ian Goodfellow](https://www.deeplearningbook.org/)    
- **Image Denoising Research Papers**  


