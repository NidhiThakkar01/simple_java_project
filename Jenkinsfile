pipeline {
    agent any
    tools{
        maven "Maven"
    }
    stages {
        stage('Build Project') {
            steps {
                    sh 'mvn clean install'
                }
            }
        }
        stage('Test Project') {
            steps {
                    sh 'mvn test'
                }
            }
        }
    }
}
