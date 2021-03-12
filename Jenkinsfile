pipeline {
    agent { docker { image 'image1' } }
    stages {
        stage('Test') {
            steps {
                sh 'python3.8 -m unittest'
            }
        }
        stage('Deployment') {
            steps {
                
                sh 'zip -r lambdacode.zip src/*'
                sh 'aws lambda update-function-code --function-name  lambdacdshalini --zip-file fileb://lambdacode.zip'
                sh 'rm -rf lambdacode.zip'
                
            }
    }
}
