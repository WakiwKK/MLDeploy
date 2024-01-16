pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/WakiwKK/MLDeploy.git']]])
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