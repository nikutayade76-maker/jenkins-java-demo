pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Use the 'git' step with a 'url' parameter
                git url: 'https://github.com/nikutayade76-maker/jenkins-java-demo.git' 
            }
        }
        stage('Publish') {
            steps {
                // 'publishHTML' step takes a 'target' nested object
                publishHTML([
                    target: [
                        allowMissing: true,
                        alwaysLinkToLastBuild: false,
                        keepAll: false,
                        reportDir: '.',
                        reportFiles: 'love.html',
                        reportName: 'My html report'
                    ]
                ])
            }
        }
    }
}
