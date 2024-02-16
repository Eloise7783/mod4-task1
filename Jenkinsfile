pipeline {
  agent any
    stages {
      stage('cleanup'){
        steps {
          sh "sh cleanup.sh || true"
        }
      }
      stage('build app container'){
        steps {
          sh "docker build -t flask-app ."
        }
      }
      stage('run flask app'){
        steps {
          sh "docker run -d --name flask-app"
        }
      }
      stage('build nginx container'){
        steps {
          sh "docker build -t nginx -f Dockerfile.nginx"
        }
      }
    }
  }
