pipeline {
    agent { dockerfile true }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
                sh 'svn --version'
            }
        }
    }
    post {
        always {
            mail to: 'dhrubt@hexaware.com', subject: 'Testing Jenkins EMail',
                body: "Run display URL ${env.RUN_DISPLAY_URL}"
        }
    }
}
