# Smoker Detection using Swin Transformer

## Dataset

- **Source:** [Kaggle_Smoking](https://www.kaggle.com/datasets/sujaykapadnis/smoking)
- **Total Images:** 1120
- **Classes:** Smoker (560 images), Non-Smoker (560 images)
- **Acquisition:** Collected through search engines and various keywords
- **Preprocessing:** Resized to 250×250 resolution
- **Data Split:** 80% for training and validation, 20% for testing
- **Data Characteristics:** Smoking class includes diverse smoking poses; Non-smoking class includes some poses similar to smokers

## Data Preparation

- **Data Augmentation:** Different transformations for training and testing sets
- **Custom Dataset:** Defined a custom dataset `MyDataset` and used `DataLoader` for convenient batch loading

## Model Architecture

- **Model:** Swin Transformer
- **Modified Head:** Changed to `nn.Linear` with output features `class_size = 2` to match dataset classes

## Training

- **Optimizer:** AdamW
- **Learning Rate:** 0.0001
- **Learning Rate Scheduling:** Adjusted dynamically; milestones at epochs 7, 14, 21, 28, and 35, where learning rate becomes 0.1 times the current value (gamma=0.1)
- **Loss Function:** CrossEntropyLoss

## Testing

- **Performance Metrics:** Precision, Recall, and Accuracy
- **Good Performance:** Achieved 93% Accuracy

## Optimization Strategies

- **Hyperparameter Tuning:** Adjusted hyperparameters for better performance
- **Increased Epochs:** Extended the number of training epochs
- **Optimizer Change:** Explored different optimizers for potential improvements


