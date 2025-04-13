pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Soumyapadma03/cd-project.git'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying with Ansible...'
                sh label: 'Run Ansible Playbook', script: '/bin/sh -c "/opt/homebrew/bin/ansible-playbook -i inventory/hosts.ini playbooks/deploy.yml"'
            }
        }
    }
}




