pipeline {
    agent any

    tools {
        nodejs 'node18' // Make sure this name matches your Global Tool Configuration
    }

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning repository...'
                checkout scm
            }
        }

        stage('Install') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'npm run check'
            }
        }
    }

    post {
    always {
        echo 'Pipeline finished'
        echo 'Build succeeded!'
    }
}

}
