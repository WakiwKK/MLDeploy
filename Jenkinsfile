pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                checkout scm
                def branchRevision = sh(script: 'git rev-parse HEAD', returnStdout: true).trim()
                    echo "Branch Revision: ${branchRevision}"
            }
        }
        stage('Hello2') {
            steps {
                echo "${env}"
            }
        }
        stage('Hello3') {
            steps {
                echo "Hello World20 ${BUILD_ID}" 
            }
        }
        
    }
}