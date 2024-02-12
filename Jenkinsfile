pipeline {
        agent {
        node {
            label 'Agent-1'       
        }
        }
    // build
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
    post {
        always {
            echo "the build ran"
        }
        success {
            echo "build success"
        }
        failure {
            echo "build failed , please check and run again"
        }
    }
}


