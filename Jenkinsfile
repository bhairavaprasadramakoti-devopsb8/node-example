pipeline {
    agent {
        label :'java-slave'
    }

    environment {
        COURSE       = "KUBERNETES"
        GITHUB_CREDS = credentials('bhairavaprasadramakoti-devopsb8_github_pat')
        SONAR_CREDS  = credentials('i27_sonar_token')
        SONAR_URL    = "http://136.116.60.14:9000"
    }

    stages {
        stage ('Build') {
            steps {
                echo "My Github Credentials are ${GITHUB_CREDS}"
                echo "My user name is: ${GITHUB_CREDS_USR}"
                echo "My password is: ${GITHUB_CREDS_PSW}"
            }
        }
        stage ('Sonar') {
            steps {
                sh """
                mvn sonar:sonar \
                    -Dsonar.host.url=${SONAR_URL} \
                    -Dsonar.login=${SONAR_CREDS}  
                """
            }

        }
    }
}
