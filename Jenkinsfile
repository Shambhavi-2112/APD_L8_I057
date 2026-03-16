pipeline {
    agent any

    stages {
        stage('Pull from Git') {
            steps {
                // Clones the repository
                git branch: 'main', url: 'https://github.com/kapilrahtor/Jenkins_pipeline.git'
            }
        }

        stage('Build') {
            steps {
                // Compiles the code and creates a JAR/WAR file
                sh 'mvn clean package -DskipTests'
            }
        }

        stage('Test') {
            steps {
                // Runs unit tests
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Example: Copying the build artifact to a local deployment folder on your Mac
                sh 'mkdir -p ~/Desktop/Jenkins_Deploy'
                sh 'cp target/*.jar ~/Desktop/Jenkins_Deploy/'
            }
        }
    }
}
