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
        stage('git clone') {
            steps {
                sh 'sudo rm -r *;sudo git clone https://github.com/sabavnk/jenkins.git'
            }
        }
        stage('terraform init') {
            steps {
                sh 'sudo /var/lib/jenkins/workspace/terraform2 terraform init ./jenkins'
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
