pipeline {
     agent any
     stages {
          stage("update calculator") {
               steps {
                    sh "ls -l"
                    sh "kubectl apply -f calculator.yaml"
               }
             }
     }
    }
