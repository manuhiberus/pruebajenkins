#!groovy

node {
  
    def mvnHome = tool 'M3'
    env.PATH = "${mvnHome}/bin:${env.PATH}"
   
    stage 'mvn install'
    bat 'mvn install'
}
