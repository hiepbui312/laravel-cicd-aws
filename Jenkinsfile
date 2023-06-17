pipeline {
    agent { 
        node {
            label 'hiepbui'
        }
    }
    stages {
        stage("Start Docker") {
            steps {
                sh 'docker compose ps'
            }
        }
        stage("Run Composer Install") {
            steps {
                sh 'docker compose run --rm composer install'
            }
        }
        stage("Run Tests") {
            steps {
                sh 'docker compose run --rm artisan test'
            }
        }
    }
}
