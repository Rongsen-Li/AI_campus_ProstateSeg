# AI_campus_ProstateSeg
AI campus prostate segmentation repo (training)

# Instructions for Setup

### 1. Install Anaconda Navigator

To get started with running the Jupyter notebook and working on the medical image segmentation project, you’ll first need to install Anaconda.

You can use any IDE you prefer (Visual Studio or Anaconda Navigator). If you would like to get started on Anaconda Navigator:

 Install Anaconda from the official website using this [link](https://www.anaconda.com/products/navigator) for your operating system (Mac, Windows, etc.). Once you follow the steps, verify the installation by printing the conda version using the following command in your terminal:

```bash
    conda --version
```

### 2. Clone this repository

Clone this repository to your local machine to access the jupyter notebooks, python files and the configuration yaml file. If you do not have git installed, follow these [instructions](https://git-scm.com/downloads) to install git for your operating system. In order to clone the repository, open terminal and navigate to the directory where you want to save the codebase. Run the following command to clone the repository. Alternatively, you could download the zip file. 
```bash
    git clone https://github.com/TheOmarLab/AI_campus_ProstateSeg.git
```
<img width="429" alt="image" src="https://github.com/user-attachments/assets/d7e8271a-2873-401b-aa7d-4e2c89565d81" />

### 3. Install required dependencies and run the configuration yaml file

To ensure all necessary libraries are installed to run the Jupyter notebooks, we will use a configuration yaml file that installs all the dependencies required for the project. This yaml file is located in the main directory of the repository. Run the following command to create a new conda environment using the configuration yaml file:
```bash
    cd AI_campus_ProstateSeg
    conda env create -f config.yaml
```
This will create a new environment and install all the required dependencies. Once the environment is created, activate it by running the following command:
```bash
    conda activate semantic-segmentation-prostate-cancer-biopsy-tissue-deep-learning
```
After activation, you should see the environment name at the beginning of your terminal prompt, indicating that the environment is active. Verify that the dependencies have been installed by running any of the Jupyter notebooks -- especially the very first few cells that import the packages. If any of the packages are not installed, run the following command(s) to install them using pip or conda:
```bash
    conda install <package-name>
```
```bash
    pip install <package-name>
```

### 4. Download subset of the PANDA dataset

Through the modules in the Jupyter notebooks, we will be interacting with and analyzing a subset of the [PANDA dataset from Kaggle](https://www.kaggle.com/competitions/prostate-cancer-grade-assessment/data). The subset of training and test images/masks has been shared through share point in the `sample_data` folder. In case you did not get the link, the data can be accessed [here](https://cedarssinai-my.sharepoint.com/:f:/r/personal/priyanka_vasanthakumari_cshs_org/Documents/AI_campus_team6?csf=1&web=1&e=41HsKL). Copy the `sample_data` folder in the `notebooks` folder where the other jupyter notebooks and python files are located. There are 10 image and mask files located in `train_images` and `train_label_masks`, and 5 image and mask files in `test_images` and `test_label_masks`. The test folder data has been sampled from the `train_images` and `train_label_masks` folders of the [Kaggle challenge dataset](https://www.kaggle.com/competitions/prostate-cancer-grade-assessment/data) as well, but it is different from the training dataset in `sample_data`. They are both selected from the Radboud study. 

### 5. Open Anaconda Navigator.
In the Environments tab on left, select the semantic-segmentation-prostate-cancer-biopsy-tissue-deep-learning environment that you created. Then go to Home and launch JupyterLab (You may have to install it first). This will launch a Jupyter notebook session in your browser. You should be able to open the directory that you cloned with the notebook and sample data within the Jupyter Notebook session.

### 5. Run the first module on loading slides and masks

In order to verify data setup, run the first notebook (`Module 1 Load Slides and Masks`) and print out the image and mask files. 

