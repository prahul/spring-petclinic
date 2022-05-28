# Getting Started

### Spring Boot Pet Clinic app
### Prerequisites
* Install Docker: https://docs.docker.com/desktop/mac/install/
* Install Jenkins: https://www.jenkins.io/download/
* Install Intellij community: https://www.jetbrains.com/idea/download/#section=mac
### Create a docker image for the app
* Clone the app from the GitHub
  * $ git clone https://github.com/prahul/spring-petclinic.git
* Clean a build your project
  * cd <project toot directory>
  * ./gradlew clean build
* Create the docker image
  * $ docker build -t spring-petclinic .
  * $ docker images
* Run the app
  * $ docker run -p 8080:8080 spring-petclinic
  * Open a browser: http://localhost:8080
