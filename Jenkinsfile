pipeline {
    agent any
    
    stages {
        stage('CheckOut') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh '/home/therecker/DevOps/Maven/apache-maven-3.9.6/bin/mvn install'
            }
        }
        stage('Deployment') {
            steps {
                sh 'cp target/declare1.war /home/therecker/DevOps/Maven/apache-tomcat-9.0.85/webapps/'
            }
        }
    }
}
