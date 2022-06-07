pipeline {
    agent {
      docker {image 'goturk'}
    }

    stages {
      
        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }
       
        stage('Static Code Analysiz') {
            steps {
                echo 'static analysis...'
            }
        }
        stage('test') {
            steps {
                sh 'node --version'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build -t first-build .'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploying...'
            }
        }
    }
}
