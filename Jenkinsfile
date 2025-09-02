pipeline {
    agent any
    tools{
        jdk 'JDK-21'
        maven 'Maven'
        nodejs 'nodejs'
    }

    stages {
        stage('导入数据') {
            steps {
                withKubeConfig([credentialsId: 'k8s1']) {
                    bat 'minikube image rm market-back:v2 2>nul'
                    bat 'docker image rm market-back:v2 2>nul'
                }
            }
        }
        
    }
    post {
        always {
            echo "1"
        }
    }
}

