pipeline {
    agent any 
    stages {
        stage('Clone the repro') {
            steps {
                echo 'Clone the repro'
                sh 'rm -fr TestPublic'
                sh 'git clone https://github.com/sajedvzaman/TestPublic.git'
            }
        }
        stage('Push repro to local website') {
            steps {
                echo 'Connect to localhost and pull down the latest version of the change'
                sh 'ssh -i ~/Key3/ssh-key-2024-02-20.key ubuntu@143.47.190.36 sudo git -C /var/www/html pull --allow-unrelated-histories'
            }
        }
        stage('Check website is up') {
            steps {
                echo 'Check website is up and running'
                sh 'curl -Is 143.47.190.36 | head -n 1'
            }
        }
    }    
}
