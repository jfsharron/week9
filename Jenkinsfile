pipeline {
     agent any
     stages {
          stage("update calculator") {
               steps {
                    sh "/usr/local/bin/kubectl apply -f calculator.yaml -n staging"
               }
          }
}
}