pipeline {
  agent any
    stages {
        stage('SCM') {
            steps { 
                git url: 'https://github.com/NayanTr09/ChatApp.git'
            }
        }
        stage('Code Analysis') {
     }
          steps {
           withSonarQubeEnv('SonarQube Server') {
           sh '''$SCANNER_HOME/bin/sonar-scanner
              '''
    }
  }
    
        stage("Quality Gate") {
            steps {
                timeout(time: 1, unit: 'HOURS') {
                  
                  waitForQualityGate abortPipeline: true
                }
            }
        }

    stage('SSH to Backend, Install dependencies and Run Application') { 
      steps {
        sshagent(['ssh']) {
          sh '''
              ssh -o StrictHostKeyChecking=no ubuntu@10.0.3.58 "sudo systemctl stop chatapp && sudo apt-get -y install python-pip python3-pip && cd /home/ubuntu/ChatApp/new_chatapp/ && git pull && sudo pip3 install -r requirements.txt && sudo systemctl start chatapp"
          
              '''  
         }
      }
    }
  }
}
