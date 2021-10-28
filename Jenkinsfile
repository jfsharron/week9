pipeline {
  agent {
    kubernetes {
      yamlFile 'calculator.yaml'
    }
  }

       stage("update calculator")

                 sh "kubectl apply -f calculator.yaml"
             
  


}