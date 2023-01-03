pipeline {


  agent any
  
  stages {
    
    stage ("Docker build") {
      steps {
        script {
          dockerImage = docker.build registry
        }
       }
    }
  }
  }
