pipeline {
    agent any
    stages {
        stage('Install') { 
            steps {
                nodejs(nodeJSInstallationName: 'Node 11.x') {
                    sh 'npm install'
                }
            }
        }
        stage('Nexus Lifecycle evaluation') { 
            steps {
                nexusPolicyEvaluation iqApplication: 'juice-shop', iqStage: 'build'
            }
        }
    }
}
