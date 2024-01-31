pipeline {
    agent any

    stages {
        stage('SCM') {
            steps {
                git branch: 'main', url: 'https://github.com/vikramkujur/SL-Docker-jenkins-pipeline-project.git'
            }
        }
        stage('build image') {
            steps {
                sh '''cd /var/lib/jenkins/workspace/git-test
                      docker build -t test .'''
            }
        }
        // stage('Deploy') {
        //     steps {
        //         echo 'Deploying....'
        //     }
        // }
    }
}