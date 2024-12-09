pipeline {
    agent any

    stages {
        stage('Instalar Python 3') {
            steps {
                script {
                    echo 'Atualizando pacotes e instalando Python 3 como root...'
                    sh '''
                    sudo apt-get update
                    sudo apt-get install -y python3
                    '''
                }
            }
        }

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
