pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'cd jenkinsfetch'
                sh './gradlew check'
            }
        }
    }
    post {
        always {
            junit 'build/reports/**/*.xml'
        }
    }
}
