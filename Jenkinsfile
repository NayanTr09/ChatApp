pipeline {
  agent any
  stages {
    stage('Deploy to AWS') {
      steps {
        sshagent(['ssh']) {
          sh '''
              ssh -o StrictHostKeyChecking=no ubuntu@10.0.3.58
          '''  
          sh '''
             git clone https://github.com/NayanTr09/ChatApp.git
          '''
          sh '''
             cd /home/ubuntu/ChatApp/new_chatapp/ ls
          '''   
         }
      }
    }
  }
}
