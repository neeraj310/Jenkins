pipeline {
         agent any
         stages {
                 stage('Build') {
                 steps {
                     echo 'This is the build State'
                 }
                 }
                 stage('State_Two') {
                 steps {
                    input('Do you want to proceed?')
                 }
                 }
                 stage('State_Three') {
                 when {
                       not {
                            branch "abc"
                       }
                 }
                 steps {
                       echo "This is 3rd State"
                 }
                 }
                 stage('Testing') {
                 parallel { 
                            stage('Unit Test') {
                           steps {
                                echo "Running the unit test..."
                           }
                           }
                            stage('Integration test') {
                           steps {
                                echo5 "Running the integration test..."
                              }
                           }
                           }
                           }
              }
}
