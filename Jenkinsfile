pipeline {
    agent any
    tools{
        jdk 'JDK-21'
        maven 'Maven'
        nodejs 'nodejs'
    }

    stages {
        stage('后端构建') {
            steps {
                    withKubeConfig([credentialsId: 'k8s1']) {
                    
                    
                    //bat 'minikube start'
                    bat 'minikube version'
                    //bat 'minikube update-context'
                    //bat 'echo %KUBECONFIG%'
                    //bat 'minikube status'
                    //bat 'minikube image ls'
                    //bat 'kubectl get pods'
                    bat 'minikube stop'
                    }
                    
                
            }
        }
        
    }
    post {
        always {
            echo "后端构建完成"
        }
    }
}

