<p align="center">
<img src="jenkins_docker.png" alt="Description of the image" width="300" height="200" align:"center">
<p>

## Devops with docker and github

### Configuration of resources and containers

#### Before initiating, clone the repository: 

<code> git clone https://github.com/leonardogonzalolaura/devops_docker_github.git
</code>


#### Step 1: Configure jenkins in a container to perform the following tasks:

- To navigate to the directory **devosp** where project was downloaded and execute the following commands:
  <code> docker build -t jenkins_devops --no-cache .</code>

  then execute:

  <code> docker run -d -p 8080:8080 -p 50000:50000 --name jenkins_container jenkins_devops </code> (review the documentation of the image at https://hub.docker.com/r/jenkins/jenkins/)

#### Step 2: Configure services jenkins 
- To access it in the browser, enter the url **http://localhost:8080/**

<p align="center">
<img src="getting_started_001.png" alt="Description of the image" width="300" height="200" align:"center">
<p>

- Run <code>docker logs jenkins_container</code> to obtain the password, copy the password and proceed with the configuration of jenkins
<p align="center">
<img src="getting_started_002.png" alt="Description of the image" width="500" height="150" align:"center">
<p>

- Select the option **Install suggested plugins** 
<p align="center">
<img src="getting_started_003.png" alt="Description of the image" width="500" height="300" align:"center">
<p>

- Wait while the installation completes
<p align="center">
<img src="getting_started_004.png" alt="Description of the image" width="500" height="300" align:"center">
<p>

- After completing the installation, create an admin user and provide the required information
  
<p align="center">
<img src="getting_started_005.png" alt="Description of the image" width="500" height="400" align:"center">
<p>

- In our case,we will use  **http://localhost:8080/** 
<p align="center">
<img src="getting_started_006.png" alt="Description of the image" width="500" height="400" align:"center">
<p>

- To access jenkins, click on the button **Start using Jenkins**
<p align="center">
<img src="getting_started_007.png" alt="Description of the image" width="500" height="200" align:"center">
<p>

- The Jenkins dashboard will be shown 
<p align="center">
<img src="getting_started_008.png" alt="Description of the image" width="500" height="200" align:"center">
<p>

#### Step 3: Create an automated pipeline with jenkins
- Select **New Intem** or **Create a job**
<p align="center">
<img src="create_pipeline_jenkins_001.png" alt="Description of the image" width="500" height="100" align:"center">
<p>

- Enter the name of the pipeline for example **webhook_pipeline_java** and select **Freestyle project** then click **OK**
<p align="center">
<img src="create_pipeline_jenkins_002.png" alt="Description of the image" width="500" height="350" align:"center">
<p>

- Configure the pipeline in the following ways:

- Use *nrg* **https://ngrok.com/** to router the Jenkins url**http://localhost:8080/**, create an account and in the select the options **Setup & Installation**, then choose the operating system
  
<p align="center">
<img src="create_pipeline_jenkins_003.png" alt="Description of the image" width="500" height="350" align:"center">
<p>
  