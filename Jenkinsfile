pipeline {
    agent any

    stages {
        stage('docker build') {
            steps {
              sh 'whoami'
                sh "docker build -t aminellouze/appang:${env.BUILD_NUMBER} . "
            }
        }
         stage('docker push') {
            steps {
                sh "docker push aminellouze/appang:${env.BUILD_NUMBER} "
            }
        }
    }
}
