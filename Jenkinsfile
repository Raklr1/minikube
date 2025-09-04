pipeline {
  agent any

  tools {nodejs "nodejs23"}

  stages {
    stage('Install Apifox CLI') {
      steps {
       bat 'start /B kubectl port-forward svc/frontend 59990:8080 > portforward.log 2>&1'
        bat 'kubectl get pods'
      }
    }
  }
}
