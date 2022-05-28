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
//         stage('Build Docker Image') {
//             steps {
//                 sh './gradlew docker'
//             }
//         }
//         stage('Push image to artifactory') {
//             steps {
//                 sh './gradle artifactory'
//             }
//         }
    }
}
