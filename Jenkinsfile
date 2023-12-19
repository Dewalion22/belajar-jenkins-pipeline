pipeline {
    agent {
     node {
         label "linux && java11"
     }
    }
    
    stages {
        stage('Build') {
            steps {
                script {
                    for (int i = 0; i< 10; i++){
                        echo("Script ${i}")
                    }
                }
                
                echo ('Start Build')
                sh("./mvnw clean compile test-compile")
                echo ('Finish Build')

            }
        }
        stage('Deploy') {
            steps {
                echo 'Hello Deploy'
            }
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



