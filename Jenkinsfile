pipeline {
    agent {
        label 'java-slave'
    }

    environment {
        // key = value
        course = "Kubernetes"
        name   = "Siva"
    }

    stages {
        stage ('Build') {
            steps {
                echo "**** Building the application ****"
                echo "**** Welcome ${name} ****"
                echo "**** You enrolled to ${course}, All the best ${name} ****"
            }
        }
    }
}
