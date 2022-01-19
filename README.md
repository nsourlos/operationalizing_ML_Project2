# Operationalizing ML

The goal of this project is to train a ML model using autoML, deploy it and consume it by using REST endpoints. 

## Architectural Diagram

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/forreadme.png)

After having imported and registered the dataset, the first step is authentication in which we install az, enable it and login. We then create a service principal and allow it to access our workspace. The second step is to perform autoML in which we get many different models all of which perform the same classification task (try to find column ‘y’ in our data). We specify the ‘STANDARD_DS12_v2’ as our compute instance and set exit criterion to 1 hour and concurrency to 5. The next step is to deploy the best of these models. We then enable logging and application insight to keep track of the number of requests that succeeded/failed and to check the performance of the model. Then, we consume the specific model’s REST endpoint and interact with it. We then create and publish a pipeline and check the documentation of it. 

To further improve the project the same things as in project 1 could be tested (https://github.com/nsourlos/optimizing_a_ML_pipeline_Project1#future-work). That means that we can try different combinations/values for the parameters in random sampling (or even try other sampling methods like Bayesian Sampling), add more total runs, use ‘AUC_weighted’ and other metrics instead of accuracy, apply methods to combat class imbalance issues (alert generated in AutoML runs), increase experiment timeout in AutoML to perform more runs/experiments.

## Screen Recording

https://drive.google.com/file/d/1RFojPLQj9dys4MvSavrEqNLKEMcYsa2I/view?usp=sharing

## Screenshots

Preparation - Initialize compute instance with ‘STANDARD_DS12_v2’ 
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/1.0compute_instance.png)


Step 2 - ‘Registered Datasets’: Dataset uploaded and used in this project
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/1.1registered_dataset.png)

Step 2 - AutoML Experiment Completed, along with the best model. We can see that the run stopped since there was no improvement of score in the last 20 epochs. The best model is a VotingEnsemble with an AUC_weighted of 0.9478.
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/1.2exp_complete.png)

Step 2 - Metrics for the VotingEnsemble (Best model). Along with AUC-weighted other metrics like accuracy, average precision etc. are provided
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/1.3best_model.png)

Step 4 - We choose the best model for deployment and enable "Authentication" while deploying the model using Azure Container Instance (ACI). The executed code in logs.py enables Application Insights. "Application Insights enabled" is disabled before executing logs.py.
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/4.1app_insights_enabled.png)

Step 4 - Two pictures of logs created when run the logs.py script. The first one is produced when this script is run locally and the second one is the same output as this is saved on Azure endpoints section, in the deployment logs tab.
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/4.2logs.png)

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/4.3logs2.png)


Step 5 - Swagger Running on localhost port 9000 (changed by me) with HTTP API methods and responses
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/5.1model_API_swagger.png)

Step 5 - Pipeline runs, one created without (first) and one with (second) Python SDK
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/5.3pipeline.png)

Step 5 - Pipeline run overview, with an active status
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/5.4pipeline_run_overview.png)


Step 6 - Published pipeline overview - The REST url/endpoint.
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/6.1endpoint_1.png)

Step 6 - Pipeline endpoints created without and with Python SDK
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/6.2endpoint_2.png)

Step 6 - Output of the model after data from 2 individuals are given to it.
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/6.3endpoint_out.png)


Step 7 - Registered Bankmarketing dataset for AutoML experiments
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/7.1dataset_2.png)

Step 7 - Run Widgets Jupyter output of the pipeline run
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/7.3jupyter.png)




