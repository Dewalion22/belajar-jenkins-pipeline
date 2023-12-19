pipeline {
    agent {
     node {
         label "linux && java11"
     }
    }
    
    stages {
        stage('Build') {
            steps {
                echo ('Start Build')
                sleep(10)
                echo ('Finish Build')

            }
        }

         stage('Test') {
            steps {
                echo 'Hello Test'
            }
        }

         stage('Deploy') {
            steps {
                echo 'Hello Deploy'
            }
        }
    }

    post {
        always {
            echo "I will alaways say Hello Again!"
        }
        success {
            echo "Yay, succes"
        }       
        failure {
            echo "oh no, failure"
        }
        cleanup {
            echo "Don't care succes or error"
        }
    }

}
