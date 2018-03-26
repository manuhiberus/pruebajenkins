#!groovy

node {
  
    def mvnHome = tool 'M3'
    env.PATH = "${mvnHome}/bin:${env.PATH}"
   
    stage 'mvn clean'
    bat 'mvn clean'
  
   
  
     stage 'Instalar'
     echo 'Instala el paquete generado en el repositorio maven'
     bat 'mvn install -Dmaven.test.skip=true'
}
