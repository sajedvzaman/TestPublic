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


30351778 - DELAYED TASK CREATION IN SHM CAN LEAD TO UNEVEN LOAD BALANCING ACROSS OM SERVERS

36225600 - POC - INVOKEMETHOD GENERATES ERROR WHEN USED IN BROWSER SCRIPT IN SIEBEL - POC 23.12 WIN

36342661 - NON REPRO: HIGH CPU UTILIZATION ON EAI SERVER




        stage('Push repro to local website') {
            steps {
                echo 'Connect to localhost and pull down the latest version of the change'
                sh 'ssh -i ~/Key3/ssh-key-2024-02-20.key ubuntu@143.47.190.36 sudo git -C /var/www/html pull --allow-unrelated-histories'
            }


ssh -i ssh-key-2024-02-28.key ubuntu@144.21.38.188



        stage('Connect to OCI Server and Push latest Git Repository to OCI Ubuntu server') {
            steps {
                echo 'Connect to OCI Server and Push latest Git Repository to OCI Ubuntu server'
                sh 'ssh -i ~/KeyTest/ssh-key-2024-02-28.key ubuntu@144.21.38.188 sudo git -C /var/www/html pull'
            }





http://localhost:8080/

144.21.38.188

