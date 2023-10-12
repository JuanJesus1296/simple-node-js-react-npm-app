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

    stage('Compilando...') {
      steps {
        sh 'npm run build'
      }
    }

    stage('Testeando...') {
      steps {
        sh 'npm test'
      }
    }


    
  }
  
}
