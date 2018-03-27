#!groovy

node {
  
   // def mvnHome = tool 'M3'
   // env.PATH = "${mvnHome}/bin:${env.PATH}"
   
       agent any    //Agente de Docker, de momento no utilizo Docker
     tools { //Alias a herramientas instaladas en Jenkins
        maven 'M3' //M3 es el nombre que le puse al maven instalado para Jenkins
        jdk 'JDK8' //JDK8 es el nombre que le puse al java de Jenkins
    }

}
