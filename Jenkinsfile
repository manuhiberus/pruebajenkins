#!groovy

node {
    stage 'mvn clean'
    def mvnHome = tool 'M3'
    env.PATH = "${mvnHome}/bin:${env.PATH}"
    bat 'mvn clean'
    stage 'mvn install'
    bat 'mvn install'
}
