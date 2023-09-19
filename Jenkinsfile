// pipeline {
// //     agent any
//     agent { node { label 'workstation' } }
//     tools {
//             maven 'maven'
//         }
//         environment {
//         url = "google.com"
//          siva = credentials('centos-ssh')
//
//         }
// //          options {
// //                 ansiColor('xterm')
// //             }
//
//     //
//     triggers { pollSCM(' */1 * * * *') }
//         parameters {
//             string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//   }
//     stages {
//         stage('Build') {
// //           input {
// //                                     message "Should we continue?"
// //                                     ok "Yes, we should."
// //                                     submitter "alice,bob"
// //                                     parameters {
// //                                         string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
// //                                     }
// //                                 }
//             steps {
//                 echo "build"
//                 sh 'mvn --version'
//             }
//         }
//         stage('Test') {
//
//             steps {
//                  echo "test"
//                  echo url
//                  sh 'env'
//             }
//         }
//         stage(' app Deploy') {
//             steps {
//                 echo "deploy"
//             }
//
//
//         }
//     }
//      post {
//             always {
//                 echo 'I will always say Hello again!'
//                 echo 'send email'
//             }
//         }
// }
// pipeline {
//     agent any
//     stages {
//         stage('Non-Parallel Stage') {
//             steps {
//                 echo 'This stage will be executed first.'
//             }
//         }
//         stage('Parallel Stage') {
//
//             failFast true
//             parallel {
//                 stage('Branch A') {
//                     agent {
//                         label "for-branch-a"
//                     }
//                     steps {
//                         echo "On Branch A"
//                     }
//                 }
//                 stage('Branch B') {
//                     agent {
//                         label "for-branch-b"
//                     }
//                     steps {
//                         echo "On Branch B"
//                     }
//                 }
//                 stage('Branch C') {
//                     agent {
//                         label "for-branch-c"
//                     }
//                     stages {
//                         stage('Nested 1') {
//                             steps {
//                                 echo "In stage Nested 1 within Branch C"
//                             }
//                         }
//                         stage('Nested 2') {
//                             steps {
//                                 echo "In stage Nested 2 within Branch C"
//                             }
//                         }
//                     }
//                 }
//             }
//         }
//     }
// }
def sample() {
print "XYZ function"
}
node('workstation') {
def x = 10
env.y = 20

stage('build') {
print x
sh 'echo y - ${y}'
sample()
}
}
