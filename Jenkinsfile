pipeline {
  agent any
  environment {
    // Set the Node.js version you want to use
    NODE_VERSION = '14.17.0'
  }
  stages {
    stage('Checkout') {
      steps {
        // Checkout the code from your source code management system
        checkout scm
      }
    }
    stage('Install Dependencies') {
      steps {
        // Install the Node.js dependencies
        sh 'npm install'
      }
    }
    stage('Run Tests') {
      steps {
        // Run the tests for your project
        sh 'npm test'
      }
    }
    stage('SonarScanner') {
      steps {
        // Run SonarScanner with the necessary parameters
        withSonarQubeEnv('My SonarQube Server') {
          sh 'sonar-scanner'
        }
      }
    }
  }
}
