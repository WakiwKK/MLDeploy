pipeline {
    agent any
    
    environment{
        BENTO_HOME = "${WORKSPACE}/bento_home"
        BENTO_NAME = "your_bento_service_name"
        BENTO_VERSION = "1.0.0"
        DOCKER_REGISTRY_URL = "your.docker.registry"
        DOCKER_IMAGE_NAME = "${DOCKER_REGISTRY_URL}/${BENTO_NAME}:${BENTO_VERSION}"
    }

    stages {
        stage('Hello') {
            steps {
                checkout scm
                echo "${sh(script: 'git rev-parse HEAD', returnStdout: true).trim()}"
            }
        }
        stage('Hello2') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[ url: 'https://github.com/WakiwKK/MLDeploy.git']]]) 
                sh "ls -lart ./*"
            }
        }
        stage('Hello3') {
            steps {
                echo "Hello World20 ${BUILD_ID}" 
            }
        }
        
    }
}