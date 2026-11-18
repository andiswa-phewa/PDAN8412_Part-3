
# PDAN8412/w Part 3: Book Cover Classification

**Student number:** ST10123828  
**Module:** Programming for Data Analytics 2

## About the Project

For the final part of my portfolio, I developed and evaluated a Convolutional Neural Network (CNN) to classify book covers into 30 categories. This continues the publishing company scenario used in Parts 1 and 2, but focuses on recognising book categories from images.

I used the publicly available BookCover30 dataset, which contains 57,000 labelled book covers. **Apache Spark** was used to examine the dataset and check its quality, while **TensorFlow** was used to train and compare two CNN models.

## Dataset and Model Development

The original dataset contains **51,300 training images** and **5,700 test images**. For model development, I selected **15,000 images for training** and **3,000 for validation**, while keeping all **5,700 original test images** for the final evaluation.

I first examined the category distribution, missing metadata and image availability. I then trained a baseline CNN and a second model with changes to the architecture and training settings. The models were compared using validation results before the selected model was evaluated on the test set.

The baseline CNN was selected based on its stronger validation macro F1-score. It achieved **12.26% test accuracy** and a **macro F1-score of 0.0960**. These results show that the model learned some patterns in the covers, but its performance is not yet reliable enough for automatic categorisation in practice. The report discusses these findings and possible improvements.

## Running the Notebook

The project was run using **Python 3.11** in Anaconda. To reproduce the work, extract the project folder and keep the notebook, **metadata** folder and **requirements.txt** together.

Open **Anaconda PowerShell Prompt** and run the following commands:

    conda create -n pdan_cnn python=3.11 -y
    conda activate pdan_cnn
    cd "$env:USERPROFILE\PDAN8412_Part3_ST10123828_BookCover30"
    python -m pip install -r requirements.txt
    java -version
    python -m notebook

If the **pdan_cnn** environment already exists, activate it without creating it again. If the project is saved somewhere else, use that folder's location in the **cd** command. **Java 17** is needed for the Spark analysis.

In Jupyter Notebook, open **ST10123828_PDAN8412_Part3_BookCover30_CNN.ipynb** and select **Run > Run All Cells**. Save the notebook once execution is complete. CNN training may take longer on a laptop without a dedicated graphics card.

## Book Cover Images

The **metadata** folder contains the original listing files and category labels. The separate BookCover30 image archive, **title30cat.zip**, is not stored in the submission folder.

The notebook looks for the image archive on the computer and can download it to the local **PDAN8412_BookCover30_Cache** folder. Images are read directly from the ZIP, so they do not need to be extracted into the project folder.

If the automatic download does not work, the image archive can be downloaded from the researchers' Google Drive link:

https://drive.google.com/file/d/1LVWYXn2WdF-7NuLbl_LyyEwXSvIJUdPr/view

## Project Files and Outputs

The Jupyter Notebook contains the data analysis, preprocessing, model training and evaluation code, with explanations of the steps followed.

The **outputs** folder contains the saved training histories, test results, model comparison, predictions and trained CNN model. Its **figures** subfolder contains **17 numbered figures** used to support the report.

The accompanying **PDF report** presents the methodology, results, discussion, limitations and references in more detail.

The original image archive is not included with the submission because it can be obtained from the dataset source.

## Dataset Reference

Iwana, B.K., Raza Rizvi, S.T., Ahmed, S., Dengel, A. and Uchida, S. 2016. Judging a book by its cover. *arXiv preprint*, arXiv:1610.09204. Available at: https://arxiv.org/abs/1610.09204.

**Dataset repository:** https://github.com/uchidalab/book-dataset

The book cover images are provided for academic research. Copyright for the images remains with the relevant rights holders.
