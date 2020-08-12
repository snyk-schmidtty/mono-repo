pipeline {
    agent
    { node { label 'master' } }
    stages {
        stage('Snyk Test') {
            steps {
                sh 'ls -la'
                snykSecurity additionalArguments: '--all-projects', failOnIssues: false, snykInstallation: 'SnykPlugin', snykTokenId: 'SnykAPI'
            }
        }
    }
}
