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
        stage('Deploying application') {
            steps {
                echo 'deploying application'
            }
        }
        stage('Deploy') {
            steps {
                sshagent(credentials: ['ssh']) {
                    sh '''
                    ssh ubuntu@3.90.15.163 '
                    cd /path/to/your/application &&
                    git pull origin main &&
                    npm install &&
                    pm2 restart app.js'
                    '''
                }
            }
        }
    }
}
