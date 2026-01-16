pipeline {
    agent {
        node {
            label 'maven'
        }
    }

    stages {
        stage('Clone Project Code') {
            steps {
                git branch: 'main', url: 'https://github.com/singhpalwinder27-ai/tweet-trend-for-Project2.git'
            }
        }
    }
}