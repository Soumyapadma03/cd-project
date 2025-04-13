pipeline {
    agent any

    environment {
        // Ensure the correct path to Ansible is included
        PATH = "/opt/homebrew/bin:${env.PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Soumyapadma03/cd-project.git'
            }
        }
        stage('Deploy') {
            steps {
                ansiblePlaybook credentialsId: 'ansible-ssh-key', inventory: 'inventory/hosts.ini', playbook: 'playbooks/deploy.yml'
            }
        }
    }
}


