# 📰 Automated Fake News Detection System using SAS Viya

This repository contains the complete data science pipeline and datasets for an automated **Fake News Detection System** built within the SAS Viya Model Studio environment. The project evaluates and compares three machine learning frameworks—**Support Vector Machine (SVM)**, **Forest Ensemble**, and a **Bayesian Network**—to accurately classify authentic and deceptive text streams.

---

## 📦 Repository Contents

As displayed in the file structure, this repository includes:
*   **`Fake_News_Detection.zip`**: The exported SAS Viya Model Studio project archive containing all pipeline node configurations (Data, Text Mining, and Machine Learning models).
*   **`Fake.csv.zip`**: The compressed dataset containing compiled records of deceptive news articles.
*   **`True.csv.zip`**: The compressed dataset containing compiled records of authentic news articles.

---

## 👨‍🏫 Instructions for Evaluators: How to Restore and Run the Project

Because SAS Viya separates project visual pipelines from raw storage libraries, follow these two phases to successfully link the datasets and view the executed machine learning workflows on your institutional SAS Viya account.

### Step 1: Download and Extract the Datasets
1. Download **`Fake.csv.zip`** and **`True.csv.zip`** from this repository.
2. Extract the ZIP files on your local machine to obtain the raw `.csv` data tables. 

### Step 2: Upload Data to CAS Memory
1. Log into your **SAS Viya** homepage.
2. Click the top-left **Applications Menu** (the 9-dot grid icon) and select **Manage Data**.
3. Navigate to the **Import** tab -> Click **Local files** -> Select the extracted CSV dataset file(s).
4. Ensure the target destination library is set to your active user library (e.g., `casuser`), then click **Import Item** in the top-right corner to load the data tables into active system memory.

### Step 3: Import the Project ZIP and Map the Pipeline
1. Return to the SAS Viya homepage and click **Model Studio (Build Models)**.
2. On the main Projects dashboard, click the **Import** button located in the top-right menu.
3. Select the unextracted **`Fake_News_Detection.zip`** file directly from your local downloads and confirm the import.
4. Open the newly imported project workspace. 
5. If SAS prompts that the data source is missing, click on the **Data** tab at the top of the screen, select **Change Data Source**, choose the news dataset you imported to your library in Step 2, and click **OK**.
6. Switch back to the **Pipelines** tab and click **Run pipeline** in the top-right corner. The entire workspace (**Text Mining -> SVM -> Forest -> Bayesian Network**) will automatically execute and display all validation checkmarks, ROC curves, and performance metrics.
