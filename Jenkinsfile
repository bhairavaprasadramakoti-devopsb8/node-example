pipeline {
    agent {
        label 'java-slave'
    }
    stages {
        stage ('Build'){
            steps {
                echo "Building the application"
            }
        }
        stage ('Scans'){
            steps {
                echo "Performing the scans"
            }
        }
        stage ('DeplotoDev'){
            steps {
                echo "**** Deploying to Dev Environment ****"
            }
        }
        stage ('DeplotoTest'){
            steps {
                echo "**** Deploying to Test Environment ****"
            }
        }
        stage ('DeplotoStage'){
            steps {
                echo "**** Deploying to Stage Environment ****"
            }
        }
        stage ('DeplotoProd'){
            steps {
                echo "**** Deploying to Prod Environment ****"
            }
        }
    }
}
