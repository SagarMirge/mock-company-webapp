pipeline {
    agent any  // Run on any available agent (node)

    stages {
        stage('Build') {
            steps {
                script {
                    // Run the build command for Gradle
                    echo 'Building the project...'
                    sh './gradlew assemble'  // Run Gradle assemble to build the project
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    // Run the test command for Gradle
                    echo 'Running tests...'
                    sh './gradlew test'  // Run Gradle test to execute tests
                }
            }
        }
    }
    
    post {
        always {
            echo 'Cleaning up...'
            // Optional: clean up or notifications after the build
        }
    }
}
