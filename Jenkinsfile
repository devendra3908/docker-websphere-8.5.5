#!groovy

pipeline {
  agent none
  stages {
    stage('Maven Install') {
      agent {
        docker {
         image 'maven:3.5.0'
        }
      }
      steps {
        sh 'mvn -version'
      }
    }
     stage('Docker Build image for Operating System') {
      agent any
      steps {
	          sh "docker build -t devendra3908/dockerwebsphere8.5.5:latest ."
      }
    }
  }
}
