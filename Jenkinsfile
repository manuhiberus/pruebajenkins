#!groovy

 node {
   def mvnHome = tool 'M3'
   env.PATH = "${mvnHome}/bin:${env.PATH}"
   echo "var mvnHome='${mvnHome}'"
  echo "var env.PATH='${env.PATH}'"
  
   echo 'Descargando código de SCM'
   bat 'rm -rf *'
   checkout scm
 }
