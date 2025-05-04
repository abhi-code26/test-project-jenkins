
    
pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/abhi-code26/test-project-jenkins.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'cd $WORKSPACE && npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'cd $WORKSPACE && npx jest'
            }
        }

        stage('Build') {
            steps {
                sh 'cd $WORKSPACE && npm run build'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check logs for issues.'
        }
    }
}


    

   
