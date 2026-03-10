pipeline {
    agent any

    stages {

        stage('Run Ansible Playbook') {
            steps {
                sh 'sudo -u ansible ansible-playbook nginx-playbook.yml -i localhost,'
            }
        }

    }
}