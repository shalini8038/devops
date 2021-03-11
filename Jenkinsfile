pipeline {
    agent { docker { image 'image1' } }
    stages {
        stage('Test') {
            steps {
                sh 'python3.8 -m unittest'
            }
        }
    }
}