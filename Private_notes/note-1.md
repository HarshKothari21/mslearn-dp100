# Notebooks
- A notebook can only be run after creating a compute Instance.
- You can also run terminals through your compute instance.

- It provides 3 environments - python, R and azureml-python(here azureml-python package is already installed in the environment).
  - Through AzureMl-python you can create an experiment, run a experiment and all other features included in Azureml-python.
  
 # Experiments
 - It contains all the records of experiments that you have performed.
 - Within an experiment, how many runs have you performed and all log details of experiment.
    - Logs are stored under metrics section which can store varibles,list,image,table,etc...
 
 # Relation between Script, Experiment and Environment
 (Script based Experiment)
 - Scirpts contins the code to perform specific stasks for eg : train a model
 - You need an environment to run the script with all necessary libraries installed
 - Experiment will store all the information related to input and output and all log files. Thus running a script as an experiment.
 - Use a ScriptRunConfig to run a model training script as an Azure Machine Learning experiment.
 
# Register a model
- Note that the outputs of the experiment include the trained model file (diabetes_model.pkl). You can register this model in your Azure Machine Learning workspace, making it possible to track model versions and retrieve them later.
- You can also view registered models in your workspace on the Models page
