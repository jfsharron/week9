pipeline {
     node(10.42.3.186:8080)
     stages {
          stage("update calculator") {
               steps {
                    sh "kubectl apply -f calculator.yaml -n staging"
               }
          }
}
}