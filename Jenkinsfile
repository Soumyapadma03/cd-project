pipeline {
    agent any

    environment {
        ANSIBLE_PATH = '/opt/homebrew/bin/ansible-playbook'
    }                                         
  
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Soumyapadma03/cd-project.git'
            }
        }
        stage('Deploy') {
            steps {
                sh """
                    /bin/sh -c '$ANSIBLE_PATH playbooks/deploy.yml -i inventory/hosts.ini'
                """
            }
        }
    }
}



