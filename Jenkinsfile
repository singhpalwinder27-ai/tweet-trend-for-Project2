pipeline {
    agent {
        node {
            label 'maven'
        }
    }
enviornment {
    PATH = "/opt/apache-maven-3.9.12/bin:$PATH"
}
    stages {
        stage('build') {
            steps {
               echo  "build started"
               sh 'mvn clean deploy'
               echo "build completed"
            }
        }
    }
}