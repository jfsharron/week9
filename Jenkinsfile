pipeline {
    agent any
    stages {
        stage('Deploy on kubernetes') {
            steps {
                kubernetesDeploy(
                    kubeconfigId: 'k8s-default-namespace-config-id',
                    configs: 'dcalculator.yaml',
                    enableConfigSubstitution: true
                )
            }
        }
    }
}
