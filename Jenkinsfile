pipeline {
//     agent any
    agent { node { label 'workstation' } }
    stages {
        stage('Build') {
            steps {
                echo "build"
            }
        }
        stage('Test') {
            steps {
                 echo "test"
            }
        }
        stage(' app Deploy') {
            steps {
                echo "deploy"
            }


        }
    }
     post {
            always {
                echo 'I will always say Hello again!'
            }
        }
}