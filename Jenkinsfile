pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from Git repository
                git 'https://github.com/sachdevaak/https://github.com/sachdevaak/katalonTesting.git'
            }
        }
        
        stage('Build') {
            steps {
                // Compile your Java code (if required)
                sh 'javac KatalonApp.java'
            }
        }
        
        stage('Test') {
            steps {
                // Run your Katalon tests
                sh 'java -cp .:junit.jar:hamcrest-core.jar org.junit.runner.JUnitCore KatalonAppTest'
            }
        }
    }
    
    post {
        success {
            echo 'Build and tests passed successfully!'
            // Additional post-build actions if needed
        }
        failure {
            echo 'Build or tests failed!'
            // Additional actions for failure handling
        }
    }
}
