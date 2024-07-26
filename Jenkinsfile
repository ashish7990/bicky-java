node {
    stage('checkoutcode'){
        git branch: 'main' , url: 'https://github.com/ashish7990/web-app.git'
    }
    stage('buildcode'){
        sh '/opt/maven/bin/mvn clean package'
        
    }    
    stage('deploy to tomcat container'){
        deploy adapetrs: [tomcat9(url: 'http://18.140.66.218:8080' , credentialsId: 'tomcatcred')] , war: '**/*.war'
        
    }
}