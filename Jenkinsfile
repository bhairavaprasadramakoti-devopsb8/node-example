pipeline {
    agent {
        label 'java-slave'
    }
    parameters {
        string (
            name: 'PERSON',
            defaultValue: 'Siva',
            description: 'Whats your name???'
        )
    }
    stages {
        stage ('ParametersStage') {
            steps {
                echo "Hello, ${params.PERSON}"
            }
        }
    }
}
