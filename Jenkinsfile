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

    stage('Desplegando en Servidor...') {
      steps {
        withCredentials([sshUserPrivateKey(credentialsId: "WebFinance-ssh", keyFileVariable: "keyHost")]) { 
          sh 'rsync -e "ssh -i $keyHost" -avz build/ ansible@192.168.0.17:/var/www/html/webFinance'
        }
      }
    }
    
  }
  
}
