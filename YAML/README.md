# Defining a pipeline using YAML

This project defines two pipelines: one using the Python SDK in the Jupyter notebook, the other can be created by running:

     az ml pipeline create -n multistep -y pipeline_multistep.yml -w pipelines -g laobri-rg

The YAML definition requires the Jupyter notebook to have been run, as the notebook writes the Python files and creates the Dataset for input. 

Note that YAML-defined Azure ML Pipelines must use FileDataset (not TabularDataset) for input, so that's why there are two datasets created in the Jupyter notebook. 