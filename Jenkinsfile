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
        stage('Run backend') {
            steps {
                echo 'executing gradle......'
                withGradle(){
                    sh './gradlew -v'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
