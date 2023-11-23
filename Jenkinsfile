pipeline {
    agent any

    stages {
        stage('Run Frontend') {
            steps {
                echo 'executing yarn..'
                nodejs('NodeJS-21-2'){
                    sh 'yarn install'
                }
            }
        }
        stage('Gradle Version') {
  steps {
    // Get the gradle version
    def gradleVersion = sh(script: './gradlew -version', returnStdout: true).trim()

    // Print the gradle version
    echo "Gradle version: $gradleVersion"
  }
}
        }
}
        

