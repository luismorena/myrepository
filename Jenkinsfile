node ('master') { 
    checkout scm
    stage('Compilar') {
	echo "Comienza la compilacion..."
	withMaven(
           maven:'Maven Test'			
	){
         sh 'mvn compile'
	}
    }
    stage('Test') {
	echo "Comienzan las pruebas..."
	withMaven(
           maven:'Maven Test'			
	){
         sh 'mvn test'
	}
    }
    stage('Empaquetar') {
	echo "Comienza la empaquetacion..."
	withMaven(
           maven:'Maven Test'			
	){
         sh 'mvn package'
	}
    }
}


