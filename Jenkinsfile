pipeline {


  agent any
  
  stages {

    stage ("checkout") {
      steps {
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/hardikpi/order-my-food.git']]])
       }
    }
   
    stage ("Docker build") {
      steps {
        script {
          dockerImage = docker.build registry
        }
       }
    }
  }
