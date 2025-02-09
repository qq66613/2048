pipeline {
    //Jobs akan di jalanakan pada server devops 1 -> root
    agent {
        node  {
            label 'devops1-kiki'
        }
    }
    //Step SDLC
    stage('Builds Images') {
            steps {
                sh 'docker compose build'
            }
        }
        stage('Deploy Images') {
            steps {
                sh 'docker compose up -d'
            }
        }
        stage('Publish Images') {
            steps {
                sh 'docker compose push'
            }
        }
}
