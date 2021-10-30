pipeline {
  agent {
    kubernetes {
      yaml '''
      spec:
        containers:
        - name: gradle
          image: gradle:6.3-jdk14
      '''
    }
}
stages {
  stage('update calculator') {
    steps {
      echo "updating"
      kubectl apply -f calc2.yaml 
    }
  }
}
}