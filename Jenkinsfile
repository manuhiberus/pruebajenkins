#!groovy

node {
   
   // -- Compilando
   echo '${env.JOB_NAME}-${env.BUILD_ID}'
   stage('instalacion'){
   bat 'mvn install'
   
   }
}
