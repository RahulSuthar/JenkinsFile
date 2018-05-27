pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo "Running Checkout Stage......"
            }
        }
        stage('Compile') {
            steps {
                echo "Compiling Project Source code....."
            }
        }
        stage('Build') {
            steps {
                echo "Building Project....."
            }
        }
        stage('Unit Test') {
            steps {
                echo "Running Unit Test....."
            }
        }
        stage('Regression Test') {
            steps {
                echo "Running Regression Test....."
            }
        }
        stage('Report Generation') {
            steps {
                echo "Generating Report....."
            }
        }
        stage('Sanity check') {
            steps {
                input "Does the staging environment look ok?"
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
