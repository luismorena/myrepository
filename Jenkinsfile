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
 //   withMaven(
   //     maven: 'Maven por defecto'
    //){
        sh 'mvn compile'
   // }
 //   mvn compile
  }
  
  stage ('Test') {
    echo "Comienzan las pruebas ... "
  }
  stage ('Empaquetar') {
    echo "Comienza la empaquetación ... "
  }
}

