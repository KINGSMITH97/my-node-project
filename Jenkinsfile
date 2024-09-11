pipeline{
    agent any

    stages{
        stage('Git checkout'){
            steps{
                git branch: 'master', url: 'https://github.com/KINGSMITH97/my-node-project.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Deploying application') {
            steps {
                echo 'deploying application'
            }
        }
    }
}