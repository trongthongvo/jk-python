pipeline {
  agent {
        label 'slave'
    }
  stages {
    stage('build') {
      steps {
        sh 'pip3 install -r requirements.txt'
      }
    }

    stage('run') {
      steps {
        sh 'python3 app.py &'
      }
    }

    stage('test') {
      steps {
        sh 'sleep 60 && curl -s localhost:8080'
      }
    }

    stage('clear up') {
      steps {
        sh 'fuser -k 8080/tcp'
      }
    }
     
      }    
    }
 
