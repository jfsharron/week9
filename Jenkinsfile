pipeline {
     agent any
     stages {
          stage("update calculator") {
               steps {
                    sh "kubectl -f calculator.yaml -n staging"
               }
          }
}
}