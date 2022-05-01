pipeline {
  agent any
  stages {
    stage('SSH to Backend and Clone Repository') {
      steps {
        sshagent(['ssh']) {
          sh '''
              ssh -o StrictHostKeyChecking=no ubuntu@10.0.3.58 git clone https://github.com/NayanTr09/ChatApp.git
          '''  
         }
      }
    }
  }
}
