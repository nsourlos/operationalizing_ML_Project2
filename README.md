# Operationalizing ML

The goal of this project is to train a ML model using autoML, deploy it and consume it by using REST endpoints. 

## Architectural Diagram

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/forreadme.png)

After having imported and registered the dataset, the first step is authentication in which we install az, enable it and login. We then create a service principal and allow it to access our workspace. The second step is to perform autoML in which we get many different models all of which perform the same classification task (try to find column ‘y’ in our data). We specify the ‘STANDARD_DS12_v2’ as our compute instance and set exit criterion to 1 hour and concurrency to 5. The next step is to deploy the best of these models. We then enable logging and application insight to keep track of the number of requests that succeded/failed and to check the performance of the model. Then, we consume the specific model’s REST endpoint and interact with it. We then create and publish a pipeline and check the documentation of it. 

To further improve the project the same things as in project 1 could be tested (https://github.com/nsourlos/optimizing_a_ML_pipeline_Project1#future-work).

## Screen Recording

https://drive.google.com/file/d/1AicHRHQgjVnaPl3gMbITLQhu9WnuZFlu/view?usp=sharing

## Screenshots

Step 2 - ‘Registered Datasets’: Dataset uploaded and used in this project
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/1.1registered_dataset.png)

Step 2 - AutoML Experiment Completed, along with the best model
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/1.2exp_complete.png)

Step 2 - Best model metrics
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/1.3best_model.png)

Step 4 - Application Insights Enabled and URL to it
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/4.1app_insights_enabled.png)

Step 4 - Logs created when run the logs.py script
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/4.2logs.png)

Step 5 - Swagger Running on localhost port 9000 (changed by me) with HTTP API methods and responses
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/5.1model_API_swagger.png)

Step 5 - File data.json output from Swagger
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/5.2data_json.png)

Step 5 - Pipeline created from Swagger
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/5.3pipeline.png)

Step 6 - Endpoint 1 - The REST url
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/6.1endpoint_1.png)

Step 6 - Endpoint 2 - Created when pipeline run
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/6.2endpoint_2.png)

Step 7 - Bankmarketing dataset
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/7.1dataset_2.png)

Step 7 - Pipelines produced
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/7.2pipeline_rest1.png)

Step 7 - Run Widgets Jupyter output
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/7.3jupyter.png)

Step 7 - Experiments run 
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/blob/main/images/7.4experiments.png)



