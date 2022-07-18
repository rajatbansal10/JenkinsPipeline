pipeline {
    agent any
    environment {
        NAME="Rajat"
    }

    stages {
        stage('Build') {
            steps {
                echo 'Build-Test'
                sh '''
                date
                cal 2022
                pwd
                '''
                
            }
        }
        
        stage('Test') {
            steps {
                echo 'Test-Test'
                echo "${NAME}"
                sh 'echo `expr 2 + 2`'
            }
        }
        
        stage('Continue ?') {
            input {
                message "Should we continue ?"
                ok "Yes we should"
            }
            
            steps {
                echo 'Deploy Test'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploy Test'
            }
        }
        
        stage('Monitor') {
            steps {
                echo 'Monitor Test'
            }
        }
    }
    post
    {
        failure{
            echo "Failure"
        }
            
        success{
            echo "Success"
        }
    }
}
