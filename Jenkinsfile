#!groovy

 node {
   def mvnHome = tool 'M3'
   env.PATH = "${mvnHome}/bin:${env.PATH}"
   echo "var mvnHome='${mvnHome}'"
   echo "var env.PATH='${env.PATH}'"
  
   //echo 'Eliminar el contenido'
   //bat 'rmdir /s /q *.*'
   echo 'Descargando código de SCM' 
  
  checkout scm
   echo 'Compilando aplicación'
   bat 'mvn clean compile'
  
   stage 'Test'
   echo 'Ejecutando tests'
   try{
      bat 'mvn verify'
      step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])
   }catch(err) {
      step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])
      if (currentBuild.result == 'UNSTABLE')
         currentBuild.result = 'FAILURE'
      throw err
   }
 }
