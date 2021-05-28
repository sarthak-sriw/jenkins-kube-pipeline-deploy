pipeline {
  agent any
  
  stages {
    
    stage("Test") {
      
      steps {
        sh "kubectl apply -f deploy.yml --kubeconfig /admin.conf"
      }
      
      
    }
  
  }
  

}
