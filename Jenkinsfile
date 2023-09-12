pipeline {
  agent any
  stages {
    stage('git pull') {
      steps {
        // Git-URL will replace by sed command before RUN
        git url: 'https://github.com/byunghyuns/gitops.git', branch: 'main'
      }
    }
    stage('k8s deploy'){
      steps {
        sh '''
        kubectl apply -f deployment.yaml
        '''
      }
    }    
  }
}
