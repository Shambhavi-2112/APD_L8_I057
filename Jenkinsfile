pipeline {
    agent any
    
    tools {
        maven 'maven_3' 
    }

    stages {
        stage('Build') {
            steps {
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
                sh 'mkdir -p /Users/saumya_shambhavi/Desktop/Jenkins_Deploy'
                sh 'cp target/*.jar ~/Desktop/Jenkins_Deploy/'
            }
        }
    }
}
