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
        withKubeConfig([credentialsId: 'mykubeconfig', serverUrl: 'https://0615CDB22445853E01165AD9C054A48F.gr7.us-east-1.eks.amazonaws.com']) {
           sh 'kubectl apply -f nginx.yaml'
               
            }
        }
    }
  }
}
