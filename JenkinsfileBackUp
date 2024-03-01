pipeline {
    agent any 
    stages {
        stage('Clone The Git Repository') {
            steps {
                echo 'Clone The Git Repository'
                sh 'rm -fr TestPublic'
                sh 'git clone https://github.com/sajedvzaman/TestPublic.git'
            }
        }
        stage('Pull in the latest Git Repository to Ubuntu OCI server') {
            steps {
                echo 'Connect to OCI Server and Push latest Git Repository to OCI Ubuntu server'
                sh 'ssh -i ~/KeyTest/ssh-key-2024-02-28.key ubuntu@144.21.38.188 sudo git -C /var/www/html pull'
            }
        }
        stage('Check Website Is Up') {
            steps {
                echo 'Check website is up and running'
                sh 'curl -Is 144.21.38.188 | head -n 1' 
            }
        }
    }
}
