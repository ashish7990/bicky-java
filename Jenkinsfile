pipeline {
    agent {
        node {
            label 'jenkins-slave-label'
        }
    }
    
    stages {
        stage('checkout code') {
            steps {
                git branch: 'main', url: 'https://github.com/ashish7990/web-app.git'
            }
        }
        stage('build code') {
            steps {
                sh '/opt/maven/bin/mvn clean package'
            }
        }
    }
}
