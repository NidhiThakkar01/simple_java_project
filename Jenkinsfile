pipeline {
    agent any
    tools{
        maven "maven"
    }
    stages {
        stage('Build Project') {
            steps {
                    sh 'mvn clean install'
                }
        }
        stage('Test Project') {
            steps {
                    sh 'mvn test'
                }
        }
        stage("Build project"){
            steps{
                sh "mvn package"
            }
        }
    }
    post{
        success{
            archiveArtifacts artifacts:'**/target/*.jar', allowEmptyArchive: true
        }
    }
}
