# Emotion Recognition
## _Image Classification using CNN's_

I train convolutional neural networks to classify the emotions depicted in frontal face images. In this sample of 11,000+ images, each was be labelled as depicting either anger, disgust, fear, happiness, neutral, or sadness.

[Please find my analysis and modelling here](Emotion_Recognition.ipynb), which I performed in Google Colab.

### My Optimal Model
My optimally accurate model achieved a test score of `0.8839`. A few of its most common misclassifications of depicted emotions were revealed in the confusion matrix:
- Fear misclassified as disgust.
- Fear misclassified as Happiness.
- Happiness misclassified as fear.

#### Interpreting the Misclassification
Musing on this, I speculate that fear and happiness might be commonly confused for each other because they are both very high energy. They might also be alike in how their facial expressions share widened eyes, often.

When I reflect on the mutual misclassification of fear and disgust, I try to consider these emotions' likeness and first think of the repulsion they share.

### Conclusions

This being a classification task that was thin on exploration, my conclusions primarily relate to my recalibrations in the iterative modelling process:
- Lowering the image size benefitted both the runtimes _and the accuracies_ of my models. Surprisingly, raising the batch size only marginally decreased my runtimes, and with considerable cost to accuracy.
- The models that incorporated regularization measures, which here were the DropOut and BatchNormalization layers, appeared to have greatly benefitted therefrom.
- 


### Process Details

To determine a fitting architecture for this neural network classifier, I performed eight iterations of lengthy model-training. For each new training, I made one of the following adjustments:
- Lowering the image size
- Raising the batch size
- Hypertuning, using the Keras tuner
- Using early stopping
- Adding epochs
- Adding batch normalization and dropout layers, for regularization

From the evaluation of these models' performances, I identified one model as optimally accurate. But as I speculate in the discussion section, it might well have benefitted from the regularizing adjustments that were enjoyed by two other models. It might also have well benefitted from an additon of epochs in training. additional epochs of training I speculate in discussion that it could have benefitted from 

Following the training, the models were evaluated on validation and test datasets. From these results, I determined an optimal model and examined its confusion matrix from test. 

<br></br>

This work was a final project that I completed for the course _CSC 578 (Neural Networks and Deep Learning)_ at DePaul, where I earned an MS in Computer Science.
