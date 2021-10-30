podTemplate(yaml: '''
    apiVersion: v1
    kind: Pod
    spec:
      containers:
      - name: centos
        image: centos
        command:
        - sleep
        args:
        - 99d
      restartPolicy: Never
''') {
  node(POD_LABEL) {
    stage('k8s') {
      git ' https://github.com/jfsharron/week9.git'
      container('centos') {
        stage('update calculator') {
          sh '''
          curl -k -v -XPATCH -H "Authorization: BearereyJhbGciOiJSUzI1NiIsImtpZCI6InQxU3I3czUxRDFWRUNTMnNORzlfSE1CY04tbjlDRER0cG9laEM3cW1qZzAifQ.eyJpc3MiOiJrdWJlcm5ldGVzL3NlcnZpY2VhY2NvdW50Iiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9uYW1lc3BhY2UiOiJkZXZvcHMtdG9vbHMiLCJrdWJlcm5ldGVzLmlvL3NlcnZpY2VhY2NvdW50L3NlY3JldC5uYW1lIjoiamVua2lucy10b2tlbi04bGZodiIsImt1YmVybmV0ZXMuaW8vc2VydmljZWFjY291bnQvc2VydmljZS1hY2NvdW50Lm5hbWUiOiJqZW5raW5zIiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9zZXJ2aWNlLWFjY291bnQudWlkIjoiYmM1MzQ4NTgtYzYwNi00MDBhLWFhNzktOTczNzgzNTQ1MjNhIiwic3ViIjoic3lzdGVtOnNlcnZpY2VhY2NvdW50OmRldm9wcy10b29sczpqZW5raW5zIn0.hqO4ixUJKIsVqa52-EFP7Wr9bHCoI0JNtTAb2DNb95FQ7mxTw4D0uFYbxv4eDvQDgBN-E-ihGitWVOn2t2C6keI6GncBKy5XyYyFTOLHuucne--Zr-IktRPJxWLxEXmbAioPMtRdu3KpFdXcARSM2o2QCTst353TnHvG7TUBcogzRAXyuqrV7rwVry5f-tysxlR4lVtoJ9WQDmw8Zsnp2v_PaUI_kGa3OuH6xeZihoxwQTG2M3za8CwvjMkj5MASltZLzboQRemmVpdhQxdQDqW4IH7181ouiI1urClO-PF2jAXtXcDbYrHk1KayyAjIfmqWJK0Vy6Es2cK9-12SPw"   -H "Accept: application/json" -H "Content-Type: application/strategic-merge-patch+json" -H "User-Agent: kubectl/v1.21.5 (darwin/amd64) kubernetes/aea7bba" 'https://10.43.0.1:443/apis/apps/v1/namespaces/staging/deployments/calculator-deployment?fieldManager=kubectl-client-side-apply' --data '{"spec":{"template":{"spec":{"containers":[{"name":"calculator","image":"dlambrig/hello-kaniko:1.0"}]}}}}'
          '''
        }   
      }
    }
  }
}