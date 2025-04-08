pipeline {

    stages {
        stage('Cloning Git') {
          steps {
              git([url: 'https://git.athene.tech/romanov73/example-web.git', branch: 'master'])
          }
        }
        stage('Test') {
            steps {
                sh 'java -version'
                sh "bash ./gradlew bootRun --args='--example-web.check-run=true'"
            }
        }
    }
}