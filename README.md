# AI-Voice-recognition

The Voice Recognition project folder does not contain the audios because there is
a great number of them and it would have taken a lot of time to submit them. Because of this, you
will see that the test and train folders are empty. If you want to test feature extraction or the csv
file generation you will need to download the file from the website of the competition and insert the
audios in the respective folders.

In the Pickel folder there is supposed to be 3 files:
- preprocessed_data.pkl
- pca_preprocessed_data.pkl
- pca_200_preprocessed_data.pkl

We didn't upload those files because they are also too big. If you want to test the training models
you need to generate those files with the first block of code of each ipynb file or you can download
them here (It is faster if you download them)

https://drive.google.com/file/d/1IfGgnKAqnSaO4cKn4eJESAHtgGgrCSzj/view?usp=sharing

There are 3 ipynb files which contain similar code. The main difference is the number
of features/dimensions that each of them uses for their training and evaluation.

The best model chosen by us is MLP with 200 features/dimensions because it is the one who has got
very good results and that uses the smaller number of dimensions preventing overfitting. 

We tested our model in the test set given by the competition website, and you can see the labels that 
were inserted by the MLP with 200 features in the sample_submission.csv file. 

We created the file in the format that the competition website asked for (filename | label).

We didn't find any labels for the test set to evaluate it and see if the results were correct. So, 
if one wants to see if the model inserted a correct label, it must listen to the audios manually.

If you want to train a model by yourself follow these steps:

1. You must generate the Pickel files or download them
2. Run the "Creation of train, test and validation set" section
3. Run "Visualization of a sample" section
4. Run "Splitting of the train set into test set and training set"
5. Depending on the model you want to train, run every module of the respective model
you want to train except the block “Algorithm to select best parameters” because we only used
its output.

Example: 
If you want to train MLP run directly “Training of the model and display of the metrics” and
the rest of modules below it. If you want to see for yourself the best parameters, you can run
“Algorithm to select best parameters”.

!!!!!!Warning!!!!!!!

- Do not run the first code of each of the ipynb files unless you really want to generate the Pickel files.
It will cost a great amount of your CPU. If you want to do it anyway you will have to wait minimum 30
minutes so it can finish.

- Do not run all the modules at the same time, it will use all your cpu.

- If you see a warning before the display of the metrics of a model, it is because the 
zero_division parameter was not put into the function :

print(metrics.classification_report(y_test, predicted, labels=labels_to_include, zero_division=0))

- If you want to test the models in the 1248 file, you will have to wait a lot of time(e.g ~20 minutes for
the training of MLP model)


Author of the features and data extraction (2 first modules of each ipynb file): 

Harish Arvind SELVAKUMAR and Nissanth Nadarassin

Author of the data splitting, training and evaluation (the rest of the modules in each ipynb file) :

Ivan Arturo Grandi Flores

Thank you for reading this :)
