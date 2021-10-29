pipeline {
     node("server17")
     stages {
          stage("update calculator") {
               steps {
                    sh "kubectl apply -f calculator.yaml -n staging"
               }
          }
}
}