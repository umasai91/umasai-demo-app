pipeline {
    agent any
    stages {
        stage {
            steps {
                git branch: 'main', url: 'https://github.com/umasai91/umasai-demo-app.git'
            }
        }
        stage {
            steps {
                echo "Testing"
            }
        }
        stage {
            steps {
                script {
                    sh "docker build --no-cache -t umasai-demo-app ."
                }
            }
        }
        stage {
            steps {
                script {
                    sh "docker run -p 8001:8001 -d umasai-demo-app"
                }
            }
        }
    } 
}
