pipeline {
    agent any

    stages {
        stage('Validate Ansible Playbook') {
            steps {
                sh """
                sudo -u ansible ansible-playbook -i inventory playbook.yml --check
                """
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh """
                sudo -u ansible ansible-playbook -i inventory playbook.yml -v
                """
            }
        }
    }

    post {
        success {
            echo 'Ansible playbook executed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check logs above.'
        }
    }
}