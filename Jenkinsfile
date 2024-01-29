pipeline {
    agent any

       stages {
        stage('Instalación de Dependencias') {
            steps {
                script {
                    def result = sh(script: 'npm install', returnStatus: true)
                    echo "Resultado de npm install: ${result == 0}"
                }
            }
        }

        stage('Construyendo la App') {
            steps {
                script {
                    def result = sh(script: 'npm run ng build', returnStatus: true)
                    echo "Resultado de npm run ng build: ${result == 0}"
                }
            }
        }

        stage('Moviendo la carpeta para su ejecución') {
            steps {
                script {
                    def result = sh(script: 'cp -r $WORKSPACE/dist $HOME/Work/itsmqet/nginx', returnStatus: true)
                    echo "Resultado de cp: ${result == 0}"
                }
            }
        }
    }
}
