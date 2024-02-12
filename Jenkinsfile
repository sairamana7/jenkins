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
        parameters {
        string(name: 'trigerred by', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'reason', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'terms and conditions', defaultValue: true, description: 'Accept to proceed')

        choice(name: 'pick the version', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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


