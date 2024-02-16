pipeline {
  agent any
  stages {
    stage('build app container'){
      steps {
        sh "docker build -t taskone ."
      }
    }
    stage('build nginx container'){
      steps {
        sh "docker build -t nginxcont .nginx"
      }
    }
  }
}
