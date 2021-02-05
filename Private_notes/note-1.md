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
 - You need an environment to run the script with all necessary libraries instaled
 - Experiment will store all the information related to input and output and all log files. Thus running a script as an experiment.
 
