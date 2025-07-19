# **Micro-Hybrid Model for Indian Pines Classification**

## **Overview**

This project implements and evaluates several deep learning models for the classification of the Indian Pines hyperspectral dataset. The primary goal is to compare a baseline 3D Convolutional Neural Network (CNN) against more advanced hybrid architectures, including models with self-attention, graph convolutions, and recursive gating.

The final, optimized hybrid model incorporating a **3D-CNN with a self-attention mechanism** achieved the highest performance, demonstrating a significant improvement over the baseline. This notebook will reproduce all experiments and generate the final evaluation artifacts.

## **Requirements**

* A Google Account  
* Access to Google Colab (free tier is sufficient)

## **Setup Instructions**

1. **Create a Project Folder**: In your Google Drive, create a new folder named Micro-Hybrid\_Model.  
2. **Upload Dataset**: Download the Indian\_pines.mat and Indian\_pines\_gt.mat files and place them inside the Micro-Hybrid\_Model folder.  
3. **Upload Notebook**: Upload the main project notebook (.ipynb file) into the same Micro-Hybrid\_Model folder.

Your Google Drive folder structure should look like this:

/MyDrive/  
└── Micro-Hybrid\_Model/  
    ├── Indian\_pines.mat  
    ├── Indian\_pines\_gt.mat  
    └── your\_notebook\_name.ipynb

4. **Update File Paths**: Ensure the data\_path and gt\_path variables in the second cell of the notebook point to the correct file locations in your Drive. The default path is set to /content/drive/MyDrive/Micro-Hybrid Model for IndianPines in One Day/. You may need to update this to match your folder name.

## **How to Run**

1. Open the project notebook in Google Colab.  
2. Run the cells sequentially from top to bottom by selecting Runtime \> Run all.  
3. The first code cell will handle the installation of necessary libraries like torch-geometric and faiss-cpu.  
4. The second code cell will prompt you to authorize Google Drive access. Please follow the on-screen instructions.  
5. The entire script, including the training of all four models, will complete in **under 1 hour** on a standard Colab free-tier instance.

## **Expected Output**

After the notebook has finished running, the following will be generated:

* **Printed Metrics**: The final cells will print the detailed performance metrics (Overall Accuracy, Average Accuracy, Kappa, and a classification report) for each of the four models.  
* **Generated Files**: The following image files will be saved to your Colab session's local storage. You can download them from the file browser on the left-hand side.  
  * confusion\_matrix.png  
  * tsne\_plot.png  
  * prediction\_map.png