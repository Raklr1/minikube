pipeline {
  agent any

  tools {nodejs "nodejs23"}

  stages {
    stage('Install Apifox CLI') {
      steps {
       powershell '''
                    $process = Start-Process -NoNewWindow -PassThru kubectl -ArgumentList "port-forward svc/backend 59999:80"
                   
      '''
        bat 'kubectl get pods'
      }
    }
  }
}
