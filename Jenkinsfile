pipeline {
    agent any
    triggers {
        githubPush()
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/<your-repo>.git'
            }
        }
        stage('Validation') {
            steps {
                echo "Running validation..."
                sh 'python -m unittest discover'
            }
        }
    }
}
