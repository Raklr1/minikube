pipeline {
    agent any
    tools{
        jdk 'JDK-21'
        maven 'Maven'
        nodejs 'nodejs'
    }

    stages {
        stage('1') {
            steps {
                    withKubeConfig([credentialsId: 'k8s1']) {
                    
                    //bat 'echo PATH=%PATH%'
                    //bat 'minikube start'
                    bat 'minikube version'
                    //bat 'minikube update-context'
                    //bat 'echo %KUBECONFIG%'
                    bat 'minikube status'
                    bat 'docker image ls'
                    //bat 'minikube image ls'
                    //bat 'kubectl get pods'
                    //bat 'minikube stop'
                    //bat 'minikube image load mysql:8.0.43'
                    //bat 'minikube service mysql'
                    //bat 'minikube delete'
                    bat 'minikube image ls'
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

