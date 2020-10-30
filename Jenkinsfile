pipeline {
  agent { 
      docker { 
          image 'python:3.7.2' 
          } 
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
        sh 'sleep 10 && curl -s localhost:8000'
      }
    }
     
      }    
    }
 
