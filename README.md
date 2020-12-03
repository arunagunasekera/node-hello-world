==Hello World==

Install

Use the Dockerfile to build the Jenkins container

To run the jenkins 

docker run --name jenkins --rm --detach --publish 8080:8080 --publish 50000:50000 --volume jenkins-data:/var/jenkins_home jenkins:1.0


Create a jenkins job 

Create a new pipeline job and associate to the Jenkinsfile
