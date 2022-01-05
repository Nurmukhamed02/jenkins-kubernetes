pipeline {

  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/Nurmukhamed02/jenkins-kubernetes.git', branch:'main'
      }
    }

    stage ('K8S Deploy') {
      steps {
        script {
           kubernetesDeploy(
                    configs: 'nginx.yaml',
                    kubeconfigId: 'kube_config',
                    enableConfigSubstitution: true
                    )           
               
            }
        }
    }
  }

}
