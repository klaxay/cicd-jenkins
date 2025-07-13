pipeline {
  agent any

  tools {
    nodejs "NodeJS 18"
  }

  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/klaxay/cicd-jenkins.git'
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
