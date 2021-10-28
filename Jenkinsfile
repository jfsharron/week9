pipeline {
     agent any
     stage("update calculator") {
       sh 'echo "starting update"'
       sh '''
         kubectl apply -f calculator.yaml -n staging
       '''         
     }
}
