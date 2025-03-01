## Utilizing Mask R-CNN to Identify COT Starfish and Its Predators
This project applies Mask R-CNN, a deep learning model, to automatically detect and segment Crown-of-Thorns (COT) Starfish and its predators in underwater images. The goal is to aid marine conservation efforts by providing a more efficient and accurate method of identifying these species in coral reef ecosystems.

![image](https://github.com/Merihandaniel/Utilizing-Mask-R-CNN-to-identify-COT-Starfish-and-its-predators-/blob/3d2d944f17a86498ef2c77fd4d4754e6564f6ad6/Coral%20Reef.png)

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
The dataset analysis revealed that all images have dimensions of 1280 × 720, with an aspect ratio distribution of 1.78. The bounding boxindicates tha t and species label distribution indicate that the Crown-of-Thorns Starfish is the most frequently labeled species, as shown below.

![image](https://github.com/Merihandaniel/Utilizing-Mask-R-CNN-to-identify-COT-Starfish-and-its-predators-/blob/3613a96d4dea01f2a6a5a058fa73711876150a1b/Frequency%20of%20Species.png)

![image](https://github.com/Merihandaniel/Utilizing-Mask-R-CNN-to-identify-COT-Starfish-and-its-predators-/blob/2c745546a5655e9090089b1f229c16aab855f02a/Bounding%20boxes.png)

## Machine learning Models

Using logistic regression, I aimed to understand the relationship between bounding box count and species classification. However, the model struggled to accurately differentiate species, suggesting that bounding box count alone is not a strong predictor. To improve performance, I applied a random forest classifier, leveraging its ability to handle complex patterns and interactions between features. Despite this, the classification report revealed that while COT and F_coral had some predictive power, S_coral and Surgeonfish were entirely misclassified, leading to a low overall accuracy of 36%. This highlights the need for better feature selection, data balancing, or alternative models to improve species identification.

![image](https://github.com/Merihandaniel/Utilizing-Mask-R-CNN-to-identify-COT-Starfish-and-its-predators-/blob/61e31ac7cdc4a800c05d5922f27bc5815325e338/Distribution%20of%20Species%20per%20Filename.png)

Classification Report
![image](https://github.com/Merihandaniel/Utilizing-Mask-R-CNN-to-identify-COT-Starfish-and-its-predators-/blob/ce3e1d0595391de3a293238b3dd3291fff98340e/Classification%20Report.png)

## Mask R-CNN Model 

Model was found to be uncompatbible with my environemt and furthere updates were needed. 

Debugging: MRCNN model requires older versions of Python and TensorFlow to run, specifically Python 3.6.0 and TensorFlow 2.0.0. Also, Google Colab's environment only supports Python 3.8.0 and above and TensorFlow 2.15.0 and above.

