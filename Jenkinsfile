pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                ansiblePlaybook inventory: 'hosts', playbook: 'playbook.yml'
            }
        }
    }
}

