pipeline {
    agent {
        label 'agent-1'
    } 
    options{
        timeout(time: 10, unit: 'MINUTES')
    }
    stages {
        stage('Build') { 
            steps {
                sh 'echo this is build'

                }
            }
        
        stage('Test') { 
            steps {
             sh  'echo this is test'  
            }
        }
        stage('Deploy') { 
            steps {
               sh 'echo this is deploy'
            }
        }
    }

 post {
        always{
            echo "This sections runs always"
            deleteDir()
        }
        success{
            echo "This section run when pipeline success"
        }
        failure{
            echo "This section run when pipeline failure"
        }
    }
}