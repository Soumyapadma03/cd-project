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
                sh """
                  $ANSIBLE_PATH playbooks/deploy.yml -i inventory/hosts.ini
                """
            }
        }
    }
}




