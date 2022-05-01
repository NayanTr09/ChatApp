pipeline {
  agent any
  stages {
    stage('Deploy to AWS') {
      steps {
        sshagent(['ssh']) {
          sh '''
              ssh -o StrictHostKeyChecking=no ubuntu@ec2-54-237-146-61.compute-1.amazonaws.com
          '''
          sh '''
             git clone https://github.com/NayanTr09/ChatApp.git
          '''    
         }
      }
    }
  }
}
