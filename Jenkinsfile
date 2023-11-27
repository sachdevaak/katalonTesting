pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                dir('/Users/Akhil/IdeaProjects/untitled') { // Replace with your project directory path
                    bat '''
                        docker run -t --rm -v %WORKSPACE%:/tmp/project katalonstudio/katalon \
                        katalonc.sh -projectPath=/tmp/project -browserType="Chrome" \
                        -retry=0 -statusDelay=15 -testSuitePath="Test Suites/TS_RegressionTest" \
                        -apiKey=6052bbfe-f4fc-4553-b334-6769d9eff78b'
                    '''
                }
            }
        }
    }
}
