pipeline {
    agent any

    stages {
        stage('Check Files') {
            steps {
                sh 'ls -l'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh 'sudo -u ansible ansible-playbook install_nginx.yml -i web,'
            }
        }

    }
}