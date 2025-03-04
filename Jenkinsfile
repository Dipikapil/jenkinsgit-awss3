pipeline {
    agent any
    stages {
        stage('List S3 Buckets') {
            steps {
                script {
                    withCredentials([aws(accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'awsjenkinsid', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY')]) {
                        sh '''
                            aws s3 ls
                        '''
                    }
                }
            }
        }
    }
}