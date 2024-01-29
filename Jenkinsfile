node {
    state('Instalación de Dependencias'){
        'npm install'
    }
    stage('Construyendo la App'){
        'npm run ng build'
    }
    stage('Moviendo la carpeta para su ejecucion') {
        'cp -r /Users/mrmango1/.jenkins/workspace/web2-rutasDinamicas/dist /Users/mrmango1/Work/itsmqet/nginx'
    }
}