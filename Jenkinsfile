pipeline {
  agent any
  stages {
    stage('SSH to Backend, Install dependecies and Run Application') {
      steps {
        sshagent(['ssh']) {
          sh '''
              ssh -o StrictHostKeyChecking=no ubuntu@10.0.3.58 "sudo apt-get -y install python-pip python3-pip"; "cd /home/ubuntu/ChatApp/new_chatapp/"
          
              
          '''  
         }
      }
    }
  }
}
