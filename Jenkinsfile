pipeline {
    agent any

    stages {
        stage('Baixar index.html') {
            steps {
                script {
                    // Baixar o arquivo index.html diretamente do repositório GitLab
                    echo 'Baixando o arquivo index.html do GitLab...'
                    sh 'curl -o index.html https://gitlab.com/Relax-112/Jenkins_git/-/raw/main/index.html'
                }
            }
        }

        stage('Servir index.html') {
            steps {
                script {
                    // Servir o arquivo index.html com Python HTTP Server
                    echo 'Iniciando servidor HTTP...'
                    sh 'python3 -m http.server 8000 --bind 0.0.0.0'
                }
            }
        }
    }
}
