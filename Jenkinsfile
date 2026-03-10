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
                sh 'sudo -u ansible ansible-playbook -i inventory install_nginx.yml'
            }
        }

    }
}