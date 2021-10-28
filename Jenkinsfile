pipeline {
  agent {
    kubernetes {
      yamlFile 'calculator.yaml'
    }
  }
   stages {
       stage("update calculator")
             steps {
                 sh "kubectl apply -f calculator.yaml"
             }
  }


}