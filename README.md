# Hackerearth-DL-competitions
Hi,
I am a Machine learning/Deep learning enthusiast, student at IIT-Guwahati,branch : Mtech in Signal Processing and Machine Learning.
This repository contains Machine Learning/Deep Learning (python) code for hackerearth Dance form competition (Classification Challenge)!!
U may find the extended dataset link below and also in the notebook containing 944 training images and 156 test images .I have trained my deep learning model with a smaller subset of this dataset which was provided in competition which was (364 train images and 156 test images) and achieved a total score of 79.5 and a rank of 169/5864 on the leaderboard. 
I have also attached the google colab notebook(Dance_DL.ipynb) and python(Dance_DL.py) file, where u can find this implementation. 

public Dataset link = https://www.kaggle.com/raoofnaushad/indian-dance-forms-1000/download

The following are the description points regarding the hyperparameters used which gave me better results and model layers description:
1. The model was based on Transfer Learning and the base_model used was ResNet50.
2. Target shape of Images were made (224x224x3).
3. Out of 181 layers in base_model it as fine tuned from layer no 160. i.e layers 0 to 160 were not trainable and from 160 onwards they were trainable.
4. Output of the base_model was GlobalavgPooled2d().
5. Followed by a Dense layer with 256 'relu' activation units and a Dropout rate of 0.3.
6. Followed by a Dense layer with 128 'relu' activation units and a Dropout rate of 0.3.
7. Followed by an final output Dense layer with 8 'softmax' activation units.
8. Model is compiled with a optimizer = Adam, learning_rate = 0.0001, loss = 'sparse_categorical_crossentropy',metrics = ['accuracy'].
9. 5 Fold cross-val-score is computed and its avg mean and std_dev is printed to know the varience of train data for different training and testing inputs.
10. Model is trained with a batch_size = 128 and epochs = 50.
