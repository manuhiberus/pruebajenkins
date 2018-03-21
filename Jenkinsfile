#!groovy

node {
   
   // -- Compilando
   echo 'Compilando aplicación'
   bat 'mvn clean compile'
   
   // prueba
   // ------------------------------------
   // -- ETAPA: Instalar
   // ------------------------------------
   stage 'Instalar'
   echo 'Instala el paquete generado en el repositorio maven'
   bat 'mvn install
   
 
}
