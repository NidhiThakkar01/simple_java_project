pipeline {
    agent any
    triggers {
        cron('* * * * *')
    }
    stages {
        stage('Checkout') {
            steps {
                git(url: "https://github.com/NidhiThakkar01/simple_java_project", branch: "master")
            }
        }
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
