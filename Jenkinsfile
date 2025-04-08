pipeline {

    agent any

    stages {
        stage('Cloning Git') {
          steps {
              git([url: 'https://github.com/Cyust3/web_projects_lab_3', branch: 'master'])
          }
        }
        stage('Build') {
            steps {
                sh './gradlew clean build'
            }
        }


        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }
    }
}
