pipeline {
  agent {
    kubernetes {
      yaml '''
        apiVersion: apps/v1
        kind: Deployment
        metadata:
          name: calculator-deployment
          labels:
            app: calculator
        spec:
          replicas: 5
          strategy:
            type: RollingUpdate
            rollingUpdate:
              maxUnavailable: 25%
              maxSurge: 0
          selector:
            matchLabels:
              app: calculator
          template:
            metadata:
              labels:
                app: calculator
            spec:
              containers:
              - name: calculator
                image: leszko/calculator
                ports:
                - containerPort: 8080
                readinessProbe:
                  httpGet:
                     path: /sum?a=1&b=2
                     port: 8080
                '''
    }
  }
}