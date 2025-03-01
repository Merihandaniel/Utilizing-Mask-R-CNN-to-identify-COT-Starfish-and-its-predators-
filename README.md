## Utilizing Mask R-CNN to Identify COT Starfish and Its Predators
This project applies Mask R-CNN, a deep learning model, to automatically detect and segment Crown-of-Thorns (COT) Starfish and its predators in underwater images. The goal is to aid marine conservation efforts by providing a more efficient and accurate method of identifying these species in coral reef ecosystems.

## Technologies Used
- **Mask R-CNN** (Deep Learning)
- **TensorFlow** / **Keras**
- **OpenCV** for image processing
- **Python** (programming language)
- **Jupyter Notebooks** for development and analysis
- **Matplotlib** / **Seaborn** for data visualization

## Dataset 
https://www.kaggle.com/c/tensorflow-great-barrier-reef

## Exploratory Data Analysis
The dataset analysis revealed that all images have dimensions of 1280 × 720, with an aspect ratio of 1.78. The bounding box size distribution indicates that most detected objects, such as the Crown-of-Thorns Starfish, are relatively small, with the majority of bounding boxes ranging between 0 and 10,000 pixels in area, peaking around 4,000 pixels. Larger bounding boxes (above 10,000 pixels) are rare, suggesting that the starfish and other objects of interest are typically small in the images. The species label distribution further indicates that the Crown-of-Thorns Starfish is the most frequently labeled species, as shown below.

![image](https://github.com/Merihandaniel/Utilizing-Mask-R-CNN-to-identify-COT-Starfish-and-its-predators-/blob/3613a96d4dea01f2a6a5a058fa73711876150a1b/Frequency%20of%20Species.png)

![image](https://github.com/Merihandaniel/Utilizing-Mask-R-CNN-to-identify-COT-Starfish-and-its-predators-/blob/2c745546a5655e9090089b1f229c16aab855f02a/Bounding%20boxes.png)

## Machine learning Models

Using logistic regression, I aimed to understand the relationship between bounding box count and species classification. However, the model struggled to accurately differentiate species, suggesting that bounding box count alone is not a strong predictor. To improve performance, I applied a random forest classifier, leveraging its ability to handle complex patterns and interactions between features. Despite this, the classification report revealed that while COT and F_coral had some predictive power, S_coral and Surgeonfish were entirely misclassified, leading to a low overall accuracy of 36%. This highlights the need for better feature selection, data balancing, or alternative models to improve species identification.

![image](https://github.com/Merihandaniel/Utilizing-Mask-R-CNN-to-identify-COT-Starfish-and-its-predators-/blob/61e31ac7cdc4a800c05d5922f27bc5815325e338/Distribution%20of%20Species%20per%20Filename.png)

![image](https://github.com/Merihandaniel/Utilizing-Mask-R-CNN-to-identify-COT-Starfish-and-its-predators-/blob/ce3e1d0595391de3a293238b3dd3291fff98340e/Classification%20Report.png)

## Mask R-CNN Model 
The model was found to be incompatible with my current environment, necessitating further updates for compatibility.

Debugging Insights: The Mask R-CNN (MRCNN) model requires older versions of Python and TensorFlow to operate effectively, specifically Python 3.6.0 and TensorFlow 2.0.0. However, Google Colab’s environment only supports Python 3.8.0 and above, along with TensorFlow 2.15.0 and higher, creating a version mismatch that prevents seamless execution.

