pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // chmod +x gives the script permission to run on Mac
                sh 'chmod +x Build.sh'
                sh './Build.sh'
            }
        }

        stage('Test') {
            steps {
                sh 'chmod +x Test.sh'
                sh './Test.sh'
            }
        }

        stage('Deploy') {
            steps {
                sh 'chmod +x Deploy.sh'
                sh './Deploy.sh'
            }
        }
    }
}
