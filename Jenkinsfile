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
                awsCodeDeploy deploymentType: 's3', applicationName: 'jenkins-project', s3Bucket: 'mahesh-project-codedeploy', region: 'ap-south-1', deploymentGroup: 'jenkins-dg'
            }
        }
    }
}
