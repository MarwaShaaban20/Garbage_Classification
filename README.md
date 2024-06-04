# Garbage Classification with Genetic Algorithm Feature Selection

## Dataset

The dataset should be organized in the following structure:
```
/path/to/dataset/
    /train/
        /cardboard/
        /glass/
        /metal/
        /paper/
        /plastic/
        /trash/
    /validation/
        /cardboard/
        /glass/
        /metal/
        /paper/
        /plastic/
        /trash/
```

## Model Training

The training process involves the following steps:

1. **Data Augmentation**: Using `ImageDataGenerator` for augmenting the training images.
2. **Feature Extraction**: Utilizing a pre-trained MobileNet model to extract features from the images.
3. **Classification**: Using a Support Vector Machine (SVM) to classify the extracted features.
4. **Feature Selection**: Implementing a Genetic Algorithm to select the most relevant features.

## Genetic Algorithm for Feature Selection

A custom Genetic Algorithm class is used to optimize the feature selection process. The algorithm involves:

1. **Initialization**: Creating a random population of solutions.
2. **Evaluation**: Assessing each solution's fitness based on SVM classification accuracy.
3. **Selection**: Using tournament selection to choose parents for the next generation.
4. **Crossover**: Performing single-point crossover to generate offspring.
5. **Mutation**: Applying bit-flip mutation to introduce variability.
6. **Iteration**: Repeating the process for a specified number of generations to find the best feature subset.

## Evaluation

The model's performance is evaluated using accuracy, precision, recall, and F1-score metrics. A confusion matrix is also plotted to visualize the classification results.

## Results

The selected features and the final classification accuracy are displayed, showcasing the effectiveness of the Genetic Algorithm in improving the model's performance.



