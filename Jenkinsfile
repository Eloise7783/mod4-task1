pipeline {
  agent any
  stages {
    stage('build app container'){
      steps {
        sh "docker build -t flask-app ./var/lib/jenkins/workspace/task-1-pipeline/Dockerfile"
      }
    }
    stage('build nginx container'){
      steps {
        sh "docker build -t nginx ./var/lib/jenkins/workspace/task-1-pipeline/Dockerfile.nginx"
      }
    }
  }
}
