pipeline {
    agent any

    stages {
        stage('Baixar index.html') {
            steps {
                script {
                    echo 'Baixando o arquivo index.html do GitLab...'
                    sh 'curl -o index.html https://gitlab.com/Relax-112/Jenkins_git/-/raw/main/index.html'
                }
            }
        }

        stage('Servir index.html') {
            steps {
                script {
                    echo 'Iniciando servidor HTTP...'
                    sh 'python3 -m http.server 30000 --bind 0.0.0.0'
                }
            }
        }
    }
}
