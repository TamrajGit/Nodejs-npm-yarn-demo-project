pipeline {
    agent any
    tools {
        gradle 'Gradle'
    }

    stages {
        stage('run Frontend') {
            steps {
                echo 'yarn ....'
                nodejs('NodeJS-21-2'){
                    sh 'yarn install'
            }
        }
        stage('run Backend') {
            steps {
                echo 'executing gradle....'
                sh './gradlew -v'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
