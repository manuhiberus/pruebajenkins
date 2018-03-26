#!groovy

node {
    stage 'mvn Limpieza'
    def mvnHome = tool 'M3'
    env.PATH = "${mvnHome}/bin:${env.PATH}"
    bat 'mvn clean'
}
