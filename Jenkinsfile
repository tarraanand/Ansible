pipeline {
    agent any
    parameters {
      choice choices: ['Anand', 'Harish'], description: 'Please choose the instance name', name: 'instance_name'
    }

    stages {
        stage('Launch Instance') {
            steps {
                ansiblePlaybook inventory: 'hosts', playbook: 'test.yml', extras: '-e parameter="${instance_name}"'
            }
        }
    }
}

