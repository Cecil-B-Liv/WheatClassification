First in order to run anything in this file, you must extract the models.zip folder which include the models thats needed for the application:
Extract the models.zip to 2 locations:
a. For the local application:
extract the models.zip so its in form off: 
_____Local
  |________database
	|_________models
		|_______Task1
		|_______Task2
		|_______Task3	

b. For the web application
_____Web
  |________database
	|_________models
		|_______Task1
		|_______Task2
		|_______Task3	

And you need to put the zip image dataset of test_images.zip provided to model/dataset so its in form of:
	|_________model
		|__________dataset
			|___test_images.zip

If you want to run the script to load model and predict the data from test images directly, you need to navigate to model\dataset, extract the test_image folder so that its in form of: 
	|_________dataset
		|__________test_images
			|___200001.jpg
			|___200002.jpg
			|___....

You also need to put two of the zip image dataset provided to model/zip_data so its in form of:
	|_________model
		|__________zip_data
			|___test_images.zip
			|___train_images.zip


1. For the jupyter file:
For the 3 tasks file code, navigate to the 'model' folder, then you will see there's 4 ipynb file which is: 
- Task1_Disease.ipynb (holds the code for training task 1 model)
- Task2_Variety.ipynb (holds the code for training task 2 model)
- Task3_Age.ipynb (holds the code for training task 3 model)
- model_load_to_predict.ipynb (holds the script for loading model and extract answer to prediction file)

Here you will also see:
- 'dataset' folder which holds the extracted images from the given dataset. 
-'zip_data' is the place which holds the zip data thats the assignment has given us.
- 'saved_model' is the place which holds the model output from the training jupyter file. 
- 'opencv' is the place that has the meta_train.csv
- 'logs' is the place which has the training log and 'prediction' is the place that used to hold the prediction file (which you dont need to care a lot)

2. For the GUI code, there's two version:
- Folder 'Local' that has the GUI Application which run on your own computer. (Navigate to the readme-instruction file to see more in details, install all the library and tool just like the backend requirements, then at following until step 5 of the last headline)

- Folder 'Web' that has the GUI Application which will deploy a website for other devices to access. (Navigate to the readme-instruction file to see more in details)

