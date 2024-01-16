pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                checkout scm
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