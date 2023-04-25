pipeline {
  agent any

  environment {
    DIRECTORY_PATH = "path/to/code/directory"
    TESTING_ENVIRONMENT = "test-environment"
    PRODUCTION_ENVIRONMENT = "your-name-production"
  }

  stages {
    stage('Build') {
      steps {
        echo "Fetching the source code from the directory path ${DIRECTORY_PATH}"
        echo "Compiling the code and generating any necessary artifacts"
      }
    }

    stage('Test') {
      steps {
        echo "Running unit tests"
        echo "Running integration tests"
      }
    }

    stage('Code Quality Check') {
      steps {
        echo "Checking the quality of the code"
      }
    }

    stage('Deploy') {
      steps {
        echo "Deploying the application to a testing environment specified by the environment variable ${TESTING_ENVIRONMENT}"
      }
    }

    stage('Approval') {
      steps {
        sleep time: 10, unit: 'SECONDS'
      }
    }

    stage('Deploy to Production') {
      steps {
        echo "Deploying the code to the production environment ${PRODUCTION_ENVIRONMENT}"
      }
    }
  }
}
