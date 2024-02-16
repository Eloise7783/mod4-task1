pipeline {
  agent any
  stages {
    stage('build app container'){
      steps {
        sh "docker build -t flask-app ."
      }
    }
    stage('build nginx container'){
      steps {
        sh "docker build -t nginx -f Dockerfile.nginx"
      }
    }
  }
}
