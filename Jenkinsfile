pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Build your application
                sh 'mvn clean package'
            }
        }
        stage('Deploy') {
            steps {
                // Deploy using AWS CodeDeploy
                awsCodeDeploy deploymentType: 's3', applicationName: 'YourCodeDeployApp', s3Bucket: 'your-s3-bucket', region: 'your-region', deploymentGroup: 'your-deployment-group'
            }
        }
    }
}
