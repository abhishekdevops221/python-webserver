pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/abhishekdevops221/python-webserver.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh '''
                python -m venv venv
                venv\\Scripts\\activate
                pip install -r requirements.txt
                '''
            }
        }
        stage('Run Application') {
            steps {
                sh 'python app.py'
            }
        }
    }
}
