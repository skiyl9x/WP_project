properties([pipelineTriggers([githubPush()])])

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                git branch: 'main', 
                    credentialsId: 'eb41fdb4-beeb-428a-9c0e-20b054fd2597', 
                    url: 'git@github.com:skiyl9x/LEMP_stack.git'
                sh 'ls -la'
                sh 'docker build -t l9xhub/mariadb:1.0 Dockerfile'
            }
        }
        stage('Test') {
            steps {
                sh 'docker images'
            }
        }
    }
}
