pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                dir('/Users/<user_name>/Downloads/ci-samples-master'){
                    bat 'docker run -t --rm -v "$(pwd)":/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/Users/Akhil/IdeaProjects/untitled
 -browserType="Chrome" -retry=0 -statusDelay=15 -testSuitePath="Test Suites/TS_RegressionTest" -apiKey=6052bbfe-f4fc-4553-b334-6769d9eff78b'
                }
            }
        }
    }
