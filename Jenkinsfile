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
        fingerprint 'target/my-webapp (1).war'
      }
    }

    stage('Testeando...') {
      steps {
        sh 'npm test'
      }
    }


    
  }
  
}
