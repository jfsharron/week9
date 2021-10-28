pipeline {
     agent any
     stages {  
         stage("update calculator") {
           sh 'echo "starting update"'
           sh '''
             kubectl apply -f calculator.yaml -n staging
           '''         
         }
}
}
