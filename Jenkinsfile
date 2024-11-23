pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/ErevanskShpak/SITAiRIS_Lab9.git'
            }
        }

        stage('Execute') {
            steps {
                bat 'ant ci'
            }
        }
    }
    post {
        success {
            echo 'Успешно выполнен'
        }
        failure {
            echo 'Провал'
        }
    }
}
