pipeline {
    agent {
        docker {
            image 'node:11-alpine' 
        }
    }
    stages {
        stage('Install') { 
            steps {
                sh 'npm install' 
            }
        }
        stage('Nexus Lifecycle evaluation') { 
            steps {
                nexusPolicyEvaluation iqApplication: 'juice-shop', iqStage: 'build'
            }
        }
    }
}
