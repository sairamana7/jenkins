pipeline {
        agent {
        node {
            label 'Agent-1'       
        }
        }

    stages {
        stage('DEV') {
            steps {
                echo ' DEV DONE'
            }
        }
        stage('QA') {
            steps {
                echo 'QA COMPLETED '
            }
        }
        stage('PROD') {
            steps {
                echo ' DEPLOYMENT DONE'
            }
        }
        stage('deployed') {
            steps {
                echo 'DONE123 '
            }
        }
        
    }
}


