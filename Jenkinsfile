pipeline {
    agent any
    stages {
        stage('Build') {
            
            steps {
                notifyStarted()
                echo 'Change from Machine Building'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
}

def notifyStarted() {
   emailext (
    subject: "Job '${env.JOB_NAME} ${env.BUILD_NUMBER}'",
    body: """<p>Check console output at <a href="${env.BUILD_URL}">${env.JOB_NAME}</a></p>""",
    to: "rahul16194@gmail.com",
    from: "no-reply-from@jenkins.com"
)
 }


