pipeline {
  agent any
  stages {
    stage('Cloning Git') {
      steps {
        git 'https://github.com/arunagunasekera/node-hello-world.git'
      }
    }
    stage('Build') {
       steps {
         sh 'npm install'
       }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('package'){
        steps{
            sh 'npm pack'
        }
    }
    stage('deploy'){
        steps{
            sh 'npm install Hello-World-0.0.1.tgz'
        }
    }

  }
}

