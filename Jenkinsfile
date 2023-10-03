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

    withCredentials([sshUserPrivateKey(credentialsId: "WebFinance-ssh", keyFileVariable: "keyHost")]) {
      stage('Desplegando en Servidor...') {
        sh 'echo ok'
      }
    }
    
  }
  
}
