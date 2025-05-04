
    pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/abhi-code26/test-project-jenkins.git'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'cd $WORKSPACE && npm test'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }
}

    

   
