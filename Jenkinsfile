pipeline {
    agent any

    stages {
        stage('SCM_checkout') {
            steps {
              git url: "https://github.com/devops98/shopizerMaven.git", branch: 'master'
            }
        }

        stage('Build') {
            steps {
                echo "build started"                
                echo "build finished"
            }
        }
        stage('Unit_Test'){
            steps {
                echo "execute unit test"
            }
        }
        stage('SonarQube'){
            steps {
                echo "SonarQube Analysis"
            }
        }
        stage('Nexus_deploy') {
            steps {
                echo "push to nexus"
            }
        }
        stage('deploy_to_env') {
            steps {
            echo "build deployed"
            }
        }
        stage('email') {
           steps {
                echo "email sent"
            }
        }
    }
}
