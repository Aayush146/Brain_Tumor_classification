# Brain_Tumor_classification


To use the code files provided, please follow the instructions carefully. 

The AMLS_dataset_loader file is the first file to load. It contains the dataset classes built using pytorch. Please download the dataset from the folllwing link:

'''' https://www.kaggle.com/competitions/rsna-miccai-brain-tumor-radiogenomic-classification/overview''' 

The link will take you to the kaggle competition. Please download the training datset and its subsequent CSV file only. Download both file in the same folder so that it is easier to process the data. 


Dataset loader file:

1. First pip install pydicom, a libary used to read the MRI images.
2. Load the class for the datasets. If you structure your dataset files correctly there should not be any issues 

''' please note - I have used google collab pro to gain access to the reserved GPUs and higher RAM. there will be issues with loading the data into momory for the model intrepretability code'''


AMLS_neural_net file 

1. For this py file, you will also need to install pydicom and captum ( pytroch model interpretation library
2. there is a step where I import the dataset oader file. For this please change the file path in the arguement for os.chdir() to where you have stored the dataset loader file. 
3. load the datasets, this should require two important arguements, the patient files and the labels csv file. For the base_path_x arguement, use a path until the training folder whihc contains all the patient folders. For the label file, direct it to the downloaded label file. 
4. load all three classes of the neural neural net, these were used for finding the optimum number of convolutional layers. Please note if you are using google colab, set the runtime hardware to GPU as it is called along the code. 
5. for the grid search algorithm, create an object of the CRNNnet3 class ( already there) and then run the cell or code block for the Grud search algorithm. 
6. The rest of the bloacks should run smoothly from here.Howeevr, there will be issues regarding the memory. 
