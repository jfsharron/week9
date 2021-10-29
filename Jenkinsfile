pipeline {
     agent master
     stages {
          stage("update calculator") {
               steps {
                    sh "kubectl apply -f calculator.yaml -n staging"
               }
          }
}
}