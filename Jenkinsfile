pipeline {
  agent any
  
  stages {
    
    stage("Test") {
      
      steps {
        sh "kubectl apply -f deploy.yml --kubeconfig /admin.conf"  // always work
        // kubernetesDeploy(configs: 'deploy.yml' , kubeconfigId: 'mykubeconfigfile')  ---->> might face version issue 
      }
      
      
    }
  
  }
  

}
