pipeline {
//     agent any
    agent { node { label 'workstation' } }
    tools {
            maven 'maven'
        }
//          options {
//                 ansiColor('xterm')
//             }

    //
    triggers { pollSCM(' */1 * * * *') }
        parameters {
            string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
  }
    stages {
        stage('Build') {
          input {
                                    message "Should we continue?"
                                    ok "Yes, we should."
                                    submitter "alice,bob"
                                    parameters {
                                        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                                    }
                                }
            steps {
                echo "build"
                sh 'mvn --version'
            }
        }
        stage('Test') {
         when {
                        branch 'production'
                    }
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