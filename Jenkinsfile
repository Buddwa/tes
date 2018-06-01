pipeline {
    agent {label "master"}
    stages {
        stage('Build') {
            steps {
                ansiblePlaybook(credentialsId: 'root', inventory: '/root/gittes/hosts', playbook: '/root/gittes/mytest.yml')
            }
        }
}
}
