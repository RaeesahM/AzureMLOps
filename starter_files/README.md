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
![alt text](http://url/to/img.png](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/ServicePrincipleCreateed.png)
![alt text](https://github.com/RaeesahM/AzureMLOps/blob/master/starter_files/AuthenticationProof.png)

## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.
