# Amazon Managed Workflows for Apache Airflow

### Some high-level features
1. Deploy at scale.
2. no operational burden.
3. no need to manage underlying architecture.
4. Run in own isloated cloud environment.
5. Secure cloud environment.
6. Environments monitoring through cloudwatch integration.
7. Connct to AWS, cloud & on-prem resources.
8. vast number of plugins available.


### How it works?
1. Orchestrate your workflows using Directed Acyclic Graphs (DAGs) written in Python. 
2. Create an environment with your Airflow cluster, including your scheduler, workers, and web server.
3. Upload DAGs, Plugins & requirements file to s3.</br>
![Screenshot from 2022-10-31 10-47-11](https://user-images.githubusercontent.com/19406666/198936491-0b23124d-0876-4863-bb64-4327be826a28.png)
4. Run your DAGs from AWS Management Console, CLI, SDK, or the Apache Airflow UI.
5. Monitor your environment with Amazon CloudWatch.

**Here are the steps to be taken**:
![Screenshot from 2022-10-31 10-55-55](https://user-images.githubusercontent.com/19406666/198937569-b434a888-cf2b-4547-a4fd-57a6e2e4637b.png)

**Here is the flow**:
![Screenshot from 2022-10-31 10-51-18](https://user-images.githubusercontent.com/19406666/198937001-936292e4-b69a-445a-a5fd-67b7fa2144c4.png)

### Use Cases
1. Support complex workflows.
2. Create scheduled or on-demand workflows that prepare and process complicated data from big data providers.
3. Coordinate extract, transform, and load (ETL) jobs.
4. Orchestrate multiple ETL processes that use diverse technologies within a complex ETL workflow.
5. Automate your pipeline to help machine learning (ML) modeling systems ingest and then train on data.

### Features
1. _Easy deployment_: Deploy Managed Workflows from AWS Management Console, CLI, AWS CloudFormation, or AWS SDK.
2. _Automatic scaling_: Worker monitoring is built in - when workers are over-burdened, additional workers are auto-provisioned, and auto-decommissioned.
3. _Built-in security_: </br>
    a. Your data secure using Amazon’s Virtual Private Cloud (VPC). </br>
    b. Data is automatically encrypted using AWS Key Management Service (KMS).</br>
    c. So your workflow environment is secure by default.</br>
4. Workflow monitoring in AWS or on-premises through Amazon Cloudwatch.
5. Low operational costs due to managed workflows at scale.
6. Different Plug-in integration including AWS, Apache airflow provided and custom built.
