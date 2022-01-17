*NOTE:* This file is a template that you can use to create the README for your project. The *TODO* comments below will highlight the information you should be sure to include.


# Your Project Title Here

*TODO:* Write an overview to your project.

The goal of this project is to train a ML model using autoML, deploy it and consume it by using REST endpoints. 

## Architectural Diagram
*TODO*: Provide an architectual diagram of the project and give an introduction of each step. An architectural diagram is an image that helps visualize the flow of operations from start to finish. In this case, it has to be related to the completed project, with its various stages that are critical to the overall flow. For example, one stage for managing models could be "using Automated ML to determine the best model". 

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/tree/main/images/forreadme.png)

After having imported and registered the dataset, the first step is authentication in which we install az, enable it and login. We then create a service principal and allow it to access our workspace. The second step is to perform autoML in which we get many different models all of which perform the same classification task (try to find column ‘y’ in our data). We specify the ‘STANDARD_DS12_v2’ as our compute instance and set exit criterion to 1 hour and concurrency to 5. The next step is to deploy the best of these models. We then enable logging and application insight to keep track of the number of requests that succeded/failed and to check the performance of the model. Then, we consume the specific model’s REST endpoint and interact with it. We then create and publish a pipeline and check the documentation of it. 

## Key Steps
*TODO*: Write a short discription of the key steps. Remeber to include all the screenshots required to demonstrate key steps. 

Described above. To further improve the project the same things as in project 1 could be tested (https://github.com/nsourlos/optimizing_a_ML_pipeline_Project1#future-work).

## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:

lllll

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.

## Screenshots
![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/tree/main/images/1.1registered_dataset.png)

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/tree/main/images/1.2exp_complete.png)

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/tree/main/images/1.3best_model.png)

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/tree/main/images/4.1app_insights_enabled.png)

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/tree/main/images/4.2logs.png)

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/tree/main/images/5.1model_API_swagger.png)

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/tree/main/images/5.2data_json.png)

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/tree/main/images/5.3pipeline.png)

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/tree/main/images/6.1endpoint_1.png)

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/tree/main/images/6.2endpoint_2.png)

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/tree/main/images/7.1dataset_2.png)

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/tree/main/images/7.2pipeline_rest1.png)

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/tree/main/images/7.3jupyter.png)

![alt text](https://github.com/nsourlos/operationalizing_ML_Project2/tree/main/images/7.4experiments.png)



