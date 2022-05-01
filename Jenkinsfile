pipeline {
  agent any
  stages {
    stage('SSH to Backend and Install dependecies') {
      steps {
        sshagent(['ssh']) {
          sh '''
              ssh -o StrictHostKeyChecking=no ubuntu@10.0.3.58 sudo apt-get -y install python-pip python3-pip
          '''  
         }
        steps {
          sshagent(['ssh']) {
            sh '''
               ssh -o StrictHostKeyChecking=no ubuntu@10.0.3.58 cd /home/ubuntu/ChatApp/new_chatapp/
          '''
          }
        }
      }
    }
  }
}
