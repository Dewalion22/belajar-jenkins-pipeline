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
                sh("./mvnw clean compile test-compile")
                echo ('Finish Build')

            }
        }
        stage('Test') {
            script {
          def data = [
              "firstName": "Eko",
              "lastName" : "Khannedy"
          ]
          writeJSON(file: "data.json", json: data)
        }
                
            
                echo ('Start Test')
                sh("./mvnw test")
                echo ("Finish Test")
            }
        }

    stage('Deploy') {
            steps {
            
                echo ('Start Deploy')
                echo ("Finish Deploy")
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

   


