# Operationalising Machine Learning Project

In this project we use the Bankmarketing dataset and Azure to configure a cloud based machine learning production model, deploy it and consume it. We also use a Jupyter Notebook and the Python SDK to create, publish and consume a pipeline. 

## Architectural Diagram
The main steps of the project can be seen in the image below.
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/ArchitecturalDiagram.png)

First, we create a service principal and allow it access to the workspace. Next we use AutoML to determine the best model on the Bank marketing dataset. The third step is to deploy the model to an Azure Container Instance. We then enable logging by enabling Application Insights. In the fifth step swagger is used to generate documentation and finally we consume the model using the rest endpoint. In the seventh step a Jupyter notebook is used to create, publish and consume a pipeline.

## Further Project Improvements
Use manual feature selection to improve the model performance.


## Key Steps
### Step 1: Authentication 
In this step we create a service principal and allow it access to the workspace. This enables authentication with automation so that the system does not stop to wait for the user to input a password. In the screenshots below you can see that a service principal has been created and that the az ml workspace share command excutes successfully with no errors
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/ServicePrincipleCreateed.png)
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/AuthenticationProof.png)

### Step 2: Create AutoML Run
We create an AutoML experiment using the Bank marketing dataset. The dataset can be seen in the following screenshot.
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/DatasetAvailable.png)
The experiment creates a classification model. The completed experiment can be seen below.
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/ExperimentCompleted.png)
We will be using the best model for deployment.The best model in this case was a voting ensemble.
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/AutoMLBestModel.png)

### Step 3: Deploying the model
We deploy the best model to an endpoint. We enable logging by enabling Application Insights.
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/ApplicationInsightsEnabled.png)
The logs produced from logs.py can be seen below:
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/logs.pyOutput.png)

We generate documentation using the Swagger tool.
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/SwaggerRunning.png)

### Step 6: Consume the model
By modifying the scoring_uri and key in the endpoint.py script to match the model enpoint we can interact with the trained model. The output of endpoint.py is shown below.
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/EndpointRuns.png)

### Step 7: Create, publish and consume a pipeline
In this step we use a Jupyter Notebook to create, publish and consume a pipeline. 

You can see that the pipeline has been created in the following screenshot:
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/PipelinesCreated.png)

In the pipelines section we also see the Pipeline Endpoint.
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/PublishedPipelineEndpoint.png)

Clicking on the pipeline we see the bank market dataset with the AutoML model as was created in the notebook.
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/BankmarketingWithAutoML.png)

The published pipeline overview shows the REST endpoint and that the status of the endpoint is ACTIVE
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/PublishedPipelineOverview.png)

In the Jupyter notebook we see that the "Use RunDetails Widget" shows the step runs"
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/ShowsStepRuns.png)

We can also see the run in ML Studio
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/ScheduledJob.png)


## Screen Recording
The screencast for the project can be found at the following link:
https://youtu.be/pOrwqQ4LhOI


