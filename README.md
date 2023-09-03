# Ultrasound-Fetal-CNS-Anomaly-Detection

This project focuses on implementing a deep learning-based model capable of classifying anatomical structures in 2D fetal ultrasound images. Ultrasound imaging is a safe, accessible, and widely used method for the detection of multiple fetal anomalies. Accurate detection of planes, such as the abdomen, thorax, brain, and femur, is crucial for the correct diagnosis of fetal abnormalities.

## Annotation of Images
The dataset was annotated using Roboflow tools, ensuring accurate bounding box annotations for each of the three target fetal brain structures - MIDLINE_FALX, CSP, and CHOROID_PLEXUS. 

![Annotate](https://github.com/FozanAzhar/Ultrasound-Fetal-CNS-Anomaly-Detection/assets/95569589/d3c5b7b4-d7bd-4693-a5f2-873b5de04648)


## Data Preprocessing and Augmentation
To enhance the dataset's size and promote model generalization, data augmentation techniques were applied:

- Rotational Variations (5%-10%): These variations mimic real-world probe positioning, introducing diversity into the dataset.
- Image Blur (2.5px): This simulation of image clarity fluctuations enhances the model's robustness to varying image quality.

  ![preprocess](https://github.com/FozanAzhar/Ultrasound-Fetal-CNS-Anomaly-Detection/assets/95569589/e5e19425-7756-4cd1-8681-dc837a64c6b6)

Standardization of Image Size: All images were resized to a uniform 640x432 resolution. This adjustment not only facilitated a more efficient training process but also ensured that the model's performance was consistent across various image sizes.

## Experimental Setup 
- Data Set Split: The dataset was divided into training, validation, and testing sets using a standard split ratio. This separation allowed us to train the model on a diverse range of images and then evaluate its performance on previously unseen data.
- Utilization of Ultralytics: We utilized the Ultralytics library to streamline training, evaluation, and visualization of our <b>YOLOv8</b> model. The model was trained using the dataset, and an appropriate data split strategy was employed. The experimental setup included the selection of optimizers, loss functions, and hyperparameters to optimize model performance.

## Result

The trained YOLOv8 model exhibited promising results in detecting MIDLINE_FALX, CSP, and CHOROID_PLEXUS structures in fetal ultrasound images. The model demonstrated the ability to generalize well across images with varying degrees of zoom and rotation. Further analysis of precision, recall, and F1 scores highlighted the model's effectiveness.

![WhatsApp Image 2023-08-27 at 11 02 20 AM (1) (1)](https://github.com/FozanAzhar/Ultrasound-Fetal-CNS-Anomaly-Detection/assets/95569589/952cd7df-2ce1-45fb-8a3a-d484a79ff51e)




 

