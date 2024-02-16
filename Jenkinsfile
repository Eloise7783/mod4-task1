pipeline {
  agent any
    stages {
      stage('cleanup'){
        steps {
          sh "sh cleanup.sh || true"
        }
      }
      stage('create network'){
        steps {
          sh "docker network create taskonenetwork || true"
        }
      }
      stage('build app container'){
        steps {
          sh "docker build -t flask-app ."
        }
      }
      stage('run flask app'){
        steps {
          sh "docker run --name flask-app -dp 80:5500 --network taskonenetwork flask-app"
          
        }
      }
      stage('build nginx container'){
        steps {
          sh "docker build -t nginx Dockerfile.nginx"
        }
      }
      stage('run nginx'){
        steps {
          sh "docker run --name nginx -dp 80:80--network taskonenetwork nginx"
          
        }
      }
    }
  }
