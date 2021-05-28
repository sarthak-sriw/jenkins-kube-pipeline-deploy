pipeline {
  agent any
  
  parameters{
    booleanParam(name: 'DeployPod',defaultValue: true)
  }
  
  stages {
    
    stage("Test") {
      when{
        expression{
          param.DeployPod
        }
      
      }
      steps {
        sh "kubectl apply -f deploy.yml --kubeconfig /admin.conf"  // always work
        // kubernetesDeploy(configs: 'deploy.yml' , kubeconfigId: 'mykubeconfigfile')  ---->> might face version issue 
      }
      
      
    }
  
  }
  

}
