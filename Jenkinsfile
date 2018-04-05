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
   echo 'Ejecutando '
   bat 'java -version'
   bat 'mvn -version'
   bat 'ant -version'
 }
