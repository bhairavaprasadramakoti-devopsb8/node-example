pipeline {
    agent {
        label 'java-slave'
    }

    environment {
        // key = value
        course = "Kubernetes"
        name   = "Siva"
        cloud  = "AZURE"
    }

    stages {
        stage ('Build') {
            environment{
                cloud = "GCP"
            }
            steps {
                echo "**** Building the application in First Stage****"
                echo "**** Welcome ${name} ****"
                echo "**** You enrolled to ${course}, All the best ${name} ****"
                echo "**** You are certified in ${cloud} cloud"
            }
        }
        stage ('SecondStage') {
            steps {
                echo "**** Building the application in Second Stage****"
                echo "**** Welcome ${name} ****"
                echo "**** You are certified in ${course}"
            }
        }
    }
}
