# BowelSegmentation-MRI

**Project Proposal: Transfer Learning and Clustering for Unsupervised Segmentation of Bowel Regions Using Multi-Modal MRI Scans**  
**Authors**: Rohith Kumar Senthil Kumar and Shweta Perumal

---

### **Summary**  
This project aims to identify bowel regions in MRI scans without needing labeled data. It uses a combination of pre-trained deep learning models (DenseNet-121/DenseNet-169) and a clustering method (K-means) to segment the images. By using models that have already learned patterns from large datasets (like ImageNet), the process is faster, more efficient, and less reliant on manually labeled medical images. If time permits, the project will explore Vision Transformers (ViT) to improve feature learning and enable self-supervised classification of bowel regions as healthy or inflamed.  

---

### **Proposed Design**  
This project aims to segment bowel regions in MRI scans without requiring labeled data. Crohn's disease is a long-term condition that causes inflammation in the gut, leading to visible changes on MRI scans. In this study, MRI scans (T1/T2-weighted and diffusion-weighted images) from Crohn's patients will be used, which helps ensure that the models learn to identify real signs of inflammation and bowel damage in a structured pipeline.
#### **Modules & Workflow**  
First, the **EDA Module** analyzes the image intensity distributions and class imbalance across the dataset using Numpy and OpenCV. The **Data Preprocessing Module** normalizes and aligns the scans with MedicalDataLoader, which applies intensity correction and normalization to ensure consistency. Next, the **Transfer Learning Module** uses pre-trained deep learning models like DynUNet or DenseNet-121 to extract important features, fine-tuned with synthetic Crohn's MRI data to improve accuracy. These features are then processed by a segmentation model built using TensorFlow. To classify bowel regions as inflamed or healthy, the **Clustering Module** groups similar features using K-Means, while the **Image Processing Module** refines the segmentation with techniques like thresholding and filtering to enhance boundary clarity. Challenges include addressing variations in scan quality, diversifying the training data using synthetic data, and minimizing computational costs through mixed-precision training

---

#### **Work Split**
 The workload will be divided between the two team members based on a peer review system. Rohith will take the lead on the technical aspects, including implementing deep learning models, clustering techniques, and image processing methods. Meanwhile, Shweta will focus on documentation, ensuring that the project is well-documented with clear explanations, methodology, and results. She will also be responsible for compiling reports, maintaining version control, and organizing findings for presentations. We will both work on Exploratory Data Analysis and review each other's work to ensure accuracy, clarity, and overall project quality.

