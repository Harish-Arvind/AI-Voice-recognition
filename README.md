# AI Voice Recognition

Welcome to the AI Voice Recognition project!

### Overview

The Voice Recognition project folder does not include audio files due to the large number of them, which would have made uploading time-consuming. As a result, the **train** and **test** folders are empty. To test feature extraction or generate CSV files, you will need to download the audio files from the competition website and place them in the respective folders.

### Required Files

In the **Pickle** folder, there should be 3 files:

- `preprocessed_data.pkl`
- `pca_preprocessed_data.pkl`
- `pca_200_preprocessed_data.pkl`

Due to their large size, these files have not been uploaded. You can either generate them by running the first block of code in each notebook (`.ipynb` file) or download them directly from the following link for faster access:

[Download Pickle Files](https://drive.google.com/file/d/1IfGgnKAqnSaO4cKn4eJESAHtgGgrCSzj/view?usp=sharing)

### Notebooks Overview

There are 3 Jupyter notebooks included, which contain similar code with the main difference being the number of features/dimensions used for training and evaluation. 

The best-performing model, chosen based on results, is the **MLP** (Multi-Layer Perceptron) with 200 features, as it achieved great results while minimizing the risk of overfitting by using fewer dimensions.

The model was tested on the test set provided by the competition website. You can find the predictions made by the MLP model with 200 features in the `sample_submission.csv` file, formatted as requested by the competition (filename | label).

Please note: We did not have access to the true labels for the test set, so to verify the accuracy of the model’s predictions, you will need to manually listen to the audios.

### Steps to Train Your Own Model

To train the model yourself, follow these steps:

1. **Generate or Download the Pickle Files** (as mentioned above).
2. **Run the "Creation of Train, Test, and Validation Set" Section.**
3. **Run the "Visualization of a Sample" Section.**
4. **Run the "Splitting of the Train Set into Test and Training Set" Section.**
5. Depending on the model you wish to train, run the relevant modules, skipping the block titled “Algorithm to Select Best Parameters,” which is only used for selecting optimal parameters.

**Example:** 
- If you want to train the **MLP** model, run the "Training of the Model and Display of Metrics" section, along with the subsequent modules. 
- If you want to find the best parameters, run the "Algorithm to Select Best Parameters" section.

### Important Notes:

- **Do not run the first code block** in any of the `.ipynb` files unless you want to generate the Pickle files. This will be very resource-intensive and can take up to **30 minutes** or more.
- **Avoid running all modules simultaneously** as it will utilize a large portion of your CPU.
- If you encounter a warning before the model metrics are displayed, it is because the `zero_division` parameter was not added to the classification report function:

  ```python
  print(metrics.classification_report(y_test, predicted, labels=labels_to_include, zero_division=0))
  ```

- Testing the models on the full dataset (1248 files) can take a significant amount of time. For example, **MLP** training could take around **20 minutes**.

### Acknowledgments

- **Feature extraction and data preparation** (first two modules of each notebook) by:  
  **Harish Arvind SELVAKUMAR** and **Nissanth Nadarassin**.
  
- **Data splitting, training, and evaluation** (remaining modules in each notebook) by:  
  **Ivan Arturo Grandi Flores**.

Thank you for your interest in this project!

---

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/Harish-Arvind/AI-Voice-recognition/blob/main/AI%20Voice%20recognition/LICENSE) file for details.
