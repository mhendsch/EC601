# Project 1 Proposal - Optimizing Athletic Performance via Wearable Health Data
## Problem Statement
In recent years, wearable health devices, such as smart watches or rings have become more and more prevalent in the fitness world. There exist many studies on how machine learning can be used to interpret this data in a way that’s useful to athletes. This project will aim to use wearable health device analytics in order to allow athletes to optimize their training specifically to improve timed trial outcomes. Specifically, I want to focus on non-professional athletes, for whom training may not be very consistent, and injury not as clear and present a danger. Previous work (see below) tends to focus on elite, professional athletes, with normal people being underrepresented in this field. 

## Prior Work
Alkasasbeh, Walaa Jumah et al. “Artificial intelligence and wearables in sport: performance, injury risk, and wellbeing.” Frontiers in artificial intelligence vol. 9 1838507. 29 May. 2026, doi:10.3389/frai.2026.1838507. https://pmc.ncbi.nlm.nih.gov/articles/PMC13260332/ 

Claudino, J.G., Capanema, D.d., de Souza, T.V. et al. Current Approaches to the Use of Artificial Intelligence for Injury Risk Assessment and Performance Prediction in Team Sports: a Systematic Review. Sports Med - Open 5, 28 (2019). https://doi.org/10.1186/s40798-019-0202-3 

Seshadri DR, Thom ML, Harlow ER, Gabbett TJ, Geletka BJ, Hsu JJ, Drummond CK, Phelan DM and Voos JE (2021) Wearable Technology and Analytics as a Complementary Toolkit to Optimize Workload and to Reduce Injury Burden. Front. Sports Act. Living 2:630576. doi: 10.3389/fspor.2020.630576. https://www.frontiersin.org/journals/sports-and-active-living/articles/10.3389/fspor.2020.630576/full 
## Proposed Approach
My proposed approach consists of 5 steps, outlined below.  These steps are general, and may need refining as I start to implement. They will likely also be split into subtasks.

### Find Wearable Health Datasets
The first step in this project will be to find datasets that have health data from wearable devices. Preferably, these datasets will have metrics such as heartrate, activity duration, activity intensity, activity type, as well as pace indicators such as average running or swimming pace. 
I’ve found one such dataset that may work [here](https://www.kaggle.com/datasets/ziya07/wearable-sports-health-monitoring-dataset), and will continue to look for more. 

### Clean/Preprocess the Data
After I have the data, I have to preprocess it. This will involve cleaning and normalizing the data, if they haven’t been already. I then have to decide which features I want to train on. As mentioned in Find Wearable Datasets, I imagine heart rate and activity details will be the most relevant. Data such as sleep score and stress levels could also prove useful.

### Choose a Model
From my research [3], it seems that Neural Networks are the most common type of model to predict athlete performance. I’ll probably end up using a neural network, but I may try other models, such as an SVM or decision tree classifier, to compare their performance. The important thing is to choose a model that can handle data with a high dimensionality, as wearable devices tend to capture many different types of data. This step will depend on the dataset I end up using. 

### Train the Model
Next, I will train the model I end up choosing on my dataset(s). In order to do this, I will split the dataset into a training set, a testing set, and a validation set. Training will be done on the training set, then evaluated on the test and validation sets. The validation set is used to fine-tune the model. We’ll continue training the model until the error gets worse on the evaluation set. Once this happens, we move on to testing (see below). I plan to use Pytorch for creating the model, including defining the forward and backward passes and the optimizer. Computing will be done on either the Shared Computing Cluster or through Google Colab’s GPUs.

### Evaluate the Model
Once the model is trained, I will test it on the testing set. The model will not be shown any of the testing set during training. It’s done this way so that the model doesn’t simply memorize the training data. We want to make sure that the model is able to generalize, and correctly process data that it hasn't seen before. If the model is able to achieve a high accuracy on the testing set, then we know that training has gone well. If not, I will tweak the hyperparameter (learning rate, optimizer, etc.) until I reach the desired model performance. 

## Milestones
- Found dataset(s) with enough parameters/data points to create an accurate model
- Cleaned and preprocessed the data
- Isolated the features that we want the model to train on
- Chose an appropriate model that can handle the data
- Possibly try multiple models and compare their performance (may be ambitious)
- Completed first rounds of training
- Completed first evaluation of model
- Fine-tune the model to increase performance
- Switch models if needs be
- Retrained and reevaluated
- Repeat until meet “Done” criteria

## What “Done” Looks Like
The project will be considered “Done” when a model has been trained that is able to predict athletic performance with a reasonable accuracy. As a stretch goal, it would be useful if the model could also offer suggestions for increasing athletic performance (this may be too ambitious, however).
