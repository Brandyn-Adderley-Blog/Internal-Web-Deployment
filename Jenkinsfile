pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'make migrate_data'
                sh 'make collectstatic'
            }
        }
        stage('Test'){
            steps {
                sh 'make unit_test'
                junit 'reports/**/*.xml'
            }
        }
        
    }
}
