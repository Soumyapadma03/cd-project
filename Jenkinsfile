pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Soumyapadma03/cd-project.git'
            }
        }
        stage('Deploy') {
            steps {
                ansiblePlaybook credentialsId: 'ansible-ssh-key', inventory: 'inventory/hosts.ini', playbook: 'playbooks/deploy.yml'
            }
        }
    }
}


