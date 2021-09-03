pipeline {
    agent any
    environment {
         PATH = "/usr/share/maven/bin/:$PATH"
    }
    stages {
        stage('fetch from git') {
            steps {
               git 'https://github.com/Baddamnikhilreddy/springboot.git'   
            }
        }
         stage('build a package') {
            steps {
                sh 'mvn clean package'
            }
        }
         stage('Deploy to tomcat') {
            steps {
                sh 'mvn package'
            }
        }   
    }
}

