pipeline {
  agent any
  environment {
    SCANNER_HOME = tool 'SonarQube'
  }
  stages {
    stage('Test') {
      steps {
        withSonarQubeEnv('SonarQube') {
          sh "${SCANNER_HOME}/bin/sonar-scanner \
            -D sonar.projectKey=adv_java \
            -D sonar.projectName=Unreal-Engine-pro"
        }
      }
    }
  }
}
