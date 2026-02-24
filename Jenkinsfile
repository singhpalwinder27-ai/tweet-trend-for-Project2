pipeline {
    agent {
        node {
            label 'maven'
        }
    }

    environment {
        PATH = "/opt/apache-maven-3.9.12/bin:$PATH"
    }

    stages {

        stage('Build') {
            steps {
                echo "Build started"
                sh 'mvn clean deploy'
                echo "Build completed"
            }
        }

        stage('SonarQube Analysis') {
            environment {
                scannerHome = tool 'fqts-sonar-scanner'
            }
            steps {
                withSonarQubeEnv('fqts-sonar-server') {
                    sh "${scannerHome}/bin/sonar-scanner"
                }
            }
        }

    }
}