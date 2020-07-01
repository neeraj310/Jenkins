pipeline {
    agent any
    stages {
        stage('build') {
        parallel { 
                            stage('PY3 Build') {
                           steps {
                				echo  "first demo in python3"
                				sh  '''pwd
                       				python3 demo.py
                    				'''
            					}
                           }
                            stage('PY2 Build') {
                           steps {
                				echo  "first demo in python2"
                				sh  '''pwd
                       				python demo.py
                    				'''
            					}
                           }
            	 }	
                           
            
        }
        stage('Test') {
            steps {
                echo 'Testing my first demo..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying my first demo....'
            }
        }
    }
}
