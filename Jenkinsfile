pipeline {
  
  agent any

  tools {
    nodejs "nodejs"
  }

  stages {
    
    stage('Instalando dependencias...') {
      steps {
        sh 'npm install'
      }
    }

    stage('Testeando...') {
      steps {
        sh 'npm test'
    }
    
  }
  
}
