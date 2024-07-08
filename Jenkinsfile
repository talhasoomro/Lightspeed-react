pipeline {
    agent any

    tools { nodejs "NodeJS"}
 
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/talhasoomro/Lightspeed-react.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
    }

    post {
        always {
            cleanWs()
        }
    }
}
