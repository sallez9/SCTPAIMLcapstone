# Capstone project for AI ML

### Computer Vision for defect fruit detection based on fruit 360 database

![Screenshot of dashboard](https://i.imgur.com/UujCjhB.png)

[Link to dataset](https://github.com/sallez9/SCTPAIMLcapstone.git)

**Description of the Dataset**
The dataset used in this project is derived from the [Fruits 360 dataset](https://github.com/fruits-360) (Version: 2020.05.18.0), which is a comprehensive collection of images featuring various fruits and vegetables. The dataset is publicly available under the CC-BY-SA 4.0 license, allowing for both academic and commercial use with appropriate attribution.

This dataset is organized into three main subsets: training, test, and validation, with a diverse array of classes representing different types of fruits and vegetables. For instance, in the training set, you may find separate folders for specific fruit classes, such as "apple red," "apple hit," and "apple rotten." This granularity allows for the exploration of multiple characteristics, such as freshness or damage, within a single fruit type.

**Findings and Techniques**
To prepare the dataset for our project focused on produce quality inspection for fresh or defective apples, we needed to consolidate certain classes. Specifically, we aimed to merge the "apple hit" and "apple rotten" classes into a single category, which we termed "apple defect". This allowed us to simplify the task of classifying defect versus fresh apples.
To achieve this, we used Python scripting to rename and merge the files from the "apple hit" and "apple rotten" folders into one unified directory. This step was crucial for balancing the dataset and ensuring that the classifier could distinguish between healthy and defective fruits effectively. These steps provided a solid foundation for the subsequent machine learning and computer vision tasks, ultimately contributing to more accurate fruit quality classification.
The preprocessing involved:
1. **File Renaming**: To avoid filename conflicts, we automatically renamed the files during the merging process, ensuring unique identifiers for each image.
2. **Merging Classes**: We wrote Python code to combine the images from the "apple hit" and "apple rotten" classes into "apple defect".

<details>
<summary><b>Foldable hidden section</b></summary>

Any folded content here. It requires an empty line just above it!

</details>

What you learned

What you'd change

Link to your LinkedIn
