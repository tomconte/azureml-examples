This is a 3 step dummy pipeline job. It uploads a local sample csv file for input data. It uses locally defined components - train, score and eval. You need to edit the compute cluster in the defaults section and run the `az ml job create --file pipeline.yml` to submit the pipeline job. Alternatively, you can override the compute from the command line with `az ml job create --file pipeline.yml --set defaults.component_job.compute.target=<your_compute>`. Once you submit the job, you will find the URL to view the job graph and logs in AzureML Studio UI under the `interaction_endpoints` -> `Studio` section of the output. 