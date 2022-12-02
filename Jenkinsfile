pipeline {
         agent any
         stages {
                 stage('Code') {
                 steps {
                     echo 'Welcome to Jenkins'
                 }
                 }
                 stage('Build') {
                 steps {
                    input('Do you want to proceed?')
                 }
                 }
                 stage('Test') {
                 when {
                       not {
                            branch "master"
                       }
                 }
                 steps {
                       echo "Hello"
                 }
                 }
                 stage('Four') {
                 parallel { 
                            stage('Unit Test') {
                           steps {
                                echo "Running the unit test..."
                           }
                           }
                            stage('Integration test') {

                              steps {
                                echo "Running the integration test..."
                              }
                           }
                           }
                           }
              }
}
