pipeline {
    agent any
    
    tools {
        maven "jenkin-maven"
    }
    
    stages{
        stage('Build') {
            steps {
                git 'https://github.com/ashwin1-dev/18-feb-mvn2.git'
                sh "mvn clean package"
                sh "scp /var/lib/jenkins/workspace/mvn1/target/aaa.war  root@192.168.0.32:/opt/apache-tomcat/webapps/ex.war"
            }
        }
    }
}
