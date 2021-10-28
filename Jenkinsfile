pipeline {
     agent any

     stages {
         stage("update calculator")
               steps {
                    sh "kubectl apply -f calculator.yaml"
               }
         }
}
