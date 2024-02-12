pipeline {
        agent {
        node {
            label 'Agent-1'       
        }
        }
        environment {
            name = "Sai Ramana "
            city = "Hyderabad"
        }
        options {
        timeout(time: 1, unit: 'SECONDS') 
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
           sh """
            echo "build success by $name from $city "
            """
        }
        failure {
            echo "build failed , please check and run again"
        }
    }
}


