pipeline {
    agent any
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                sh './gradlew assemble'
            }
        }
         stage('Test') {
            steps {
                sh './gradlew test'
            }
        }
        stage('Build Docker Image') {
            agent docker
            steps {
                sh 'docker build -t spring-petclinic .'
            }
        }
//         stage('Run Docker Image') {
//             steps {
//                 sh 'gradle dockerRun'
//             }
//         }
    }
}
