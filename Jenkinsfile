pipeline {
  agent any
  stages {
    stage('build app container'){
      steps {
        sh "docker build -t flask-app ./Dockerfile"
      }
    }
    stage('build nginx container'){
      steps {
        sh "docker build -t nginx ./Dockerfile.nginx"
      }
    }
  }
}
