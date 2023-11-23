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
                    bash './gradle -version'
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
