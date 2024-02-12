pipeline {
        agent {
        node {
            label 'Agent-piro'       
        }
        }
        environment {
            name = "Sai Ramana "
            city = "Hyderabad"
        }
        options {
             timeout(time: 20, unit: 'SECONDS') 
             disableConcurrentBuilds()
        }
    // build
    stages {
        stage('DEV') {
            steps {
                echo ' DEV DONE'
                sh """
                echo "trigerred by $name from $city"
                 #sleep 10
                """ 
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
        stage('paramater') {
            steps {
                sh """

                """
            }
        }
        
    }
    post {
        always {
            echo "the build ran in always post"
        }
        success {
           sh """
            echo "build success by $name from $city "
            echo "this job is auto trigerred from git with webhook"
            """

        }
        failure {
            echo "build failed , please check and run again"
        }
        aborted {
            echo "the job has been aborted and Build not built"
        }
    }
}


