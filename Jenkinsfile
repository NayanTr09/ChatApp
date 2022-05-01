pipeline {
  agent any
  stages {
    stage('Deploy to AWS') {
      steps {
        sshagent(['ssh']) {
          sh '''
              ssh -o StrictHostKeyChecking=no ubuntu@ec2-3-218-152-19.compute-1.amazonaws.com
          '''
          sh '''
             cd /home/ubuntu/
          '''  
          sh '''
             git clone https://github.com/NayanTr09/ChatApp.git
          '''
         }
      }
    }
  }
}
