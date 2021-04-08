pipeline {
    agent {
        node {
            label 'master'
        }
    }

    stages {

        stage('terraform started') {
            steps {
                sh 'echo "Started...!" '
            }
        }
        stage('git checkout') {
            steps {
                git credentialsId: 'GIT', url: 'https://github.com/sabavnk/jenkins.git'
            }
        }
        stage('terraform init') {
            steps {
                sh 'sudo /home/ubuntu/ terraform init ./jenkins'
                sh 'pwd'
            }
        }
        stage('terraform plan') {
            steps {
                sh 'ls ./jenkins; sudo /home/ubuntu/ terraform plan ./jenkins'
            }
        }
        stage('terraform ended') {
            steps {
                sh 'echo "Ended...!!"'
            }
        }
    }
}
