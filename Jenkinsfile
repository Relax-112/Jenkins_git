pipeline {
    agent { label 'agent1' }  // Usa o agente 'agent1'
    
    stages {
        stage('Build') {
            steps {
                echo 'Building on agent1...'
                // Comandos de build aqui
            }
        }
        stage('Test') {
            steps {
                echo 'Testing on agent1...'
                // Comandos de teste aqui
            }
        }
    }
}
