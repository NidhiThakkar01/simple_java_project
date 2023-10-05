pipeline {
    agent any
    stages {
        stage('Build Project') {
            steps {
                withMaven(
                    maven: 'Maven'
                ) {
                    sh('mvn clean install')
                }
            }
        }
        stage('Test Project') {
            steps {
                withMaven(
                    maven: 'Maven'
                ) {
                    sh('mvn test')
                }
            }
        }
    }
}
