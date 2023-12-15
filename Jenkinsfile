pipeline {
    agent {
     node {
         label "linux && java11"
     }
    }
    
    stages {
        stage('Hello') {
            steps {
                echo 'Hello Pipeline'
            }
        }
    }

    post {
        always {
            echo "I will alaways say Hello Again"
    }
        succes {
            echo "Yay, succes"
        }       
        failure {
            echo "oh no, failure"
        }
    }

}
