pipeline {
    agent { node { label 'Agent-1' } }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                ls -l
                pwd
                echo "Hello from gibhub push webhook"
                '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    
    post { 
        always { 
            echo 'I will always run whether job is success or not'
        }
        success {
            echo 'I will run only when job is success'
        }
        failure { 
             echo 'I will run when job is failed'
        }
    }
}
