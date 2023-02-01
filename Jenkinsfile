pipeline {
    agent {
        node {
            label 'docker-agent-python'
            }
      }
    triggers {
        pollSCM '*/5 * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                python3 pythontests.py
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
            }
        }
    }
}
