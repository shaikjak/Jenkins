pipeline {
    agent {
        label "AGENT-1"
    }

    environment {
        Greetings = "Hello World"
    }

    parameters {
        // no parameters defined
    }

    options {
        timeout(time: 30, unit: 'MINUTES')
    }

    stages {

        stage('git clone') {
            steps {
                sh 'echo clone the repo'
            }
        }

        stage('build') {
            steps {
                sh 'echo build the package'
            }
        }

        stage('artifact') {
            steps {
                sh 'echo generate the artifcat'
            }
        }

        stage('docker Image') {
            steps {
                sh 'echo build the image'
            }
        }

        stage('deploy') {
            steps {
                sh 'echo deply the image'
            }
        }
    }

    post {
        always {
            echo 'Pipeline compeleted'
        }
        success {
            echo 'Pipeline succeeded'
        }
        failure {
            echo 'Pipeline Failed'
        }
    }
}
