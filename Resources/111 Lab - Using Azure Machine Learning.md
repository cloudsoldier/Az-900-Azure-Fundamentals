
# Lab: Building a Machine Learning Pipeline in Azure Machine Learning Studio

## Overview
This lab focuses on building a machine learning pipeline in Azure Machine Learning Studio without writing any code. Students will use prebuilt components and datasets to train, test, and evaluate a machine learning model.

---

## Step-by-Step Instructions

### Step 1: Launch Machine Learning Studio
1. Log in to the [Azure Portal](https://portal.azure.com).
2. Navigate to **All Resources**.
3. Open your Machine Learning workspace created in the previous lab.
4. Click on **Launch Studio** to access the Azure Machine Learning Studio.

### Step 2: Navigate to Designer
1. In the Azure Machine Learning Studio, go to the **Designer** section under **Authoring**.
2. Click on **New Pipeline** to open a blank canvas for building the pipeline.

### Step 3: Add and Configure a Dataset
1. Under the **Components** tab, expand **Sample Data**.
2. Drag the **Adult Census Income** dataset onto the canvas.
3. Click on the dataset and select **Preview** to explore its attributes.
   - This dataset contains attributes such as age, work class, education, etc., and a target column for income classification.

### Step 4: Set Up Compute Infrastructure
1. Right-click on the canvas and select **Manage Compute** to open a new tab.
2. Under **Compute Instances**, click **New**.
3. Configure the compute instance:
   - **VM Size**: Select `Standard_DS11_v2`.
   - Enable automatic shutdown if desired.
   - Leave other settings as default and click **Create**.
4. Wait for the compute instance to be ready.

### Step 5: Split the Data
1. From **Components**, drag the **Split Data** component onto the canvas.
2. Connect the output of the dataset to the input of the Split Data component.
3. Click on the Split Data component and configure the split ratio to `0.7` for training (70%) and `0.3` for testing (30%).

### Step 6: Train the Model
1. Drag the **Train Model** component onto the canvas.
2. Connect the **70% training data** output from Split Data to the Train Model input.
3. Drag the **Two-Class Logistic Regression** algorithm onto the canvas and connect it to the Train Model component.
4. Configure the Train Model component to predict the **income** column.

### Step 7: Score the Model
1. Drag the **Score Model** component onto the canvas.
2. Connect the **30% testing data** output from Split Data to the second input of the Score Model component.
3. Connect the output of the Train Model component to the first input of the Score Model component.

### Step 8: Evaluate the Model
1. Drag the **Evaluate Model** component onto the canvas.
2. Connect the output of the Score Model component to the Evaluate Model input.

### Step 9: Submit the Pipeline
1. Click on **Submit** to create an experiment.
2. Provide a name for the experiment.
3. Select the compute instance created earlier.
4. Click **Submit** to run the pipeline.
5. Monitor the job progress in the **Jobs** tab.

### Step 10: Review Results
1. Once the job is complete, right-click on **Evaluate Model** and select **Preview Evaluation Results**.
2. Analyze the metrics such as accuracy, precision, and recall to evaluate the model's performance.
3. Understand the **Predicted vs Actual** comparison to see how effective the model is.

### Step 11: Clean Up Resources
1. Close the Machine Learning Studio.
2. Navigate back to **All Resources** in the Azure Portal.
3. Delete the Machine Learning workspace to remove all associated resources, including the compute instance.

---

## Key Takeaways
- Azure Machine Learning Studio enables no-code model building and evaluation.
- Pipelines provide a structured workflow for training, testing, and evaluating machine learning models.
- Proper resource cleanup ensures cost efficiency.

---

**Instructor Guidance:** Highlight the significance of splitting data and using evaluation metrics to understand the effectiveness of machine learning models. Encourage students to explore other algorithms available in the studio.
