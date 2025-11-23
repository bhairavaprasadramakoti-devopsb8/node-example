pipeline {
    agent {
        label 'java-slave'
    }
    stages {
        stage ('Build') {
            steps {
                echo "Building the application"
            }
        }
        stage ('ParallelStageScans') {
            parallel {
                stage ('Sonar') {
                    steps {
                        echo 'Sonar Stage is executing'
                        sleep 10
                    }
                }
                stage ('Fortify') {
                    steps {
                        echo 'Fortify Stage is executing'
                        sleep 10
                    }
                }
                stage ('Prisma') {
                    steps {
                        echo 'Prisma Stage is executing'
                        sleep 10
                    }
                }
            }
        }
    }
}
