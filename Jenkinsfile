#!groovy

 node {
   def mvnHome = tool 'M3'
  //def antHome = tool 'ant installation'
   env.PATH = "${mvnHome}/bin:${env.PATH}"
   echo "var mvnHome='${mvnHome}'"
  echo 'ANT'
  //echo "var antHome='${antHome}'"
  //echo antHome
   echo "var env.PATH='${env.PATH}'"
  
   //echo 'Eliminar el contenido'
   //bat 'rmdir /s /q *.*'
   //echo 'Descargando código de SCM' 
  
  checkout scm
   echo 'Compilando aplicación'
   bat 'mvn clean compile'
  
   //echo 'Ejecutando '
   //bat 'java -version'
   //bat 'mvn -version'
   //bat 'ant -version'
   bat call "C:/Users/msanchez/.jenkins/workspace/prueba-jenkins_master-QU64GEUOZOHAQ4374Y3LSIGRF3RR5DGJ7HNK3TGTHYX6PQQOYOPQ/prueba.bat %java% %ant%"
 
 }
