# Pediatric-Pneumonia-Predicition


## Introduction

This model predicts whether or not a child has pneumonia and if so, is it bacterial or viral pneumonia. This kernel is part of an end to end ml solution - starting with a model . This Kaggle dataset was set up as a binary classification problem - pneumonia or no pneumonia. I found that the images had file names containing normal, bacteria or virus so I extracted these and used them as target classes to create a 3 class classification problem - Normal, Viral, Bacterial.

This solution uses transfer learning applied to a MobileNet model. All training was done in this kernel. MobileNet was designed for the web. It is small (aprox. 35MB) and runs fast.

## Findings

From the resulting confusion matrix and classification report it appears that the model is very good at predicting whether or not pneumonia is present, however it also seems to be more likely to predict bacterial pneumonia than viral pneumonia. Initially I was going to try to reduce this sensitivity to bacterial pneumonia but I decided not to do this. Because bacterial pneumonia is more serious than viral pneumonia I left the model as is.

One piece of information that would be good to have is an estimate of human level performance on this task. An F1 score of a Radiologist's ability on this dataset would allow a realistic assessment to be made of this model's performance. The developers of CheXNet used this approach to determine their model's performance. They computed the average F1 score of 4 Radiologists and compared it to CheXNet's F1 score.
