#!groovy

node {
  
    def mvnHome = tool 'M3'
    env.PATH = "${mvnHome}/bin:${env.PATH}"
   
    stage 'mvn clean'
    bat 'mvn clean'
  
      stage 'Test'
   echo 'Ejecutando tests'
   try{
      sh 'mvn verify'
      step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])
   }catch(err) {
      step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])
      if (currentBuild.result == 'UNSTABLE')
         currentBuild.result = 'FAILURE'
      throw err
   }
  
     stage 'Instalar'
     echo 'Instala el paquete generado en el repositorio maven'
     bat 'mvn install -Dmaven.test.skip=true'
}
