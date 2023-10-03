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

    stage('Desplegando en Servidor...') {
      steps {
        withCredentials([sshUserPrivateKey(credentialsId: "WebFinance-ssh", keyFileVariable: "keyHost")]) { 
          sh 'echo ok'
        }
      }
    }
    
  }
  
}
