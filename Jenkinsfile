pipeline {
   agent any
   stages {
     stage('checkoutcode') {
         steps{
             git branch: 'main', url: 'https://github.com/ashish7990/web-app.git'
         }
     }
     stage('buildcode'){
         steps{
            sh 'mvn clean package'
         }
      
     }
     stage('deploy to tomcat') {
        steps {
            deploy adapters:[tomcat9(url:'http://13.250.30.122:8080/', credentialsId:'tomcatcred')] , war: '**/*.war'
        }
     }
   }
}