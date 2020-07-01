# Dance-Form-Classification-via-Transfer-Learning
### 1) This Image Classification is done via Transfer Learning, Pre_trained model used is InceptionV3.
### 2) There are number of ways shown to approach this problem in this notebook.
### 3) The approached which is used is:
				#### Transfer Learning with InceptionV3 :-
				(a) Training Images and target class lables are appended to list data strutures respectively.
				(b) Same is done for validation images.
				(c) Target class lables are lable encoded using sklearn, and then further ahead they are One Hot Encoded using Keras.
				(d) Training Data is split into train and test using sklearn's train_test_split.
				(e) Data Augmentation is done using Keras's ImageDataGenerator and also training, testing and validating data is converted to numpy array's.
				(f) Next, parameters of pre-trained model is defined and the pre-trained model is set to not trainable.
				(g) a Sequential model is defined on top of pre-trained model consisting of:
													(A) Flatten Layer--1
													(B) Dropout Layer--2													
 													(C) BatchNormalization--2
													(D) Dense Layer with Relu and Softmax as activation functions respectively.
													(E) Optimizer = Adam , loss = categorical_crossentropy 
													(F) Callbacks : ModelCheckpoint,PlotLossesKeras,ReduceLROnPlateau
### 4) Alternative methods shown in the notebook are :
						(a) Data Augmentation using with ImageDataGenerator's flow_from_datafram(). 	
						(b) Functional API Model over a pre-trained model.
						(c) A CNN Sequential Model build from scratch.
						(d) Writing to a .csv file row-wise.

5) Model is saved as a json string in file 'model.json'.
6) Output is saved on a .csv file named 'results.csv.
														
					

