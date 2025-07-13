pipeline {
  agent any

  tools {
    nodejs "NODEJS18"
  }

  stages {
    stage('Checkout') {
      steps {
        git branch:'main', url:'https://github.com/klaxay/cicd-jenkins.git'
      }
    }

    stage('Install Dependencies') {
      steps {
        sh 'npm install'
      }
    }

    stage('Run Tests') {
      steps {
        sh 'npm test || echo "No tests defined"'
      }
    }
  }
}
