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
                    try {
                        bat 'minikube image rm market-back:v2'
                    } catch (Exception e) {
                        echo 'minikube无market-back:v2'
                    }
                    try {
                        bat 'docker image rm market-back:v2'
                    } catch (Exception e) {
                        echo 'docker无market-back:v2'
                    }
                }
            }
        }
        
    }
    post {
        always {
            echo "Kubernetes自动部署完成"
        }
    }
}
