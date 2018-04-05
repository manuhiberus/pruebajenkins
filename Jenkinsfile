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
  
    bat """
        call prueba.bat x86
        echo "Made it!"
        %antt%
        %javaa%
    """
 }
