pipeline {
    agent any
    stages {
        stage ('git checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/umasai91/umasai-demo-app.git'
            }
        }
        stage ('test') {
            steps {
                echo "Testing"
            }
        }
        stage ('build') {
            steps {
                script {
                    sh "docker build -t umasai-demo-app ."
                }
            }
        }
        stage ('runn') {
            steps {
                script {
                    sh "docker run -p 8001:8001 -d umasai-demo-app"
                }
            }
        }
    } 
}
