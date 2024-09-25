# Capstone project for AI ML

### Computer Vision for defect apple detection based on fruit 360 database

![Screenshot of Batch Apple image](https://i.imgur.com/boAPlwo.jpg)

[Link to dataset](https://github.com/sallez9/SCTPAIMLcapstone.git)

**Description of the Dataset**
The dataset used in this project is derived from the [Fruits 360 dataset](https://github.com/fruits-360) (Version: 2020.05.18.0), which is a comprehensive collection of images featuring various fruits and vegetables. The dataset is publicly available under the CC-BY-SA 4.0 license, allowing for both academic and commercial use with appropriate attribution. This dataset is organized into three main subsets: training, test, and validation, with a diverse array of classes representing different types of fruits and vegetables. For instance, in the training set, you may find separate folders for specific fruit classes, such as "apple red," "apple hit," and "apple rotten." This granularity allows for the exploration of multiple characteristics, such as freshness or damage, within a single fruit type. AI ML CV can be used to automate apple quality visual inspection via DL CNN. By analyzing images of apples, algorithms can accurately identify defects like bruises, blemishes, and wormholes, ensuring that only high-quality fruits reach consumers.

**Findings and Techniques**
To prepare the dataset for our project focused on produce quality visual inspection for fresh or defective apples, we needed to consolidate certain classes. Specifically, we aimed to merge the "apple hit" and "apple rotten" classes into a single category, which we termed "apple defect". This allowed us to simplify the task of classifying defect versus fresh apples. 
To achieve this, we used Python scripting to rename and merge the files from the "apple hit" and "apple rotten" folders into one unified directory. This step was crucial for balancing the dataset and ensuring that the classifier could distinguish between healthy and defective fruits effectively. These steps provided a solid foundation for the subsequent machine learning and computer vision tasks, ultimately contributing to more accurate fruit quality classification.
The preprocessing involved:
1. **Merge Class folders**: Create class for "fresh apples" and "defect apples". Merge "apple hit" and "apple rotten" folders into one unified defect apple directory. Similarly for fresh apple.
2. **File Renaming**: To avoid filename conflicts, we automatically renamed the files during the merging process, ensuring unique identifiers for each image.
3. **Combine Images based on Class**: Combine the images from the "apple hit" and "apple rotten" classes into "apple defect". Similarly for images from the "apple red 1", "apple red 2" and "apple red 3" classes into "apple fresh".

<details>
<summary><b>Model Training</b></summary>
  
**1. Early Stopping Prevented Overfitting:**
- The validation accuracy curve starts to plateau or even decline after epoch 3. This indicates that the model is starting to overfit the training data, learning the noise and idiosyncrasies rather than the underlying patterns.
- Early stopping at epoch 3 prevents the model from further training and overfitting, preserving its generalization ability.
  
**2. Model Performance at Epoch 3:**
- The model achieved a training accuracy of around 0.95 and a validation accuracy of around 0.95 at epoch 3. These values suggest that the model has learned the underlying patterns effectively and has reasonable generalization performance.
  
**3. Potential for Improvement:**
- While early stopping at epoch 3 prevented overfitting, it's possible that further training with careful regularization techniques (e.g., L1 or L2 regularization) could have improved the model's performance.
- Exploring different hyperparameter settings or architectural changes might also lead to better results.
  
![Accuracy and loss diagram](https://i.imgur.com/v0rKWwz.jpg)
  
</details>

<details>
<summary><b>Conclusion</b></summary>
We created a fairly accurate image classifier, as:
The model accurately predicted most of the considered apple fresh or defect categories.
The model can incorrectly label where the apples appear similar in colors and shapes, they can be challenging for the model to classify. 
  
![Screenshot of confusion matrix](https://i.imgur.com/JcQpv6h.jpg)

This can be improved by training the model with additional data using data augmentation in Keras, experimenting with adding Batch normalization to the CNN layers to improve and stabilize the learning process, adding more layers to the neural network, Adding L2 regularization, experimenting with the dropout rate, learning rate. Apart from these points, the model does a good job of classifying.
Fruit image classification can be extended to numerous practical applications, from sorting ripe fruits to detecting diseases. It offers efficiency, accuracy, and potential for optimizing inventory management in various industries. Similarly, Deep Learning can also be extended to broader plant species detection, benefiting agricultural industries.Exploring these use cases can create an awareness about potential AI projects in agricultural domain.


</details>

<details>
<summary><b>What I have learned</b></summary>
  
1. Initally, getting the dataset was the focus as our first project milestone was to secure the dataset and I was able to quickly select a popular dataset. However, my intial problem statement lack of a clear business objective that hindered progress. Dataset was further refined again and again.
  
2. Issue of biased datasets: overrepresentation of classes, if the dataset includes mostly apples from a particular farm, the model might not perform well on apples from other farms with different growing conditions or varieties.

</details>
  
**What you'd change**

- Need to add more images for better quality results. 
- There will still be a need to identify if there is an opportunity for low cost deployment 
- There is a need to ensure the ethical deployment of AI where there is no unfair job displacement to e.g. farmers.  

[Link to your LinkedIn](https://www.linkedin.com/in/zubaidah-sallehuddin/)
