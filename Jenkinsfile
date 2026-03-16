pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Grant permission and run your build script
                sh 'chmod +x Build.sh'
                sh './Build.sh'
            }
        }

        stage('Test') {
            steps {
                // Grant permission and run your test script
                sh 'chmod +x Test.sh'
                sh './Test.sh'
            }
        }

        stage('Deploy') {
            steps {
                // Grant permission and run your deploy script
                sh 'chmod +x Deploy.sh'
                sh './Deploy.sh'
            }
        }
    }
}
