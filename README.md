<p align="center">
<img src="jenkins_docker.png" alt="Description of the image" width="300" height="200" align:"center">
<p>

## Devops with docker

### Configuration of resources and containers

#### Before initiating, clone the repository: 

<code> git clone https://github.com/leonardogonzalolaura/devopscourse.git
</code>


#### step 1: configure jenkins in a container to perform the following tasks:

- To go to the directory **devosp** and execute the following commands:
  <code> docker build -t jenkins_devops --no-cache </code>

  then execute:

  <code> docker run -p 8080:8080 -p 50000:50000 </code> (review the documentation of the image at https://hub.docker.com/r/jenkins/jenkins/)


