pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/ela103/p.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip install selenium'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'python3 f.py'
            }
        }
    }

    post {
        always {
            echo 'Pipeline terminé !'
        }
        success {
            echo 'Tous les tests ont réussi.'
        }
        failure {
            echo 'Certains tests ont échoué.'
        }
    }
}
