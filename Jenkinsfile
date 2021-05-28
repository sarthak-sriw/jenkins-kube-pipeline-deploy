pipeline {
  agent any
  
  parameters{
    booleanParam(name: 'DeployPod', defaultValue: true)
  }
  
  stages {
    
    stage("Test") {
      when{
        expression{
          params.DeployPod
        }
      
      }
      steps {
        sh "kubectl apply -f deploy.yml --kubeconfig /admin.conf"  // always work
        // kubernetesDeploy(configs: 'deploy.yml' , kubeconfigId: 'mykubeconfigfile')  ---->> might face version issue 
      } 
    }
  }
  
  post{
    success{
      echo "task executed successfully"
    }
    
    failure{
      echo "task execution unsuccessfully"
    } 
    
    always{
      echo "task execution in progress"
    }
  }
}
