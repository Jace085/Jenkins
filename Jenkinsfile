pipeline {
    agent any 

    environment {
        DIRECTORY_PATH = '/path/to/your/code' 
        TESTING_ENVIRONMENT = 'jason_test_env'
        PRODUCTION_ENVIRONMENT = 'jason_armitage_prod_env'
    }

    stages {
        stage('Build') {
            steps {
                echo "fetch the source code from the directory path specified by the environment variable"
                echo "compile the code and generate any necessary artifacts"
            }
        }

        stage('Test') {
            steps {
                echo "unit tests"
                echo "integration tests"
            }
        }

        stage('Code Quality Check') {
            steps {
                echo "check the quality of the code"
            }
        }

        stage('Deploy') {
            steps {
                echo "deploy the application to a testing environment specified by the environment variable"
            }
        }

        stage('Approval') {
            steps {
                echo 'Simulating manual approval - pausing for 10 seconds'
                sleep(10) // Pause execution for 10 seconds
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "deploy the code to the ${PRODUCTION_ENVIRONMENT} environment"
            }
        }
    }
}
