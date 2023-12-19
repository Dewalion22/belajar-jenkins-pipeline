pipeline {
    agent {
     node {
         label "linux && java11"
     }
    }

    stages {
        stage('Test') {
            steps {
        
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
    }
        
}

   


