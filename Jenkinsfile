pipeline {

  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/Nurmukhamed02/jenkins-kubernetes.git', branch:'main'
      }
    }

    stage('Apply Kubernetes files') {
      steps {
        withKubeConfig([credentialsId: 'mykubeconfig', ]) {
           sh 'kubectl get nodes'
               
            }
        }
    }
  }
}
