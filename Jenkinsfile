#!groovy

node {
   
   // -- Compilando
   echo 'Compilando aplicación'
   sh 'mvn clean compile'
   
   
   // ------------------------------------
   // -- ETAPA: Instalar
   // ------------------------------------
   stage 'Instalar'
   echo 'Instala el paquete generado en el repositorio maven'
   sh 'mvn install
   
 
}
