# Image-Denoising-with-RBF-Regression
This project is created for the CSCC11: Introduction to Machine Learning and Data Mining course. It focuses on using Radial Basis Function (RBF) regression to model grayscale images and apply it to image denoising, particularly for salt-and-pepper noise. The approach represents an image as a 2D function mapping spatial positions to brightness levels and approximates this function using a set of radial basis functions (RBFs), which are smooth localized functions centered at specific positions in the image.

To remove salt-and-pepper noise, the image is divided into patches, and each patch is represented using RBFs with centers on a grid. The brightness values are learned using Least Squares (LS) regression with L2 regularization, ensuring a smooth approximation while preventing overfitting. The model is then used to estimate missing pixel values, restoring the image.

The implementation consists of:
- rbf_regression.py: Defines the RBFRegression class with methods to compute RBF values, predict pixel intensities, and fit the model using LS regression.
- image_denoising.ipynb: Runs experiments to analyze the effects of RBF width and basis function spacing on denoising performance.

The notebook compares noisy and denoised images and evaluates Mean Squared Error (MSE) across different model settings. The results highlight how adjusting RBF parameters affects denoising quality, balancing noise removal and image sharpness.
