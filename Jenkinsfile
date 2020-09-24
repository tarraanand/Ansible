pipeline {
    agent any
    parameters {
      choice choices: ['Anand', 'Harish'], description: 'Please choose the instance name', name: 'instance_name'
    }

    stages {
        stage('Hello') {
            steps {
                ansiblePlaybook inventory: 'hosts', playbook: 'playbook.yml', extras: '-e parameter="$instance_name"'
            }
        }
    }
}

