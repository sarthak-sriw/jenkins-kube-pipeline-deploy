pipeline {
  agent any
  
  stages {
    
    stage("Test") {
      when{
        expression{
          false
        }
      
      }
      steps {
        sh "kubectl apply -f deploy.yml --kubeconfig /admin.conf"  // always work
        // kubernetesDeploy(configs: 'deploy.yml' , kubeconfigId: 'mykubeconfigfile')  ---->> might face version issue 
      }
      
      
    }
  
  }
  

}
