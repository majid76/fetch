pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'pwd'

            }
        }
    }
    post {
        always {
            junit 'build/reports/**/*.xml'
        }
    }
}
