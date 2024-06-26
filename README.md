# Artificial-Vs-Real-World-datasets
In the field of artificial intelligence and machine learning, this study compares models trained on synthetic and real-world datasets. Through a rigorous assessment of model performance, robustness, and generalization ability in various circumstances, we explore the viability and effectiveness of artificial data in machine learning applications. We address fundamental problems about robustness to adversarial inputs, predicting accuracy, and biases present in synthetic data through empirical study. Our results give insightful counsel for practitioners and researchers navigating the ever-changing field of AI techniques, enabling them to make well-informed decisions and pave the way for future developments in the field.

## Experimental SETUP

We utilized a convolutional neural network (CNN) architecture consisting of twelve layers, comprising three dense layers and nine convolutional layers. The CNN model is composed of convolutional layers, which are followed by classification dense layers, regularization dropout layers, and max-pooling layers.

## THE Datasets

This study uses two datasets, one containing generated images and the other real-world photographs. The dataset containing real-world images is called FER2013. 35000 grayscale, 48 * 48 pixel images of faces depicting a range of emotions are included in the dataset. The photos are divided into test and train folders. 
The other dataset used is called SFHQ, and it consists of artificial images. 89,785 well selected 1024 × 1024 curated face pictures (not divided into test and train folders) are included in the SFHQ dataset.

## CHANGES MADE TO THE DATASETS 
To expand the size of the train dataset for the FER0213 dataset, we consolidated the two folders into a single train folder.
While using SFHQ, a state-of-the-art dataset with synthetic photos, for our research, we ran into a few problems. First off, the FER2013 dataset classifies the images into seven unique folders according to the main emotion they represent, but the SFHQ dataset does not classify the images.
Secondly, because the SFHQ dataset is significantly larger than FER2013, conducting a comparative analysis was problematic. Therefore, based on the main emotion that each image conveyed, we first divided the photos in the SFHQ dataset into seven folders: happy, sad, fear, surprise, discrete, neutral, and angry. 
Next, we randomly selected photographs from these folders based on the subsequent folders in the FER2013 dataset, ensuring that each subfolder in both datasets contained the same amount of images. For instance, the cheerful folder in the SFHQ folder contained 10497 photos, compared to 8989 in the FER2013 dataset. In order to train the model, we randomly selected 8989 photos from that collection and copied them into a new folder.
Lastly, we used Affectnet, a different comparable dataset, to analyze both models.

RESULTS
The results of our comparison analysis with both artificial and real-world datasets are presented in this section. Among the performance measures that were calculated using the "sklearn.metrics" module are precision, recall, f1 score, accuracy, weighted average, and macro average of those metrics.
First, we made adjustments to the models using different batch sizes and epoch counts. There were forty, fifty, sixty, seventy, and eighty epochs tested. However, a thorough analysis of the learning curve and performance metrics showed that 50 epochs was the ideal amount of time for our region. There was no appreciable shift in the classification accuracy after 50 epochs.Our study's conclusions demonstrated that, when it came to classifying the emotions conveyed by the photographs, the model trained on the real-world dataset (FER2013) performed better than the model built on the fake dataset (SFHQ). The model trained on the simulated dataset had a macro average precision of 0.66, while the model trained on the real-world dataset had a macro average precision of 0.75. The experiment's precise performance metrics that yielded the best results are displayed in the image below. Real-world datasets fared significantly better than fictitious datasets on all performance matrices. Artificial datasets can still be used, nevertheless, in situations where privacy is a concern or there are relatively few real-world datasets accessible.

