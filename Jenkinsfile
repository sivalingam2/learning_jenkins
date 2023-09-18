pipeline {
//     agent any
    agent { node { label 'workstation' } }
    tools {
            maven 'apache-maven-3.0.1'
        }
    //
    triggers { pollSCM(' */1 * * * *') }
        parameters {
            string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
  }
    stages {
        stage('Build') {
            steps {
                echo "build"
                sh 'mvn --version'
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
                echo 'send email'
            }
        }
}