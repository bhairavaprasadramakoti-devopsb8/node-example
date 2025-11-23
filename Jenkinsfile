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
            /*when {
                expression {
                    BRANCH_NAME ==~ /(production|staging)/
                }
            }*/
            when {
                anyOf {
                    branch 'release-*'
                    tag pattern: "v\\d{1,2}.\\d{1,2}.\\d{1,2}", comparator: "REGEXP"
                }
            }
            steps {
                echo "**** Deploying to Stage Environment ****"
            }
        }
        stage ('DeplotoProd'){
            /*when {
                expression {
                    BRANCH_NAME ==~ /(production|staging)/
                }
            }*/
            when {
                tag pattern: "v\\d{1,2}.\\d{1,2}.\\d{1,2}", comparator: "REGEXP"
            }
            steps {
                echo "**** Deploying to Prod Environment ****"
            }
        }
    }
}
