# Project 2: Tracking User Activity

In this project, you work at an ed tech firm. You've created a service that
delivers assessments, and now lots of different customers (e.g., Pearson) want
to publish their assessments on it. You need to get ready for data scientists
who work for these customers to run queries on the data. 

# Tasks

Prepare the infrastructure to land the data in the form and structure it needs
to be to be queried.  You will need to:

- Publish and consume messages with Kafka
- Use Spark to transform the messages. 
- Use Spark to transform the messages so that you can land them in HDFS

# Contents

- <b>docker-compose.yml</b> file ([here](docker-compose.yml)): This has all the containers required to run the data pipeline including Kafka, zookeeper,Spark, and HDFS.  You may need to update these ports if they are already being utilized.
- <b> Console history (elizkhan-history.txt)</b> file ([here](elizkhan-history.txt)): This is the history file of the command line prompts that were used to spin up the cluster (Zookeeper, Kafka, Spark, HDFS), publish and consume Kafka messages, create a Kafka topic, and start the Spark session. More details are in the Jupyter Notebook file.
- <b> Project_2_Tracking_User_Activity_Elizabeth_Khan_07_10_2021_final.ipynb </b> ([here](Project_2_Tracking_User_Activity_Elizabeth_Khan_07_10_2021_final.ipynb)): This is a Jupyter Notebook file that contains a comprehensive explanation of the project, command line code annotations, and Python Spark code. This includes everything from spinning up docker containers to Spark transformations, and loading into tables in HDFS.
- <b>Data Flow Conceptual Architecture Images</b> folder ([here](Data%20Flow%20Conceptual%20Architecture%20Images)): This contains the conceptual data flow diagram and a diagram of the table joins for the assessment_master table.


# Setup

This setup is using the latest docker image provided from the <b>midsw205</b> docker repository which was provided to our class. A w205 directory was created within the virtual machine environment in the GCP instance. To connect Jupyter Notebook to the Spark container, Spark has an expose section in the docker-compose.yml file. Moreover, this Jupyter Notebook kernel was started from the command line in the virtual machine and was the ip address was updated to match the virtual machine.

Below is an outline of how my w205 directory is setup for this project.

```
w205/
├── _project-2-elizkhan/
│   ├── docker-compose.yml
│   └── assessment-attempts-20180128-121051-nested.json

```




_Note: the original JSON file can be retreived by running this in the command line in the above directory:_

```bash
curl -L -o assessment-attempts-20180128-121051-nested.json https://goo.gl/ME6hjp
```
