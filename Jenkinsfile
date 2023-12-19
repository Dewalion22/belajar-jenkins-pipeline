pipeline {
    agent {
     node {
         label "linux && java11"
     }
    }

    stages {
        stage('Test') {
            steps {
                    echo ("Start Test")

            script {
                  def data = [
                      "firstName": "Eko",
                      "lastName" : "Khannedy"
                      ]
              writeJSON(file: "data.json", json: data)
            }
                
            
            echo ("Finish Test")
            }
        }    
    }
        
}

   


