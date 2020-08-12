pipeline {
    agent
    { node { label 'master' } }
    stages {
        stage('Snyk Test') {
            steps {
                sh 'ls -la'
                snykSecurity snykInstallation: 'SnykPlugin', snykTokenId: 'SnykAPI'
            }
        }
    }
}
