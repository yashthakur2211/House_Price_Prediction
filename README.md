# House_Price_Prediction

The Goal of this Project is to Predict the House prices based on variuos factors. 

# Steps to Run this Project

Step 1 - Install ZenML - https://docs.zenml.io/getting-started/installation\n
Step 2 - Create Virtual Enviroment in VS code for this project\n
Step 3 - pip install -r requirements.txt

# Run Pipeline 

Install this - /n

zenml integration install mlflow -y/n
zenml experiment-tracker register mlflow_tracker --flavor=mlflow\n
zenml model-deployer register mlflow --flavor=mlflow\n
zenml stack register local-mlflow-stack -a default -o default -d mlflow -e mlflow_tracker --set\n

Run - python run_pipeline.py\n

# Register the model on MLFlow

After running pipeline paste the cmd in terminal (mlflow ui --backend-store-uri 'file:C:\Users\Yash\AppData\Roaming\zenml\local_stores\87795587-1764-4e97-8db4-de078d3e8d20\mlruns') and open localhost http://127.0.0.1:5000

# Deploy the Model 

Run - python run_deployment.py

# Predict the Prices using Model

Run - python sample_predict.py
