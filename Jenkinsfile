
pipeline {
  agent any
  stages {
    stage ('Etapa 1:: Comienza la compilacion') {
      steps {
        echo "Comienza la compilación ... "
       withMaven(
         maven: 'Maven por defecto'
       ){
        sh 'mvn compile'
        }
      }
    }
     stage ('Etapa 2 :: Comienzan las pruebas ... " ') {
      steps {
        echo 'Comienzan las pruebas'
         withMaven(
           maven: 'Maven por defecto'
         ){
          sh 'mvn test'
        }
        
      }
    }
     stage ('Etapa 3 :: Comienza el empaquetado') {
      steps { 
        echo 'Comienza el empaquetado'
        withMaven(
           maven: 'Maven por defecto'
         ){
          sh 'mvn package'      
        }
      }
    }
  }
} 

/*

node {
  checkout scm
  stage ('Compilar') {
    echo "Comienza la compilación ... "
     withMaven(
       maven: 'Maven por defecto'
    ){
        sh 'mvn compile'
   }

  }
  
  stage ('Test') {
    echo "Comienzan las pruebas ... "
    withMaven(
        maven: 'Maven por defecto'
    ){
        sh 'mvn test'
  //      junit '**/*.xml'
//    }
  //}
//  stage ('Empaquetar') {
//    echo "Comienza la empaquetación ... "
    //try{
      
  //  }finally{
    //deleteDir()
 //  }
 //    withMaven( maven: 'Maven por defecto'
 //        sh 'mvn package'
 //   ){
        
   // }
//  }
//}

