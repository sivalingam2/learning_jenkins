pipeline {
    agent any
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
        stage('Deploy') {
            steps {
                echo "deploy"
            }
            stage(' app Deploy') {
                        steps {
                            echo "deploy"
                        }
                         stage(' app release') {
                                                steps {
                                                    echo "deploy"
                                                }

        }
    }
}