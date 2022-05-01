pipeline {
  agent any
  stages {
    stage('Deploy to AWS') {
      steps {
        sshagent(['ssh']) {
          sh '''
              ssh -o StrictHostKeyChecking=no ubuntu@10.0.3.58 git clone https://github.com/NayanTr09/ChatApp.git sudo apt-get install pip
          '''  
         }
      }
    }
  }
}
