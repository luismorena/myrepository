/*
pipeline {
  agent any
  stages {
    stage ('Etapa 1') {
      steps {
        echo 'Hola Mundo'
      }
    }
  }
} */

node {
  checkout scm
  stage ('Compilar') {
    echo "Comienza la compilación ... "
 //  withMaven(
   //     maven: 'Maven por defecto'
   // ){
        sh 'mvn compile'
   // }

  }
  
  stage ('Test') {
    echo "Comienzan las pruebas ... "
  //  withMaven(
//        maven: 'Maven por defecto'
  //  ){
        sh 'mvn test'
    //}
  }
  stage ('Empaquetar') {
    echo "Comienza la empaquetación ... "
    try{
      sh 'mvn package'
    }finally{
      deleteDir()
    }
  //  withMaven(
    //    maven: 'Maven por defecto'
   // ){
        
   // }
  }
}

